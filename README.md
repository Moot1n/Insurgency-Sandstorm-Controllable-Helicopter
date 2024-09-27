Modpage: https://mod.io/g/insurgencysandstorm/m/controllable-helicopter \
The controllable helicopter is located at Content\Game\Actors\Vehicles\BP_VH_MyHeli3.uasset \
Also uses a rappel blueprint located at Content\Game\Actors\rappelDownHeliCable.uasset \

<div data-v-4785d160="" data-testid="" class="tw-w-full tw-relative tw-mb-6 xs:tw-mb-8 sm:tw-mb-12 tw-flex-col"><!----><div id="" class="tw-absolute tw--top-20 tw-h-px tw-w-full" style="z-index: -1;"></div><header class="tw-relative"><div class="tw-w-full tw-outline-none focus:tw-text-primary-hover"><div class="tw-w-full tw-flex tw-items-center tw-justify-between"><div class="tw-w-full tw-flex tw-items-center"><div class="tw-w-full tw-mb-5"><div class="tw-flex tw-flex-row tw-justify-between lg:tw-space-x-4 tw-space-y-4 lg:tw-space-y-0"><div class="tw-w-full tw-flex tw-flex-col tw-justify-center"><!----><h2 class="tw-flex tw-leading-tight tw-justify-start tw-text-left tw-font-normal tw-text-h4"><!----> Description <!----><!----></h2><!----></div><!----><!----></div></div><!----></div><!----></div></div><div class=""></div></header><div class="tw-w-full tw-global--border-radius tw-relative tw-rounded-tr-none tw-border-transparent tw-flex-col"><div class=""><!----><!----><div class="tw-flex tw-flex-col"><!----><div class="tw-content tw-view-text"><p>This mod adds a Minigun support Helicopter that can be controlled by players. There are two versus modes and five Co-op maps that include the helicopter. <br><br>The Helicopter spawns in the following scenarios:<br><br>To take off, power up the engine by holding W and then thrust upwards by holding shift. You can use spacebar to enable Auto Hover. You will rappel if you exit the helicopter while it is flying.</p>
<h2><strong>Controls:</strong></h2>
<p>W: Engine power up<br>S: Engine power down<br>Shift: Thrust Up<br>Z: Thrust Down<br>A: Yaw left<br>D: Yaw right<br>Up Arrow: Pitch down<br>Down Arrow: Pitch Up<br>Left Arrow: Roll Left<br>Right Arrow: Roll Right<br>Spacebar: Auto Hover</p>
<h3>To customize your controls:</h3>
<p>Go to "%localappdata%\Insurgency\Saved\Config\WindowsClient\"</p>
<p>Create a file called Game.ini and paste this in:</p>
<pre><code data-highlighted="yes" class="hljs language-ini"><span class="hljs-section">[/tankmap/Game/Actors/Vehicles/BP_VH_MyHeli3.BP_VH_MyHeli3_C]</span>
<span class="hljs-attr">KeyEngineUp</span> = Up
<span class="hljs-attr">KeyEngineDown</span> = Down
<span class="hljs-attr">KeyYawLeft</span> = Q
<span class="hljs-attr">KeyYawRight</span> = E
<span class="hljs-attr">KeyRollLeft</span> = A
<span class="hljs-attr">KeyRollRight</span> = D
<span class="hljs-attr">KeyPitchUp</span> = S
<span class="hljs-attr">KeyPitchDown</span> = W
<span class="hljs-attr">KeyThrustUp</span> = LeftShift
<span class="hljs-attr">KeyThrustDown</span> = Z
<span class="hljs-attr">KeyAutoHover</span> = SpaceBar </code></pre>
<p>Then set game.ini to <strong>READ ONLY<br></strong></p>
<h2><strong>Scenario List:</strong></h2>
<h3>Coop:</h3>
<p>Canyon_Heli?Scenario=Scenario_Crossing_Checkpoint_Helicopter<br>Farmhouse_Heli?Scenario=Scenario_Farmhouse_Checkpoint_Helicopter<br>Mountain_Heli?Scenario=Scenario_Summit_Checkpoint_Helicopter<br>Sinjar_Heli?Scenario=Scenario_Hillside_Checkpoint_Helicopter<br>Town_Heli?Scenario=Scenario_Hideout_Checkpoint_Helicopter</p>
<h3>Versus:</h3>
<p>Crackshack?Scenario=Scenario_Crackshack_Occupy<br>Mountain_Heli?Scenario=Scenario_Summit_Ambush_Helicopter</p>
<h2><strong>Mutators:</strong></h2>
<p>You should use the mutators if you wish to play the "_Heli" maps with the default scenarios. For example:</p>
<p><code>Farmhouse_Heli?Scenario=Scenario_Farmhouse_Survival -mutators=SpawnInHelicopter,EverywherePlayableHeli</code></p>
<p>Will let you spawn in a helicopter in the default farmhouse survival scenario, with invisible walls and restricted areas removed.</p>
<p><strong>EverywherePlayableHeli</strong><br>Removes all restricted areas and makes the playable area larger for the helicopter.&nbsp; This is mainly to get rid of the "You will die in 10 seconds" if you fly too high. You can configure the added width and height of the playable area in the config</p>
<p><strong>SpawnInHelicopter<br></strong>Will spawn a player in a flying helicopter at the start of the game. Should be used in combination with EverywherePlayableHeli. You can set which classes / team should spawn in the heli in the config. May not work well with most maps as there are invisible walls and restricted playable areas.<br>You can use the "_Heli" maps with the vanilla scenarios to get rid of the invisible walls.</p>
<p>&nbsp;</p>
<h2>Config (Game.ini):</h2>
<pre><code data-highlighted="yes" class="hljs language-swift">[<span class="hljs-regexp">/tankmap/</span><span class="hljs-type">Content</span><span class="hljs-regexp">/Mutators/</span><span class="hljs-type">BP_EverywherePlayableHeli</span>.<span class="hljs-type">BP_EverywherePlayableHeli_C</span>]
fPAExtraHeight<span class="hljs-operator">=</span><span class="hljs-number">100.000000</span> <span class="hljs-comment">// Adds extra height to the playable area so you can fly helicopter higher</span>
fPAExtraWidth<span class="hljs-operator">=</span><span class="hljs-number">10.000000</span> <span class="hljs-comment">// Adds extra width and length to the playable area so you can fly further outside the map</span>

[<span class="hljs-regexp">/tankmap/</span><span class="hljs-type">Content</span><span class="hljs-regexp">/Mutators/</span><span class="hljs-type">BP_SpawnInHelicopter</span>.<span class="hljs-type">BP_SpawnInHelicopter_C</span>]
fSpawnHeight<span class="hljs-operator">=</span><span class="hljs-number">8000.000000</span> <span class="hljs-comment">// The height above the spawn zone to spawn the heli. Make sure it is high as the heli is meant to spawn flying in the air</span>
bRestrictToTeam<span class="hljs-operator">=</span><span class="hljs-type">False</span> <span class="hljs-comment">// Set to true if the helicopter should only be for one team</span>
iHelicopterTeam<span class="hljs-operator">=</span><span class="hljs-number">0</span> <span class="hljs-comment">// 0 for security, 1 for insurgents</span>
tPilotClassName <span class="hljs-operator">=</span> <span class="hljs-type">Commander</span> <span class="hljs-comment">// If this value is set, only spawn players of a specific class in the heli. Remove this value to let any class spawn in the heli.</span></code></pre>
<h2>Other Notes</h2>
<p>In singleplayer, you can spawn in the heli with the following command:<br>"Summon BP_MyHeli3_C"</p>
<p><br>Path for custom objects mod: Assets=BlueprintGeneratedClass'/tankmap/Game/Actors/Vehicles/BP_VH_MyHeli3.BP_VH_MyHeli3_C'</p>
<p><br>Source code: <a href="https://github.com/Moot1n/Insurgency-Sandstorm-Controllable-Helicopter">https://github.com/Moot1n/Insurgency-Sandstorm-Controllable-Helicopter</a></p>
<p><br>Big thanks to the Insurgency: Sandstorm Modding Discord for help with troubleshooting!</p></div><!----></div></div><!----></div></div>
