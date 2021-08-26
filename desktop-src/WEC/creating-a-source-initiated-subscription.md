---
title: Erstellen eines quellinitiiertes Abonnement
description: Quellinitiierte Abonnements ermöglichen es Ihnen, ein Abonnement auf einem Ereignissammlercomputer zu definieren, ohne die Ereignisquellcomputer zu definieren. Anschließend können mehrere Remoteereignisquellcomputer (mithilfe einer Gruppenrichtlinieneinstellung) eingerichtet werden, um Ereignisse an den Ereignissammlercomputer weiterzuleiten. Bevor ein lokaler Computer Ereignisse abonnieren kann und ein Remotecomputer Ereignisse weiterleiten kann, müssen beide Computer für die Ereignissammlung und Ereignisweiterleitung eingerichtet werden. Weitere Informationen zum Konfigurieren der Computer finden Sie unter Einrichten eines von der Quelle initiierten Abonnements.
ms.assetid: 489d3613-177f-4045-a055-2c1577ef2191
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 771a70758a57134cdaabd8a9a72e3ad43c8bb890
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887288"
---
# <a name="creating-a-source-initiated-subscription"></a>Erstellen eines quellinitiiertes Abonnement

Quellinitiierte Abonnements ermöglichen es Ihnen, ein Abonnement auf einem Ereignissammlercomputer zu definieren, ohne die Ereignisquellcomputer zu definieren. Anschließend können mehrere Remoteereignisquellcomputer (mithilfe einer Gruppenrichtlinieneinstellung) eingerichtet werden, um Ereignisse an den Ereignissammlercomputer weiterzuleiten. Bevor ein lokaler Computer Ereignisse abonnieren kann und ein Remotecomputer Ereignisse weiterleiten kann, müssen beide Computer für die Ereignissammlung und Ereignisweiterleitung eingerichtet werden. Weitere Informationen zum Konfigurieren der Computer finden Sie unter Einrichten eines von [der Quelle initiierten Abonnements.](setting-up-a-source-initiated-subscription.md)

Das folgende Codebeispiel folgt einer Reihe von Schritten zum Erstellen eines von der Quelle initiierten Abonnements, bei dem sich die Ereignisquellen in derselben Domäne wie der Ereignissammlercomputer befinden.

**So erstellen Sie programmgesteuert ein von der Quelle initiiertes Abonnement**

1.  Öffnen Sie das Abonnement, indem Sie den Abonnementnamen und die Zugriffsrechte als Parameter für die [**EcOpenSubscription-Funktion**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) bereitstellen. Weitere Informationen zu Zugriffsrechten finden Sie unter [**Windows Event Collector-Konstanten.**](windows-event-collector-constants.md)
2.  Legen Sie die Eigenschaften des Abonnements fest, indem Sie die [**EcSetSubscriptionProperty-Funktion**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty) aufrufen. Weitere Informationen zu Abonnementeigenschaften, die festgelegt werden können, finden Sie in der [**EC \_ SUBSCRIPTION PROPERTY \_ \_ ID-Enumeration.**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id)
3.  Speichern Sie das Abonnement, indem Sie die [**EcSaveSubscription-Funktion**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) aufrufen.
4.  Schließen Sie das Abonnement, indem Sie die [**EcClose-Funktion**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) aufrufen.

Das folgende C++-Beispiel zeigt, wie Sie ein quellinitiiertes Abonnement erstellen:


```C++
#include <windows.h>
#include <iostream>
using namespace std;
#include <string>
#include <xstring>
#include <conio.h>
#include <EvColl.h>
#include <vector>
#include <wincred.h>
#pragma comment(lib, "credui.lib")
#pragma comment(lib, "wecapi.lib")

// Track properties of the Subscription.
typedef struct _SUBSCRIPTION_SOURCE_INITIATED
{
    std::wstring Name;
    EC_SUBSCRIPTION_TYPE SubscriptionType;
    std::wstring Description;
    BOOL SubscriptionStatus;
    std::wstring URI;
    EC_SUBSCRIPTION_CONFIGURATION_MODE ConfigMode;
    EC_SUBSCRIPTION_DELIVERY_MODE DeliveryMode;
    DWORD MaxItems;
    DWORD MaxLatencyTime;
    DWORD HeartbeatInerval;
    time_t Expires;
    std::wstring Query;
    BOOL ReadExistingEvents;
    std::wstring TransportName;
    EC_SUBSCRIPTION_CONTENT_FORMAT ContentFormat;
    std::wstring DestinationLog;
    std::wstring AllowedSourceNonDomainComputers;
    std::wstring AllowedSourceDomainComputers;

} SUBSCRIPTION_SOURCE_INITIATED;

// Subscription Information
DWORD GetProperty(EC_HANDLE hSubscription,  
                  EC_SUBSCRIPTION_PROPERTY_ID propID, 
                  DWORD flags, 
                  std::vector<BYTE>& buffer, 
                  PEC_VARIANT& vProperty);


void __cdecl wmain()
{
    LPVOID lpwszBuffer;
    DWORD dwRetVal = ERROR_SUCCESS;
    EC_HANDLE hSubscription;
    EC_VARIANT vPropertyValue;
    std::vector<BYTE> buffer;
    PEC_VARIANT vProperty = NULL;
    SUBSCRIPTION_SOURCE_INITIATED sub;

    sub.Name = L"TestSubscription-SourceInitiated";
    sub.SubscriptionType = EcSubscriptionTypeSourceInitiated;
    sub.Description = L"A subscription that collects events that are published in\n" \
        L"the Microsoft-Windows-TaskScheduler/Operational log and forwards them \n" \
        L"to the ForwardedEvents log.";
    sub.URI = L"http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog";
    sub.Query = L"<QueryList>" \
        L"<Query Path=\"Microsoft-Windows-TaskScheduler/Operational\">" \
        L"<Select>*</Select>" \
        L"</Query>" \
        L"</QueryList>";
    sub.DestinationLog = L"ForwardedEvents";
    sub.ConfigMode = EcConfigurationModeCustom;
    sub.MaxItems = 5;
    sub.MaxLatencyTime = 1000;
    sub.HeartbeatInerval = 60000;
    sub.DeliveryMode = EcDeliveryModePush;
    sub.ContentFormat = EcContentFormatRenderedText;
    sub.ReadExistingEvents = true;
    sub.SubscriptionStatus = true;
    sub.TransportName = L"http";

    // This SDDL grants members of the Domain Computers domain group as well
    // as members of the Network Service group (for the local forwarder),
    // the ability to raise events for this subscription.
    sub.AllowedSourceDomainComputers = L"O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)";


    // Step 1: Open the Event Collector subscription.
    hSubscription = EcOpenSubscription(sub.Name.c_str(),
        EC_READ_ACCESS | EC_WRITE_ACCESS, 
        EC_CREATE_NEW);
    if ( !hSubscription)
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 2: Define the subscription properties.
    // Set the subscription type property (collector initiated).
    vPropertyValue.Type = EcVarTypeUInt32;
    vPropertyValue.UInt32Val = sub.SubscriptionType;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionType,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the Description property that contains a description
    // of the subscription.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.Description.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionDescription,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }    

    // Set the URI property that specifies the URI of all the event sources.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.URI.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionURI,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the Query property that defines the query used by the event
    // source to select events that are forwarded to the event collector.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.Query.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionQuery,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the Log File property that specifies where the forwarded events
    // will be stored.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.DestinationLog.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionLogFile,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the ConfigurationMode property that specifies the mode in which events 
    // are delivered.
    vPropertyValue.Type = EcVarTypeUInt32;
    vPropertyValue.UInt32Val = sub.ConfigMode;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionConfigurationMode,
        NULL,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // If the Configuration Mode is Custom, set the DeliveryMode, DeliveryMaxItems,
    // HeartbeatInterval, and DeliveryMaxLatencyTime properties.
    if ( sub.ConfigMode == EcConfigurationModeCustom)
    {
        // Set the DeliveryMode property that defines how events are delivered. 
        // Events can be delivered through either a push or pull model.
        vPropertyValue.Type = EcVarTypeUInt32;
        vPropertyValue.UInt32Val = sub.DeliveryMode;
        if (!EcSetSubscriptionProperty(hSubscription,
            EcSubscriptionDeliveryMode,
            NULL,
            &vPropertyValue))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }

        // Set the DeliveryMaxItems property that specifies the maximum number of 
        // events that can be batched when forwarded from the event sources.
        vPropertyValue.Type = EcVarTypeUInt32;
        vPropertyValue.UInt32Val = sub.MaxItems;
        if (!EcSetSubscriptionProperty(hSubscription,
            EcSubscriptionDeliveryMaxItems,
            NULL,
            &vPropertyValue))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }

        // Set the HeartbeatInterval property that defines the time interval, in 
        // seconds, that is observed between the heartbeat messages.
        vPropertyValue.Type = EcVarTypeUInt32;
        vPropertyValue.UInt32Val = sub.HeartbeatInerval;
        if (!EcSetSubscriptionProperty(hSubscription,
            EcSubscriptionHeartbeatInterval,
            NULL,
            &vPropertyValue))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }

        // Set the DeliveryMaxLatencyTime property that specifies how long, in 
        // seconds, the event source should wait before forwarding events.
        vPropertyValue.Type = EcVarTypeUInt32;
        vPropertyValue.UInt32Val = sub.MaxLatencyTime;
        if (!EcSetSubscriptionProperty(hSubscription,
            EcSubscriptionDeliveryMaxLatencyTime,
            NULL,
            &vPropertyValue))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }
    }

    // Set the ContentFormat property that specifies the format for the event content.
    vPropertyValue.Type = EcVarTypeUInt32;
    vPropertyValue.UInt32Val = sub.ContentFormat;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionContentFormat,
        0,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the ReadExistingEvents property that is used to enable or disable whether
    // existing events are forwarded.
    vPropertyValue.Type = EcVarTypeBoolean;
    vPropertyValue.BooleanVal = sub.ReadExistingEvents;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionReadExistingEvents,
        0,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the Enabled property that is used to enable or disable the subscription
    // or to obtain the current status of a subscription.
    vPropertyValue.Type = EcVarTypeBoolean;
    vPropertyValue.BooleanVal = sub.SubscriptionStatus;
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionEnabled,
        0,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Set the TransportName property that determines the type of 
    // transport used by the subscription.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.TransportName.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionTransportName,
        0,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Required:
    // Set the AllowedSourceDomainComputers property to the specified SDDL.
    vPropertyValue.Type = EcVarTypeString;
    vPropertyValue.StringVal = sub.AllowedSourceDomainComputers.c_str();
    if (!EcSetSubscriptionProperty(hSubscription,
        EcSubscriptionAllowedSourceDomainComputers,
        0,
        &vPropertyValue))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    //----------------------------------------------
    // Step 3: Save the subscription.
    // Save the subscription with the associated properties
    // This will create the subscription and store it in the 
    // subscription repository 
    if( !EcSaveSubscription(hSubscription, NULL) )
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 4: Close the subscription.
Cleanup:
    if(hSubscription)
        EcClose(hSubscription);

    if (dwRetVal != ERROR_SUCCESS)
    {
        FormatMessageW( FORMAT_MESSAGE_ALLOCATE_BUFFER | FORMAT_MESSAGE_FROM_SYSTEM,
            NULL,
            dwRetVal,
            0,
            (LPWSTR) &lpwszBuffer,
            0,
            NULL);

        if (!lpwszBuffer)
        {
            wprintf(L"Failed to FormatMessage.  Operation Error Code: %u." \
                L"Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
            return;
        }

        wprintf(L"\nFailed to Perform Operation.\nError Code: %u\n" \
            L" Error Message: %s\n", dwRetVal, lpwszBuffer);

        LocalFree(lpwszBuffer);
    }
}

DWORD GetProperty(EC_HANDLE hSubscription, 
                  EC_SUBSCRIPTION_PROPERTY_ID propID, 
                  DWORD flags, 
                  std::vector<BYTE>& buffer, 
                  PEC_VARIANT& vProperty)
{
    DWORD  dwBufferSize, dwRetVal = ERROR_SUCCESS;
    buffer.resize(sizeof(EC_VARIANT));

    if (!hSubscription)
        return ERROR_INVALID_PARAMETER;

    // Get the value for the specified property. 
    if (!EcGetSubscriptionProperty(hSubscription,
        propID, 
        flags, 
        (DWORD) buffer.size(), 
        (PEC_VARIANT)&buffer[0], 
        &dwBufferSize) )
    {
        dwRetVal = GetLastError();

        if (ERROR_INSUFFICIENT_BUFFER == dwRetVal)
        {
            dwRetVal = ERROR_SUCCESS;
            buffer.resize(dwBufferSize);

            if (!EcGetSubscriptionProperty(hSubscription,
                propID,
                flags,
                (DWORD) buffer.size(),
                (PEC_VARIANT)&buffer[0],
                &dwBufferSize))
            {
                dwRetVal = GetLastError();
            }
        }
    }

    if (dwRetVal == ERROR_SUCCESS)
    {
        vProperty = (PEC_VARIANT) &buffer[0];
    }
    else
    {
        vProperty = NULL;
    }

    return dwRetVal;
}
```



**Überprüfen, ob das Abonnement ordnungsgemäß funktioniert**

1.  Führen Sie auf dem Ereignissammlercomputer das folgende Verfahren aus:

    1.  Führen Sie den folgenden Befehl an einer Eingabeaufforderung mit erhöhten Rechten aus, um den Laufzeitstatus des Abonnements abzurufen:

        **wecutil gr** *&lt; subscriptionID &gt;*

    2.  Vergewissern Sie sich, dass eine Verbindung mit der Ereignisquelle hergestellt wurde. Möglicherweise müssen Sie warten, bis das in der Richtlinie angegebene Aktualisierungsintervall beendet ist, nachdem Sie das Abonnement für die Verbindung der Ereignisquelle erstellt haben.
    3.  Führen Sie den folgenden Befehl aus, um die Abonnementinformationen abzurufen:

        **wecutil gs** *&lt; subscriptionID &gt;*

    4.  Abrufen des Werts DeliveryMaxItems aus den Abonnementinformationen.

2.  Auslösen Sie auf dem Ereignisquellcomputer die Ereignisse, die mit der Abfrage aus dem Ereignisabonnement übereinstimmen. Die DeliveryMaxItems-Anzahl von Ereignissen muss ausgelöst werden, damit die Ereignisse weitergeleitet werden.
3.  Überprüfen Sie auf dem Ereignissammlercomputer, ob die Ereignisse an das ForwardedEvents-Protokoll oder an das im Abonnement angegebene Protokoll weitergeleitet wurden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren von Computern zum Weiterleiten und Sammeln von Ereignissen](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))
</dt> <dt>

[Einrichten eines von der Quelle initiierten Abonnements](setting-up-a-source-initiated-subscription.md)
</dt> <dt>

[Windows Ereignissammlerreferenz](windows-event-collector-reference.md)
</dt> </dl>

 

 
