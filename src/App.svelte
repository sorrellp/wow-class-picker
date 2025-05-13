<script>
    import confetti from "https://cdn.skypack.dev/canvas-confetti";

    const iconSets = {
        Tank: [
            {
                id: 1,
                role: "Tank",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/spell_deathknight_bloodpresence.jpg",
                name: "Blood Death Knight",
            },
            {
                id: 2,
                role: "Tank",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/ability_paladin_shieldofthetemplar.jpg",
                name: "Protection Paladin",
            },
            {
                id: 3,
                role: "Tank",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/ability_demonhunter_spectank.jpg",
                name: "Vengeance Demon Hunter",
            },
            {
                id: 4,
                role: "Tank",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/ability_racial_bearform.jpg",
                name: "Guardian Druid",
            },
            {
                id: 5,
                role: "Tank",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/monk_stance_drunkenox.jpg",
                name: "Brewmaster Monk",
            },
            {
                id: 6,
                role: "Tank",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/ability_warrior_defensivestance.jpg",
                name: "Protection Warrior",
            },
            
        ],
        Healer: [
            {
                id: 100,
                role: "Healer",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/classicon_evoker_preservation.jpg",
                name: "Preservation Evoker",
            },
            {
                id: 101,
                role: "Healer",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/spell_nature_healingtouch.jpg",
                name: "Restoration Druid",
            },
            {
                id: 102,
                role: "Healer",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/monk_stance_wiseserpent.jpg",
                name: "Mistweaver Monk",
            },
            {
                id: 103,
                role: "Healer",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/spell_holy_holybolt.jpg",
                name: "Holy Paladin",
            },
            {
                id: 104,
                role: "Healer",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/spell_holy_guardianspirit.jpg",
                name: "Holy Priest",
            },
            {
                id: 105,
                role: "Healer",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/spell_holy_powerwordshield.jpg",
                name: "Discipline Priest",
            },
            {
                id: 106,
                role: "Healer",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/spell_nature_magicimmunity.jpg",
                name: "Restoration Shaman",
            },
        ],
        "Melee DPS": [
            {
                id: 200,
                role: "Melee DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/spell_deathknight_frostpresence.jpg",
                name: "Frost Death Knight",
            },
            {
                id: 201,
                role: "Melee DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/spell_deathknight_unholypresence.jpg",
                name: "Unholy Death Knight",
            },
            {
                id: 202,
                role: "Melee DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/ability_demonhunter_specdps.jpg",
                name: "Havoc Demon Hunter",
            },
            {
                id: 203,
                role: "Melee DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/ability_druid_catform.jpg",
                name: "Feral Druid",
            },
            {
                id: 204,
                role: "Melee DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/ability_hunter_camouflage.jpg",
                name: "Survival Hunter",
            },
            {
                id: 205,
                role: "Melee DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/monk_stance_whitetiger.jpg",
                name: "Windwalker Monk",
            },
            {
                id: 206,
                role: "Melee DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/spell_holy_auraoflight.jpg",
                name: "Retribution Paladin",
            },
            {
                id: 207,
                role: "Melee DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/ability_rogue_eviscerate.jpg",
                name: "Assassination Rogue",
            },
            {
                id: 208,
                role: "Melee DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/ability_rogue_waylay.jpg",
                name: "Outlaw Rogue",
            },
            {
                id: 209,
                role: "Melee DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/ability_stealth.jpg",
                name: "Subtlety Rogue",
            },
            {
                id: 210,
                role: "Melee DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/spell_nature_lightningshield.jpg",
                name: "Enhancement Shaman",
            },
            {
                id: 211,
                role: "Melee DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/ability_warrior_innerrage.jpg",
                name: "Fury Warrior",
            },
            {
                id: 212,
                role: "Melee DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/ability_warrior_savageblow.jpg",
                name: "Arms Warrior",
            },
        ],
        "Ranged DPS": [
            {
                id: 300,
                role: "Ranged DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/spell_nature_starfall.jpg",
                name: "Balance Druid",
            },
            {
                id: 301,
                role: "Ranged DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/classicon_evoker_augmentation.jpg",
                name: "Augmentation Evoker",
            },
            {
                id: 302,
                role: "Ranged DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/classicon_evoker_devastation.jpg",
                name: "Devastation Evoker",
            },
            {
                id: 303,
                role: "Ranged DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/ability_hunter_bestialdiscipline.jpg",
                name: "Beast Mastery Hunter",
            },
            {
                id: 304,
                role: "Ranged DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/ability_hunter_focusedaim.jpg",
                name: "Marksmanship Hunter",
            },
            {
                id: 305,
                role: "Ranged DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/spell_fire_firebolt02.jpg",
                name: "Fire Mage",
            },
            {
                id: 306,
                role: "Ranged DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/spell_frost_frostbolt02.jpg",
                name: "Frost Mage",
            },
            {
                id: 307,
                role: "Ranged DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/spell_holy_magicalsentry.jpg",
                name: "Arcane Mage",
            },
            {
                id: 308,
                role: "Ranged DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/spell_shadow_shadowwordpain.jpg",
                name: "Shadow Priest",
            },
            {
                id: 309,
                role: "Ranged DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/spell_nature_lightning.jpg",
                name: "Elemental Shaman",
            },
            {
                id: 310,
                role: "Ranged DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/spell_shadow_deathcoil.jpg",
                name: "Affliction Warlock",
            },
            {
                id: 311,
                role: "Ranged DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/spell_shadow_metamorphosis.jpg",
                name: "Demonology Warlock",
            },
            {
                id: 312,
                role: "Ranged DPS",
                imgSrc: "https://wow.zamimg.com/images/wow/icons/large/spell_shadow_rainoffire.jpg",
                name: "Destruction Warlock",
            },
        ],
    };

    // Combine Melee DPS and Ranged DPS for the new DPS set
    const combinedDPSIcons = [
        ...iconSets["Melee DPS"],
        ...iconSets["Ranged DPS"],
    ];

    let excludedIcons = [];
    let highlightedIndex = -1;
    let isAnimating = false;
    let selectedIconName = "Unknown";
    let isIconSelected = false;

    let roles = [
        { name: "Tank", selected: false, img: "https://wow.zamimg.com/images/wow/icons/large/ability_warrior_shieldmastery.jpg" },
        { name: "Healer", selected: false, img: "https://wow.zamimg.com/images/wow/icons/large/spell_holy_flashheal.jpg" },
        { name: "DPS", selected: false, img: "https://wow.zamimg.com/images/wow/icons/large/inv_sword_24.jpg" },
        { name: "Melee DPS", selected: false, img: "https://wow.zamimg.com/images/wow/icons/large/inv_knife_1h_artifactfangs_d_05dual.jpg" },
        { name: "Ranged DPS", selected: false, img: "https://wow.zamimg.com/images/wow/icons/large/inv_111_hunter_ability_doubleknock.jpg" },
    ];

    $: selectedRole = roles.find((r) => r.selected)?.name;
    $: visibleIcons =
        selectedRole === "DPS"
            ? combinedDPSIcons.filter(
                  (icon) => !excludedIcons.includes(icon.id),
              )
            : selectedRole
              ? iconSets[selectedRole].filter(
                    (icon) => !excludedIcons.includes(icon.id),
                )
              : [
                    ...iconSets.Tank,
                    ...iconSets.Healer,
                    ...combinedDPSIcons,
                ].filter((icon) => !excludedIcons.includes(icon.id));

    $: canRandomize = visibleIcons.length > 0 && !isAnimating;

    function toggleRole(selectedRole) {
        roles = roles.map((role) => ({
            ...role,
            selected: role === selectedRole ? !role.selected : false,
        }));
    }

    function getRandomIndex(excludeIndex) {
        let index;
        do {
            index = Math.floor(Math.random() * visibleIcons.length);
        } while (index === excludeIndex && visibleIcons.length > 1);
        return index;
    }

    async function randomizeIcons() {
        if (isAnimating || visibleIcons.length === 0) return;
        isAnimating = true;
        isIconSelected = false;

        const totalSteps = 20 + Math.floor(Math.random() * 10);
        let delay = 100;
        let currentIndex = highlightedIndex;

        for (let i = 0; i < totalSteps; i++) {
            currentIndex = getRandomIndex(currentIndex);
            highlightedIndex = currentIndex;
            selectedIconName =
                visibleIcons[highlightedIndex]?.name || "Unknown";
            await new Promise((resolve) => setTimeout(resolve, delay));

            if (i > totalSteps * 0.7) delay += 25;
            else if (i > totalSteps * 0.4) delay += 18;
            else delay += 14;
        }

        isIconSelected = true;

        confetti({
            particleCount: 200,
            spread: 70,
            origin: { x: 1 },
            colors: ["#ff0", "#ff6347", "#32cd32"],
        });
        confetti({
            particleCount: 200,
            spread: 70,
            origin: { x: 0 },
            colors: ["#ff0", "#ff6347", "#32cd32"],
        });

        isAnimating = false;
    }

    function toggleExclude(icon) {
        if (isAnimating) return;
        if (excludedIcons.includes(icon.id)) {
            excludedIcons = excludedIcons.filter((id) => id !== icon.id);
        } else {
            excludedIcons = [...excludedIcons, icon.id];
        }
    }
</script>

<!-- Role Toggles -->
<div class="role-toggles">
    {#each roles as role}
        <button
            type="button"
            class="role-toggle"
            class:selected={role.selected}
            class:disabled-role={isAnimating}
            on:click={() => !isAnimating && toggleRole(role)}
            disabled={isAnimating}
        >
            <span>{role.name}</span>
            <img src="{role.img}" alt={role.name} />
        </button>
    {/each}
</div>

<!-- Icon Grid -->
<div class="icon-grid">
    {#each visibleIcons as icon, index}
        <a
            on:click={() => toggleExclude(icon)}
            class:highlighted={index === highlightedIndex}
            class:disabled={isAnimating}
        >
            <img
                src={icon.imgSrc || "https://picsum.photos/200"}
                alt={icon.name || "Static Icon"}
            />
        </a>
    {/each}
</div>

<!-- Selected Icon Name (Only Show After Selection) -->
{#if isIconSelected && highlightedIndex !== -1}
    <div style="text-align: center; margin-top: 1rem;">
        <p class="selected-icon-name">{selectedIconName}</p>
    </div>
{/if}

<!-- Excluded Icons -->
<div class="excluded-grid">
    <h3>Excluded</h3>
    <div class="icon-grid">
        {#each excludedIcons as id}
            {#each [...iconSets.Tank, ...iconSets.Healer, ...combinedDPSIcons] as icon}
                {#if icon.id === id}
                    <a on:click={() => toggleExclude(icon)} class:disabled-excluded={isAnimating} class:disabled={isAnimating}>
                        <img src={icon.imgSrc} alt={icon.name} />
                    </a>
                {/if}
            {/each}
        {/each}
    </div>
</div>

<!-- Randomize Button -->
<div style="text-align: center;">
    <button on:click={randomizeIcons} disabled={!canRandomize}>Randomize</button
    >
</div>

<style>
    :global(body) {
        font-family: Arial, sans-serif;
        background-color: lch(21.08% 10.18 285.53);
        color: #ffffff;
        margin: 0;
        padding: 2rem;
    }

    .role-toggles {
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        gap: 1rem;
        margin-bottom: 2rem;
    }

    .role-toggle {
        display: flex;
        flex-direction: column;
        align-items: center;
        cursor: pointer;
        background: none;
        border: none;
        padding: 0;
        outline: none;
        color: white;
    }

    .role-toggle img {
        width: 64px;
        height: 64px;
        border-radius: 8px;
        border: 2px solid transparent;
        transition:
            border 0.2s,
            box-shadow 0.2s;
    }

    .role-toggle.selected img {
        border-color: dodgerblue;
        box-shadow: 0 0 8px rgba(30, 144, 255, 0.6);
    }

    .role-toggle span {
        margin-bottom: 0.4rem;
        font-size: 0.9rem;
        text-align: center;
    }

    .icon-grid {
        display: grid;
        grid-template-columns: repeat(6, 1fr);
        gap: 1rem;
        justify-items: center;
        margin-bottom: 1rem;
    }

    .icon-grid a {
        cursor: pointer;
    }

    .icon-grid a.disabled {
        cursor: not-allowed;
    }

    .icon-grid a img {
        width: 64px;
        height: 64px;
        object-fit: cover;
        border-radius: 8px;
        transition:
            border 0.2s,
            box-shadow 0.2s;
        border: 2px solid transparent;
    }

    .icon-grid a.highlighted img {
        border-color: gold;
        box-shadow: 0 0 15px rgba(255, 215, 0, 0.7);
    }

    .excluded-grid {
        text-align: center;
        margin-top: 2rem;
    }

    .excluded-grid h3 {
        margin-bottom: 1rem;
    }

    button {
        padding: 0.5rem 1rem;
        font-size: 1rem;
        cursor: pointer;
    }

    .selected-icon-name {
        font-size: 1.5rem;
        font-weight: bold;
        color: rgb(255, 255, 255);
    }

    .role-toggle {
        cursor: pointer;
    }

    .role-toggle.disabled-role {
        cursor: not-allowed;
        opacity: 0.6;
    }

    .disabled-excluded {
        cursor: not-allowed;
        opacity: 0.6;
    }
</style>
