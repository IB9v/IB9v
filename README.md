import org.bukkit.Bukkit;
import org.bukkit.command.Command;
import org.bukkit.command.CommandSender;
import org.bukkit.entity.EnderDragon;
import org.bukkit.entity.Entity;
import org.bukkit.entity.Player;
import org.bukkit.event.EventHandler;
 @@ -41,6 +42,8 @@ public void onDamageEvent(EntityDamageByEntityEvent e){
        Entity ent = e.getEntity();
        if (getConfig().getBoolean("PlayerOnly") && !(ent instanceof Player))
            return;
        if (!getConfig().getBoolean("ApplyToDragon") && ent instanceof EnderDragon)
            return;
        ent.setVelocity(d.getLocation().getDirection().setY(0).normalize().multiply(multiplier));
    }
