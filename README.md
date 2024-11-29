# Weapon-Detection-Cs2
A cs2 cfg framework to detect the weapon you are holding. This can be used to change your crosshair/binds depending on the item you are holding.

This is the original soundinfo detection config. It works without the bible config (exec_async exploit).

This implementation takes the duration a sound got played into account -> works better when being spammed (multiple fast weapon switches)

It's still not perfect, since the game skips playing sounds for the same weapon twice, but shouldn't be an issue in most situations.

Another important note is, that the key_up input has to happen withing 0.5s of the key_down input, since weapon-switch sounds have a pretty short duration.

You can alias your stuff either directly to the weapon aliases in ```WeaponDetect/init``` or create new aliases named ```item_[name]``` and call them by doing ```CurrentItem | toggle "cmd;"```

Read ```WeaponDetect/binds``` for more information.
