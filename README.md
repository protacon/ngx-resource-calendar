# NgxResourceCalendar

## What is this?

Resource calendar for Angular 8+

## Install

### Step 1: Install @protacon/ngx-resource-calendar

```bash
$ npm install --save @protacon/ngx-resource-calendar
```

### Step 2: Import the module

Add `NgxResourceCalendarModule` as an import in your app's root NgModule.

```typescript
import { NgxResourceCalendarModule }  from '@protacon/ngx-resource-calendar';

@NgModule({
  ...
  imports: [
    ...
    NgxResourceCalendarModule,
  ],
  ...
})
export class AppModule { }
```

## Usage

Simple usage example

```html
<ptc-resource-calendar
  [dates]="dates"
  [events]="events"
  [infoTemplate]="infoTemplate"
  [hourTemplate]="hourTemplate"
>
</ptc-resource-calendar>
<ng-template #infoTemplate>
  Info view
</ng-template>
<ng-template #hourTemplate let-slot="slot">
  <div>{{ slot.time | data: 'shortTime' }}</div>
</ng-template>
```

| Attribute               | Description                                                                    | Template output                                              |
| ----------------------- | ------------------------------------------------------------------------------ | ------------------------------------------------------------ |
| `dates`                 | Specifies the dates and resources which calendar shows                         |                                                              |
| `events`                | Events to show in calendar                                                     |                                                              |
| `slotDurationInMinutes` | How many minutes one slot is. Default 15 minutes.                              |                                                              |
| `height`                | Heigh of one slot in pixels. Default 60px.                                     |                                                              |
| `hourBorderHeight`      | Height between slots when hour changes like border or margin etc. Default 1px. |                                                              |
| `infoTemplate`          | A custom template to use for the header empty space top of hours.              | -                                                            |
| `dayTemplate`           | A custom template to use for day view in header                                | day = DateModel                                              |
| `resourceTemplate`      | A custom template to use for day view resource in header (below day template)  | resource = ResourceModel                                     |
| `hourTemplate`          | A custom template to use for hour view (left to calendar)                      | slot = SlotModel                                             |
| `eventTemplate`         | A custom template to use for events                                            | event = EventModel, resource = ResourceModel, day = DayModel |
| `slotTemplate`          | A custom template to use for slots                                             | slot = SlotModel, resource = ResourceModel, day = DayModel   |
| `currentTimeTemplate`   | A custom template to show current time etc. custom overlay                     | day = DateModel                                              |

## License

[The MIT License (MIT)](LICENSE)

Copyright (c) 2020 [Pinja](https://www.pinja.com)
