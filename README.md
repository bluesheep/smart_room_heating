# Smart Room heating
A breakdown of how I built my smart, room-based heating system. Full disclosure too, despite the way the right up sounds, this was built over a period of about 6 months, with lots of mistakes and tweaks along the way. I've tried to provide as much detail as makes sense, but haven't included things like installing HA, or adding sensors to your HA. 

If you are following along, good luck!

## Physical BOM

- [Nest Thermostat](https://store.google.com/us/product/nest_learning_thermostat_3rd_gen?hl=en-US) (only because it was what was installed before)
- [Sandy Beach Zigbee TRV](https://www.amazon.co.uk/gp/aw/d/B09HP3HJ36/?_encoding=UTF8&pd_rd_plhdr=t&aaxitk=4abe6f79b148b584eb6894c9d5675445&hsa_cr_id=0&qid=1703843258&sr=1-2-e0fa1fdd-d857-4087-adda-5bd576b25987&ref_=sbx_be_s_sparkle_mcd_asin_1_title&pd_rd_w=VYjyl&content-id=amzn1.sym.25f7c301-a223-4ff8-91c9-accfeab9fda8%3Aamzn1.sym.25f7c301-a223-4ff8-91c9-accfeab9fda8&pf_rd_p=25f7c301-a223-4ff8-91c9-accfeab9fda8&pf_rd_r=6ZNJ1TDBTKQJV87WB5G8&pd_rd_wg=CFMpM&pd_rd_r=d2c1d0e4-a3ed-43ad-976f-bdc49325aaec&th=1) Any Zigbee TRV should work, provided it exposes the correct entities)
- [Sonoff SNZB-02](https://www.amazon.co.uk/SNZB-02-Temperature-Humidity-Compatible-Including/dp/B08BFW697F/ref=sr_1_5?crid=38HO16WLJBRRV&keywords=sonoff%2Bsnzb-02&qid=1703844221&sprefix=sonoff%2Bsnzb-02%2Caps%2C93&sr=8-5&th=1) (again, any ambient temp sensor should work)
- [TRV Spacer](https://www.thingiverse.com/thing:5030674)

## Digital BOM

- [Home Assistant](https://www.home-assistant.io/)
- [Scheduler custom component](https://github.com/nielsfaber/scheduler-component)
- [Better Thermostat custom component](https://github.com/KartoffelToby/better_thermostat)

## Overall Design

1. Configure Nest to operate as a switch rather than a thermostat
   - Set sensible thresholds
   - Create duty cycle to prevent rapid switching
2. Fit TRVs
   - Add spacers as required
4. Configure Better Thermostat to use room sensors and TRVs
6. Link radiator demand for heat to Nest instruction for boiler
   - Set sensible configuration values
7. Create Dashboard

## Nest Configuration

## TRV Installation

## Better Thermostat

## Heating Automation

## Dashboard

## Future Plans

- Replace Nest with pair of ZBMinis. I'm hesitating on this because I'll still have a hole in the wall where the Nest is mounted.
- Room centric heating controls/indicators. Something to show when the heating is on in a room. Can't decide if I should just go with room tablets or something in the microcontroller space.
