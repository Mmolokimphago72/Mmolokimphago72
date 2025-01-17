- 👋 Hi, I’m @Mmolokimphago72
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Mmolokimphago72/Mmolokimphago72 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
<xml xmlns="http://www.w3.org/1999/xhtml">
  <variables>
    <variable name="stake">1</variable>
    <variable name="duration">1</variable>
    <variable name="over_under">"over"</variable>
    <variable name="rsi_period">14</variable>
    <variable name="rsi_overbought">70</variable>
    <variable name="rsi_oversold">30</variable>
  </variables>
  <block type="trade_definition">
    <field name="TRADETYPE">Rise/Fall</field>
    <field name="CONTRACTTYPE">CALL</field>
    <value name="AMOUNT">
      <shadow type="math_number">
        <field name="NUM">1</field>
      </shadow>
    </value>
    <value name="DURATION">
      <shadow type="math_number">
        <field name="NUM">1</field>
      </shadow>
    </value>
    <value name="DURATION_UNIT">
      <shadow type="text">
        <field name="TEXT">ticks</field>
      </shadow>
    </value>
    <value name="ASSET">
      <shadow type="text">
        <field name="TEXT">Volatility 10 (1s)</field>
      </shadow>
    </value>
  </block>
  <block type="indicator_rsi">
    <field name="PERIOD">14</field>
    <value name="CONDITION">
      <block type="logic_compare">
        <field name="OP">GT</field>
        <value name="A">
          <block type="math_number">
            <field name="NUM">70</field>
          </block>
        </value>
        <value name="B">
          <block type="rsi">
            <field name="SYMBOL">Volatility 10 (1s)</field>
            <field name="PERIOD">14</field>
          </block>
        </value>
      </block>
    </value>
  </block>
</xml>
