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
# <a name="adding-an-event-source-to-a-collector-initiated-subscription"></a><span data-ttu-id="45974-103">Hinzufügen einer Ereignis Quelle zu einem vom Collector initiierten Abonnement</span><span class="sxs-lookup"><span data-stu-id="45974-103">Adding an Event Source to a Collector Initiated Subscription</span></span>

<span data-ttu-id="45974-104">Um ein weiter geleiteter Ereignis von einem Ereignis Abonnement zu empfangen, können Sie ein vom Collector initiiertes Abonnement auf dem lokalen Computer erstellen.</span><span class="sxs-lookup"><span data-stu-id="45974-104">To receive a forwarded event from an event subscription, you can create a collector-initiated subscription on the local computer.</span></span> <span data-ttu-id="45974-105">Weitere Informationen zum Erstellen eines vom Collector initiierten Abonnements finden Sie im C++-Codebeispiel unter [Erstellen eines Event Collector-Abonnements](creating-an-event-collector-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="45974-105">For more information about how to create a collector initiated subscription, see the C++ code example shown in [Creating an Event Collector Subscription](creating-an-event-collector-subscription.md).</span></span>

<span data-ttu-id="45974-106">Nachdem ein vom Collector initiiertes Abonnement erstellt wurde, können Sie dem Abonnement Ereignis Quellen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="45974-106">After a collector-initiated subscription has been created, you can add event sources to the subscription.</span></span> <span data-ttu-id="45974-107">Sie müssen einem Abonnement mindestens eine Ereignis Quelle hinzufügen, um Ereignisse zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="45974-107">You must add at least one event source to a subscription to collect events.</span></span>

> [!Note]
>
> <span data-ttu-id="45974-108">Sie können dieses Codebeispiel verwenden, um einem Abonnement eine Ereignis Quelle hinzuzufügen, oder Sie können den folgenden Befehl an der Eingabeaufforderung eingeben:</span><span class="sxs-lookup"><span data-stu-id="45974-108">You can use this code example to add an event source to a subscription or you can type the following command at the command prompt:</span></span>
>
> <span data-ttu-id="45974-109">**wecutil SS** *Abonnement Name*  \* */ESA: \* \* \* eventsourceaddress* **/AES/ESE**</span><span class="sxs-lookup"><span data-stu-id="45974-109">**wecutil ss** *SubscriptionName* \**/esa:\*\*\*EventSourceAddress* **/aes /ese**</span></span>
>
> <span data-ttu-id="45974-110">*Eventsourceaddress* kann entweder "localhost" für den lokalen Computer oder ein voll qualifizierter Domänen Name für einen Remote Computer sein.</span><span class="sxs-lookup"><span data-stu-id="45974-110">*EventSourceAddress* can be either localhost for the local computer or a fully qualified domain name for a remote computer.</span></span>

 

<span data-ttu-id="45974-111">Weitere Informationen zum Hinzufügen von Ereignis Quellen zu einem von der Quelle initiierten Abonnement finden Sie unter [Einrichten eines von der Quelle initiierten Abonnements](setting-up-a-source-initiated-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="45974-111">For more information about how to add event sources to a source initiated subscription, see [Setting up a Source Initiated Subscription](setting-up-a-source-initiated-subscription.md).</span></span>

<span data-ttu-id="45974-112">In diesem Beispiel wird eine Reihe von Schritten zum Hinzufügen einer Ereignis Quelle zu einem vom Collector initiierten Abonnement befolgt.</span><span class="sxs-lookup"><span data-stu-id="45974-112">This example follows a series of steps to add an event source to a collector initiated subscription.</span></span>

<span data-ttu-id="45974-113">**So fügen Sie einem vom Collector initiierten Abonnement eine Ereignis Quelle hinzu**</span><span class="sxs-lookup"><span data-stu-id="45974-113">**To add an event source to a collector initiated subscription**</span></span>

1.  <span data-ttu-id="45974-114">Öffnen Sie das vorhandene Abonnement, indem Sie den Abonnement Namen und die Zugriffsrechte als Parameter für die [**ecopenabonnement**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) -Funktion angeben.</span><span class="sxs-lookup"><span data-stu-id="45974-114">Open the existing subscription by providing the subscription name and access rights as parameters to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function.</span></span> <span data-ttu-id="45974-115">Weitere Informationen zu Zugriffsrechten finden Sie unter [**Windows-Ereignis Sammler Konstanten**](windows-event-collector-constants.md).</span><span class="sxs-lookup"><span data-stu-id="45974-115">For more information about access rights, see [**Windows Event Collector Constants**](windows-event-collector-constants.md).</span></span>
2.  <span data-ttu-id="45974-116">Rufen Sie das Ereignis Quellen Array des Abonnements ab, indem Sie die [**ecgetabonneptionproperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="45974-116">Get the event sources array of the subscription by calling the [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) function.</span></span> <span data-ttu-id="45974-117">Weitere Informationen zu Abonnement Eigenschaften, die abgerufen werden können, finden Sie unter der [**\_ \_ Eigenschaft \_ ID**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) -Enumeration für das EC-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="45974-117">For more information about subscription properties that can be retrieved, see the [**EC\_SUBSCRIPTION\_PROPERTY\_ID**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) enumeration.</span></span>
3.  <span data-ttu-id="45974-118">Fügen Sie dem Ereignis Quellen Array des Abonnements eine neue Ereignis Quelle hinzu, indem Sie die [**ecinsertobjectarrayelement**](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="45974-118">Add a new event source to the event sources array of the subscription by calling the [**EcInsertObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement) function.</span></span>
4.  <span data-ttu-id="45974-119">Legen Sie die Eigenschaften der Ereignis Quelle fest, indem Sie die [**ecsetobjectarrayproperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="45974-119">Set the event source properties by calling the [**EcSetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty) function.</span></span> <span data-ttu-id="45974-120">Die **ecabonneptioneventsourceaddress** -Eigenschaft ist entweder auf eine Adresse für den lokalen Computer (localhost) oder auf einen voll qualifizierten Domänen Namen für einen Remote Computer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="45974-120">The **EcSubscriptionEventSourceAddress** property is either set to an address for the local computer (Localhost) or to a fully qualified domain name for a remote computer.</span></span> <span data-ttu-id="45974-121">Weitere Informationen zu den Eigenschaften der Ereignis Quelle, die festgelegt werden können, finden Sie unter der **\_ \_ Eigenschaft \_ ID** -Enumeration des EC-Abonnements.</span><span class="sxs-lookup"><span data-stu-id="45974-121">For more information about event source properties that can be set, see the **EC\_SUBSCRIPTION\_PROPERTY\_ID** enumeration.</span></span>
5.  <span data-ttu-id="45974-122">Speichern Sie das Abonnement, indem Sie die [**ecsavesub-**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="45974-122">Save the subscription by calling the [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) function.</span></span>
6.  <span data-ttu-id="45974-123">Schließen Sie das Abonnement, indem Sie die [**ecclose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="45974-123">Close the subscription by calling the [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) function.</span></span>

<span data-ttu-id="45974-124">Im folgenden C++-Codebeispiel wird gezeigt, wie einem vom Collector initiierten Abonnement eine Ereignis Quelle hinzugefügt wird:</span><span class="sxs-lookup"><span data-stu-id="45974-124">The following C++ code example shows how to add an event source to a collector initiated subscription:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="45974-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="45974-125">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="45974-126">[Konfigurieren von Computern zum Weiterleiten und Sammeln von Ereignissen](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="45974-126">[Configure Computers to Forward and Collect Events](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))</span></span>
</dt> <dt>

[<span data-ttu-id="45974-127">Erstellen eines Event Collector-Abonnements</span><span class="sxs-lookup"><span data-stu-id="45974-127">Creating an Event Collector Subscription</span></span>](creating-an-event-collector-subscription.md)
</dt> <dt>

[<span data-ttu-id="45974-128">Referenz zur Windows-Ereignis Sammlung</span><span class="sxs-lookup"><span data-stu-id="45974-128">Windows Event Collector Reference</span></span>](windows-event-collector-reference.md)
</dt> </dl>

 

 