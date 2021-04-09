---
title: Hinzufügen einer Ereignis Quelle zu einem vom Collector initiierten Abonnement
description: Um ein weiter geleiteter Ereignis von einem Ereignis Abonnement zu empfangen, können Sie ein vom Collector initiiertes Abonnement auf dem lokalen Computer erstellen.
ms.assetid: f0100938-1702-4ef7-b20e-a0e8df224d18
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c639b496a00f56a38a0f9f8e72b9d099e58c17
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039139"
---
# <a name="adding-an-event-source-to-a-collector-initiated-subscription"></a>Hinzufügen einer Ereignis Quelle zu einem vom Collector initiierten Abonnement

Um ein weiter geleiteter Ereignis von einem Ereignis Abonnement zu empfangen, können Sie ein vom Collector initiiertes Abonnement auf dem lokalen Computer erstellen. Weitere Informationen zum Erstellen eines vom Collector initiierten Abonnements finden Sie im C++-Codebeispiel unter [Erstellen eines Event Collector-Abonnements](creating-an-event-collector-subscription.md).

Nachdem ein vom Collector initiiertes Abonnement erstellt wurde, können Sie dem Abonnement Ereignis Quellen hinzufügen. Sie müssen einem Abonnement mindestens eine Ereignis Quelle hinzufügen, um Ereignisse zu erfassen.

> [!Note]
>
> Sie können dieses Codebeispiel verwenden, um einem Abonnement eine Ereignis Quelle hinzuzufügen, oder Sie können den folgenden Befehl an der Eingabeaufforderung eingeben:
>
> **wecutil SS** *Abonnement Name*  * */ESA: * * * eventsourceaddress* **/AES/ESE**
>
> *Eventsourceaddress* kann entweder "localhost" für den lokalen Computer oder ein voll qualifizierter Domänen Name für einen Remote Computer sein.

 

Weitere Informationen zum Hinzufügen von Ereignis Quellen zu einem von der Quelle initiierten Abonnement finden Sie unter [Einrichten eines von der Quelle initiierten Abonnements](setting-up-a-source-initiated-subscription.md).

In diesem Beispiel wird eine Reihe von Schritten zum Hinzufügen einer Ereignis Quelle zu einem vom Collector initiierten Abonnement befolgt.

**So fügen Sie einem vom Collector initiierten Abonnement eine Ereignis Quelle hinzu**

1.  Öffnen Sie das vorhandene Abonnement, indem Sie den Abonnement Namen und die Zugriffsrechte als Parameter für die [**ecopenabonnement**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) -Funktion angeben. Weitere Informationen zu Zugriffsrechten finden Sie unter [**Windows-Ereignis Sammler Konstanten**](windows-event-collector-constants.md).
2.  Rufen Sie das Ereignis Quellen Array des Abonnements ab, indem Sie die [**ecgetabonneptionproperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) -Funktion aufrufen. Weitere Informationen zu Abonnement Eigenschaften, die abgerufen werden können, finden Sie unter der [**\_ \_ Eigenschaft \_ ID**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) -Enumeration für das EC-Abonnement.
3.  Fügen Sie dem Ereignis Quellen Array des Abonnements eine neue Ereignis Quelle hinzu, indem Sie die [**ecinsertobjectarrayelement**](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement) -Funktion aufrufen.
4.  Legen Sie die Eigenschaften der Ereignis Quelle fest, indem Sie die [**ecsetobjectarrayproperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty) -Funktion aufrufen. Die **ecabonneptioneventsourceaddress** -Eigenschaft ist entweder auf eine Adresse für den lokalen Computer (localhost) oder auf einen voll qualifizierten Domänen Namen für einen Remote Computer festgelegt. Weitere Informationen zu den Eigenschaften der Ereignis Quelle, die festgelegt werden können, finden Sie unter der **\_ \_ Eigenschaft \_ ID** -Enumeration des EC-Abonnements.
5.  Speichern Sie das Abonnement, indem Sie die [**ecsavesub-**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) Funktion aufrufen.
6.  Schließen Sie das Abonnement, indem Sie die [**ecclose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) -Funktion aufrufen.

Im folgenden C++-Codebeispiel wird gezeigt, wie einem vom Collector initiierten Abonnement eine Ereignis Quelle hinzugefügt wird:


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

[Erstellen eines Event Collector-Abonnements](creating-an-event-collector-subscription.md)
</dt> <dt>

[Referenz zur Windows-Ereignis Sammlung](windows-event-collector-reference.md)
</dt> </dl>

 

 