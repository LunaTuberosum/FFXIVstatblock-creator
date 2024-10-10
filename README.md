# FFXIV Stat Block Creator
### By: Luna Tuberosum

With this project you will be able to use HTML to make Stat Cards for the FFXIV TTRPG. The files included with this project are some example Stat Cards to help you have a start and refrence when making your own.

The included Stat Cards are:
> Vodyanoi & Toxic Toad; From the Free Trail FATE

> Odin, The Unbroken; From Minstrel's Ballad: Lord of the Corpse Hall by TheVagueOne on the Discord

This show off how the Stat Card works and fuctions as well as how to make Traits, Abilites (Single target, Stationary Marker, Mobile Marker, and Raid Wides), and how to make a multi-card page for your complex encounters.

To use this you will need a rudmentery understanding of how to write HTML. You DO NOT need to know how to write CSS. The CSS is already done and will format things if done correctly. The HTML always starts at line 225.

If you run into any problems please message me on Discord.

---
### How to Download and Use


1. Click on [<> Code] in the top right.
2. Click [Download ZIP] (Optional if you are familiar with GitHub and have an account just clone the Repo)
3. Unzip the ZIP file into another folder
4. Download a IDE; EX: VS Code (If you dont have one)
5. Open folder in IDE
6. Change files all you want and view them through local host. (Look it up if you dont know how to)
7. Enjoy

---
There are a couble of unique HTML elements you use in your descriptions of Traits and Abilites, they are detailed below:

| HTML Element | Change | Uses |
|--------------|--------|------|
| \<r> text \</r> | Makes the text a brownish red | For keywords in Abilities <br> EX: Target:, Base Effect, or Marker Area: |
| \<a> text \</a> | Makes the text a greyish blue | For Attributes and Keywords <br> EX: STR, DEX, Primary Action, Instant |
| \<k> text \</k> | Makes the text a brigthish red | For Ability names <br> EX: Fire, Fire II, Lap, Labored Jump
| \<in>\</in> Ability Name | Adds a box saying INVK | For Invoked Abilities

The use of some regular HTML elements are also need for pretty formating, these are their uses:
| HTML Element | Change | Uses |
|--------------|--------|------|
| \<b> text \</b> | Makes the text bold | For Enhancements, Enfeeblements, Inter-Ability Terms <br> EX: Umbral Ice, DOT (3), proc, Emnity |
| \<i> text \</i> | Makes the text italized | For Ability Types <br> EX: Ice-Aspected, Magic, Physical |

---
### Structure

I find it easiest to structure your files as so. But please do how ever pleases you.

```
Folder: Character Name
    HTML file: Character Name Simple
    *Marker Images: Named after their ability
```

This makes it so everything is orginized and in the HTML file when refrencing a Marker Image you can do so with relative path.

---
### Formating and Refrences

And for refrence here is what Traits and each Ability type looks like in HTML

### Traits
```
<ability-block>
    <header>
        <h2> Trait Name </h2>
    </header>
    <p> Trait Effect </p>    
</ability-block>
```

### Ability - Unqiue
```
<ability-block>
    <header>
        <h2> Ability Name </h2>
        <h1> Ability Types, Unique</h1>
    </header>
    <p><r>Base Effect:</r> Effect </p>
</ability-block>
```

### Ability - Single Target
```
<ability-block>
    <header>
        <h2> Ability Name </h2>
        <h1> Ability Types </h1>
    </header>
    <p><r>Target:</r> Single <r>Range:</r> X squares</p>
    <p><r>Check:</r> <a> Attribute </a> (d20+X) <r>CR:</r> Target's <a> Defense Type </a></p>
    <p><r>Base Effect:</r> Effect </p>
    <p><r>Direct Hit:</r> Effect </p>
</ability-block>
```

### Ability - Stationary Marker
```
<ability-block>
    <header>
        <h2> Ability Name </h2>
        <h1> Ability Types, Stationary Marker </h1>
    </header>
    <lower>
        <desc>
            <p><r>Origin:</r> Origin </p>
            <p><r>Marker Area:</r> A stationary YxY area centered on the origin</p>
            <p><r>Target:</r> All enemies within the marker area</p>
            <p><r>Marker Trigger:</r> The beginning of this character's next turn</p>
            <p><r>Marker Effect:</r> Deals Xd6 damage to all targets.</p>
        </desc>
        <img src="./ImageName.png" alt="">
    </lower>
</ability-block>
```

### Ability - Mobile Marker
```
<ability-block>
    <header>
        <h2> Ability Name </h2>
        <h1> Ability Types, Mobile Marker </h1>
    </header>
    <lower>
        <desc>
            <p><r>Origin:</r> Origin </p>
            <p><r>Marker Area:</r> A mobile YxY area centered on the origin that moves with the origin</p>
            <p><r>Target:</r> All enemies within the marker area</p>
            <p><r>Marker Trigger:</r> The beginning of this character's next turn</p>
            <p><r>Marker Effect:</r> Deals Xd6 damage to all targets </p>
        </desc>
        <img src="./ImageName.png" alt="">
    </lower>
</ability-block>
```

### Ability - Raid Wide
```
<ability-block>
    <header>
        <h2> Ability Name </h2>
        <h1> Ability Types </h1>
    </header>
    <p><r>Marker Area:</r> The entire encounter map</p>
    <p><r>Target:</r> All enemies within the marker area</p>
    <p><r>Marker Trigger:</r> The beginning of this character's next turn</p>
    <p><r>Marker Effect:</r> Deals Xd6 damage to all targets.</b></p>
</ability-block>
```