---
title: Hinzufügen einer Ereignisquelle zu einem vom Collector initiierten Abonnement
description: Um ein weitergeleitetes Ereignis von einem Ereignisabonnement zu empfangen, können Sie ein vom Collector initiiertes Abonnement auf dem lokalen Computer erstellen.
ms.assetid: f0100938-1702-4ef7-b20e-a0e8df224d18
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905dd9b5a250f9ab12397f851f79a8374c6847235acb34013972dea445f3622b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344211"
---
# <a name="adding-an-event-source-to-a-collector-initiated-subscription"></a>Hinzufügen einer Ereignisquelle zu einem vom Collector initiierten Abonnement

Um ein weitergeleitetes Ereignis von einem Ereignisabonnement zu empfangen, können Sie ein vom Collector initiiertes Abonnement auf dem lokalen Computer erstellen. Weitere Informationen zum Erstellen eines collector-initiierten Abonnements finden Sie im C++-Codebeispiel unter [Erstellen eines Ereignissammlerabonnements.](creating-an-event-collector-subscription.md)

Nachdem ein vom Collector initiiertes Abonnement erstellt wurde, können Sie dem Abonnement Ereignisquellen hinzufügen. Sie müssen einem Abonnement mindestens eine Ereignisquelle hinzufügen, um Ereignisse zu sammeln.

> [!Note]
>
> Sie können dieses Codebeispiel verwenden, um einem Abonnement eine Ereignisquelle hinzuzufügen, oder Sie können den folgenden Befehl an der Eingabeaufforderung eingeben:
>
> **wecutil ss** *SubscriptionName* **/wo:**_EventSourceAddress_ **/aes /ese**
>
> *EventSourceAddress* kann entweder localhost für den lokalen Computer oder ein vollqualifizierter Domänenname für einen Remotecomputer sein.

 

Weitere Informationen zum Hinzufügen von Ereignisquellen zu einem quellinitiiertem Abonnement finden Sie unter [Einrichten eines von der Quelle initiierten Abonnements.](setting-up-a-source-initiated-subscription.md)

Dieses Beispiel folgt einer Reihe von Schritten zum Hinzufügen einer Ereignisquelle zu einem vom Collector initiierten Abonnement.

**So fügen Sie einem collector-initiierten Abonnement eine Ereignisquelle hinzu**

1.  Öffnen Sie das vorhandene Abonnement, indem Sie den Abonnementnamen und die Zugriffsrechte als Parameter für die [**EcOpenSubscription-Funktion**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) bereitstellen. Weitere Informationen zu Zugriffsrechten finden Sie unter [**Windows Event Collector-Konstanten.**](windows-event-collector-constants.md)
2.  Rufen Sie das Ereignisquellenarray des Abonnements ab, indem Sie die [**EcGetSubscriptionProperty-Funktion**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) aufrufen. Weitere Informationen zu Abonnementeigenschaften, die abgerufen werden können, finden Sie in der [**EC \_ SUBSCRIPTION PROPERTY \_ \_ ID-Enumeration.**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id)
3.  Fügen Sie dem Ereignisquellenarray des Abonnements eine neue Ereignisquelle hinzu, indem Sie die [**EcInsertObjectArrayElement-Funktion**](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement) aufrufen.
4.  Legen Sie die Eigenschaften der Ereignisquelle fest, indem Sie die [**EcSetObjectArrayProperty-Funktion**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty) aufrufen. Die **EcSubscriptionEventSourceAddress-Eigenschaft** wird entweder auf eine Adresse für den lokalen Computer (Localhost) oder auf einen vollqualifizierten Domänennamen für einen Remotecomputer festgelegt. Weitere Informationen zu Ereignisquelleneigenschaften, die festgelegt werden können, finden Sie in der **EC \_ SUBSCRIPTION PROPERTY \_ \_ ID-Enumeration.**
5.  Speichern Sie das Abonnement, indem Sie die [**EcSaveSubscription-Funktion**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) aufrufen.
6.  Schließen Sie das Abonnement, indem Sie die [**EcClose-Funktion**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) aufrufen.

Das folgende C++-Codebeispiel zeigt, wie Sie einem vom Collector initiierten Abonnement eine Ereignisquelle hinzufügen:


```C++
#include <windows.h>
#include <iostream>
using namespace std;
#include <EvColl.h>
#include <vector>
#include <string>
#include <strsafe.h>

#pragma comment(lib, "wecapi.lib")

DWORD GetProperty(EC_HANDLE hSubscription,  
                  EC_SUBSCRIPTION_PROPERTY_ID propID, 
                  DWORD flags, 
                  std::vector<BYTE>& buffer, 
                  PEC_VARIANT& vProperty);

void __cdecl wmain()
{
    EC_HANDLE hSubscription;
    std::wstring eventSource = L"localhost"; 
    BOOL status = true;
    std::wstring eventSourceUserName;
    std::wstring eventSourcePassword;
    LPCWSTR lpSubname = L"TestSubscription-CollectorInitiated";
    DWORD dwEventSourceCount;
    DWORD dwRetVal = ERROR_SUCCESS;
    PEC_VARIANT vEventSource = NULL;
    std::vector<BYTE> buffer;
    LPVOID lpwszBuffer;
    EC_VARIANT vProperty;

    // Create a handle to access the event sources array.
    EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray = NULL;

    // Step 1: Open an existing subscription.
    hSubscription = EcOpenSubscription( lpSubname,
        EC_READ_ACCESS | EC_WRITE_ACCESS, 
        EC_OPEN_EXISTING);
    if (!hSubscription)
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 2: Get the event sources array to add a new event 
    // source to the subscription.
    dwRetVal = GetProperty(hSubscription, 
        EcSubscriptionEventSources,
        0,
        buffer,
        vEventSource);
    if (ERROR_SUCCESS != dwRetVal)
    {
        goto Cleanup;
    }

    // Ensure that a handle to the event sources array has been obtained. 
    if (vEventSource->Type != EcVarTypeNull  && 
        vEventSource->Type != EcVarObjectArrayPropertyHandle)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }

    hArray = (vEventSource->Type == EcVarTypeNull)? NULL: 
        vEventSource->PropertyHandleVal;
    if(!hArray)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }
    if (!EcGetObjectArraySize(hArray, &dwEventSourceCount))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 3: Add a new event source to the event source array.
    if (!EcInsertObjectArrayElement(hArray,
        dwEventSourceCount))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 4: Set the properties of the event source
    // Set the EventSourceAddress property that specifies the address
    // of the event forwarding computer, this property can be localhost 
    // or a fully-qualified domain name.
    vProperty.Type = EcVarTypeString;
    vProperty.StringVal = eventSource.c_str();
    if (!EcSetObjectArrayProperty( hArray,
        EcSubscriptionEventSourceAddress,
        dwEventSourceCount,
        0,
        &vProperty))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Get the credentials.
    wcout << "Enter credentials used to connect to the event source " <<
        eventSource << ". " << endl <<
        "Enter user name: " << endl;
    wcin >> eventSourceUserName;
    cout << "Enter password: " << endl;

    wchar_t c;
    while( (c = _getwch()) && c != '\n' && c != '\r' && eventSourcePassword.length() < 512)
    {eventSourcePassword.append(1, c);}

    // Set the EventSourceUserName property that specifies the user
    // that can retrieve events from the event source.
    if (eventSourceUserName.length() > 0)
    {
        vProperty.Type = EcVarTypeString;
        vProperty.StringVal = eventSourceUserName.c_str();
        if (!EcSetObjectArrayProperty(hArray,
            EcSubscriptionEventSourceUserName,
            dwEventSourceCount,
            0,
            &vProperty))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }

        // Set the EventSourcePassword property that defines the password
        // for the previously-defined user.
        vProperty.StringVal = (eventSourcePassword.length() > 0) ? 
            eventSourcePassword.c_str() : L"";
        if (!EcSetObjectArrayProperty(hArray,
            EcSubscriptionEventSourcePassword, 
            dwEventSourceCount,
            0,
            &vProperty))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }
    }

    // When you have finished using the credentials,
    // erase them.
    eventSourceUserName.erase();
    eventSourcePassword.erase();


    // Set the EventSourceEnabled property that enables the event source
    // to forward events.
    vProperty.Type = EcVarTypeBoolean;
    vProperty.BooleanVal = status;
    if (!EcSetObjectArrayProperty(hArray,
        EcSubscriptionEventSourceEnabled,
        dwEventSourceCount,
        0,
        &vProperty))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 5: Save the subscription to enable the event source.
    if (!EcSaveSubscription(hSubscription, NULL))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 6: Close the subscription.
Cleanup:
    if (hArray)
        EcClose(hArray);
    if (hSubscription)
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
            wprintf(L"Failed to FormatMessage.  Operation Error Code: %u\n  Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
            return;
        }
        wprintf(L"\nFailed to Perform Operation. Error Code: %u\n Error Message: %s\n", dwRetVal, lpwszBuffer);
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
        &dwBufferSize))
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
                &dwBufferSize) )
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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren von Computern zum Weiterleiten und Sammeln von Ereignissen](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))
</dt> <dt>

[Erstellen eines Ereignissammlerabonnements](creating-an-event-collector-subscription.md)
</dt> <dt>

[Windows Ereignissammlerreferenz](windows-event-collector-reference.md)
</dt> </dl>

 

 