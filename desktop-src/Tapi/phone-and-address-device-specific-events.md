---
description: Im folgenden Codebeispiel wird ein Ereignishandler für Adress-und Telefongeräte Ereignisse veranschaulicht. Der Code für jedes Ereignis zeigt, wie die Ereignis Schnittstelle erstellt wird und wie die Ereignisdaten abgerufen werden.
ms.assetid: 236d4e7f-865f-4b26-8da6-c86476588c47
title: Gerätespezifische Ereignisse per Telefon und adressieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40cf4c45eb7c7b933a36814f8eba8cd5cc39d8cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527584"
---
# <a name="phone-and-address-device-specific-events"></a><span data-ttu-id="62f2d-104">Gerätespezifische Ereignisse per Telefon und adressieren</span><span class="sxs-lookup"><span data-stu-id="62f2d-104">Phone and Address Device-specific Events</span></span>

<span data-ttu-id="62f2d-105">Im folgenden Codebeispiel wird ein Ereignishandler für Adress-und Telefongeräte Ereignisse veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="62f2d-105">The following code example illustrates an event handler for address and phone device events.</span></span> <span data-ttu-id="62f2d-106">Der Code für jedes Ereignis zeigt, wie die Ereignis Schnittstelle erstellt wird und wie die Ereignisdaten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="62f2d-106">The code for each event shows how to create the event interface and how to retrieve the event data.</span></span>

``` syntax
HRESULT STDMETHODCALLTYPE CMyEventNotification::Event(
   TAPI_EVENT TapiEvent,
   IDispatch * pEvent
)
{
    HRESULT hr = S_OK;
    //...
    switch (TapiEvent) 
    {
        case TE_ADDRESSDEVSPECIFIC:
        {
            ITAddressDeviceSpecificEvent* pITADSEvent = NULL;

            hr = pEvent->QueryInterface( 
                               IID_ITAddressDeviceSpecificEvent,
                               (void **)(&pITADSEvent) );
            // If (hr != S_OK) process the error here...

            // Retrieve data received from the TSP.
            long lParam1=0;
            hr = pITADSEvent->get_lParam1(&lParam1);
            // If (hr != S_OK) process the error here...

            long lParam2=0;
            hr = pITADSEvent->get_lParam2(&lParam2);
            // If (hr != S_OK) process the error here...

            long lParam3=0; 
            hr = pITADSEvent->get_lParam3(&lParam3);
            // If (hr !=S_OK) process the error here...

            // Process the data here.
            // ...
            pITADSEvent->Release();
            break;
        }

        case TE_PHONEDEVSPECIFIC:
        {
            ITPhoneDeviceSpecificEvent* pITPhEvent = NULL;

            hr = pEvent->QueryInterface( 
                            IID_ITPhoneDeviceSpecificEvent,
                            (void **)(&pITPhEvent) );
            // If (hr != S_OK) process the error here...

            // Retrieve data received from the TSP.
            long lParam1=0;
            hr = pITPhEvent->get_lParam1(&lParam1);
            // If (hr != S_OK) process the error here...

            long lParam2=0;
            hr = pITPhEvent->get_lParam2(&lParam2);
            // If (hr != S_OK) process the error here...

            long lParam3=0;
            hr = pITPhEvent->get_lParam3(&lParam3);
            // If (hr != S_OK) process the error here...

            // Process the data here.
            //...
            pITPhEvent->Release();
            break;
        }
        //...
    } // end of switch 
    //...
}
```

 

 



