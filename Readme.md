# How to handle a weekly recurrence rule in different time zones


<p>This example illustrates how to handle a problem reported in the <a href="https://www.devexpress.com/Support/Center/p/Q240871">Recurrence - incorrect start/end dates when creating recurring appointments in Eastern Australian Timezone</a> issue.<br />
When scheduler clients are located in different time zones, a question arises on how different recurring rules should be handled. Consider a weekly recurrence rule. A day of the week specified in the recurrence rule after applying time zone difference may become another day of the week. A similar complexity is involved when dealing with the monthly recurrence - every first Thursday of every month may become Wednesday in another time zone. Whether it breaks the recurrence rule or not, it is the question posed to a developer. Perhaps, there is no general solution to this problem.<br />
You can use the approach taken in this example to implement your own solution.</p><p>In this example the AppointmentFormShowing and BeforeExecuteCallbackCommand events are handled to replace default form container and a callback command. These steps are required to create and use a custom AppointmentFormController that properly modifies the start date of an appointment which is edited in the form.<br />
This approach can be used in ASPxScheduler starting at version v2009 vol.2.10 and higher.</p><p>Note that the formatting service for the TimeRuler is substituted to make the scheduler view more descriptive.</p>

<br/>

