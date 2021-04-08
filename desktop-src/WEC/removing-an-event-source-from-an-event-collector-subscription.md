---
title: Entfernen einer Ereignis Quelle aus einem vom Collector initiierten Abonnement
description: Sie können eine Ereignis Quelle aus einem vom Collector initiierten Abonnement entfernen, ohne das gesamte Abonnement zu löschen.
ms.assetid: 6c9e0dbf-59a2-4db9-8fb8-0dbfda5cf38b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303e0a708c2b52225af83475674e5f60d1a8418d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856447"
---
# <a name="removing-an-event-source-from-a-collector-initiated-subscription"></a><span data-ttu-id="5660f-103">Entfernen einer Ereignis Quelle aus einem vom Collector initiierten Abonnement</span><span class="sxs-lookup"><span data-stu-id="5660f-103">Removing an Event Source from a Collector Initiated Subscription</span></span>

<span data-ttu-id="5660f-104">Sie können eine Ereignis Quelle aus einem vom Collector initiierten Abonnement entfernen, ohne das gesamte Abonnement zu löschen.</span><span class="sxs-lookup"><span data-stu-id="5660f-104">You can remove an event source from a collector initiated subscription without deleting the entire subscription.</span></span> <span data-ttu-id="5660f-105">Sie müssen die Adresse der Ereignis Quelle kennen, die Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="5660f-105">You must know the address of the event source that you want to delete.</span></span> <span data-ttu-id="5660f-106">Sie können die Adresse einer Ereignis Quelle ermitteln, die einem Abonnement zugeordnet ist, indem Sie das C++-Beispiel [anzeigen, das unter Anzeigen der Eigenschaften eines Ereignis Sammler Abonnements](displaying-the-properties-of-an-event-collector-subscription.md)angezeigt wird, oder Sie können den folgenden Befehl an der Eingabeaufforderung eingeben:</span><span class="sxs-lookup"><span data-stu-id="5660f-106">You can find the address of an event source that is associated to a subscription by using the C++ example shown in [Displaying the Properties of an Event Collector Subscription](displaying-the-properties-of-an-event-collector-subscription.md), or you can type the following command at the command prompt:</span></span>

<span data-ttu-id="5660f-107">" **wecutil GS** " ( *Abonnement Name* )</span><span class="sxs-lookup"><span data-stu-id="5660f-107">**wecutil gs** *SubscriptionName*</span></span>

<span data-ttu-id="5660f-108">Zum Auflisten der aktuellen Abonnements auf einem lokalen Computer können Sie das C++-Codebeispiel in Auflisten von [Event Collector-Abonnements](listing-event-collector-subscriptions.md)verwenden, oder Sie können den folgenden Befehl an der Eingabeaufforderung eingeben:</span><span class="sxs-lookup"><span data-stu-id="5660f-108">To list the current subscriptions on a local computer, you can use the C++ code example shown in [Listing Event Collector Subscriptions](listing-event-collector-subscriptions.md), or you can type the following command at the command prompt:</span></span>

<span data-ttu-id="5660f-109">**wecutil**</span><span class="sxs-lookup"><span data-stu-id="5660f-109">**wecutil es**</span></span>

> [!Note]
>
> <span data-ttu-id="5660f-110">Sie können dieses Beispiel verwenden, um eine Ereignis Quelle aus einem vom Collector initiierten Abonnement zu entfernen, oder Sie können den folgenden Befehl an der Eingabeaufforderung eingeben:</span><span class="sxs-lookup"><span data-stu-id="5660f-110">You can use this example to remove an event source from a collector initiated subscription or you can type the following command at the command prompt:</span></span>
>
> <span data-ttu-id="5660f-111">**wecutil SS** *Abonnement Name*  \* */ESA: \* \* \* eventsourceaddress* **/Res**</span><span class="sxs-lookup"><span data-stu-id="5660f-111">**wecutil ss** *SubscriptionName* \**/esa:\*\*\*EventSourceAddress* **/res**</span></span>
>
> <span data-ttu-id="5660f-112">*Eventsourceaddress* kann entweder "localhost" für den lokalen Computer oder ein voll qualifizierter Domänen Name für einen Remote Computer sein.</span><span class="sxs-lookup"><span data-stu-id="5660f-112">*EventSourceAddress* can be either localhost for the local computer or a fully qualified domain name for a remote computer.</span></span>

 

<span data-ttu-id="5660f-113">In diesem Beispiel wird eine Reihe von Schritten zum Entfernen einer Ereignis Quelle aus einem vom Collector initiierten Abonnement befolgt.</span><span class="sxs-lookup"><span data-stu-id="5660f-113">This example follows a series of steps to remove an event source from a collector-initiated subscription.</span></span>

<span data-ttu-id="5660f-114">**So entfernen Sie eine Ereignis Quelle aus einem vom Collector initiierten Abonnement**</span><span class="sxs-lookup"><span data-stu-id="5660f-114">**To remove an event source from a collector-initiated subscription**</span></span>

1.  <span data-ttu-id="5660f-115">Öffnen Sie das vorhandene Abonnement, indem Sie den Abonnement Namen und die Zugriffsrechte als Parameter für die [**ecopenabonnement**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) -Funktion angeben.</span><span class="sxs-lookup"><span data-stu-id="5660f-115">Open the existing subscription by providing the subscription name and access rights as parameters to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function.</span></span> <span data-ttu-id="5660f-116">Weitere Informationen zu Zugriffsrechten finden Sie unter [**Windows-Ereignis Sammler Konstanten**](windows-event-collector-constants.md).</span><span class="sxs-lookup"><span data-stu-id="5660f-116">For more information about access rights, see [**Windows Event Collector Constants**](windows-event-collector-constants.md).</span></span>
2.  <span data-ttu-id="5660f-117">Rufen Sie das Ereignis Quellen Array des Abonnements ab, indem Sie die [**ecgetabonneptionproperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5660f-117">Get the event sources array of the subscription by calling the [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) function.</span></span> <span data-ttu-id="5660f-118">Weitere Informationen zu Abonnement Eigenschaften, die abgerufen werden können, finden Sie unter der [**\_ \_ Eigenschaft \_ ID**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) -Enumeration für das EC-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5660f-118">For more information about subscription properties that can be retrieved, see the [**EC\_SUBSCRIPTION\_PROPERTY\_ID**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id) enumeration.</span></span>
3.  <span data-ttu-id="5660f-119">Suchen Sie die angegebene Ereignis Quelle im Ereignis Quellen Array des Abonnements, indem Sie die [**ecgetobjectarrayproperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarrayproperty) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5660f-119">Search for the specified event source in the event sources array of the subscription by calling the [**EcGetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarrayproperty) function.</span></span> <span data-ttu-id="5660f-120">Der Wert der **ecabonneptioneventsourceaddress** -Eigenschaft ist entweder "localhost" für den lokalen Computer oder ein voll qualifizierter Domänen Name für einen Remote Computer.</span><span class="sxs-lookup"><span data-stu-id="5660f-120">The value of the **EcSubscriptionEventSourceAddress** property will be either Localhost for the local computer or will be a fully qualified domain name for a remote computer.</span></span> <span data-ttu-id="5660f-121">Weitere Informationen zu Ereignis Quellen Eigenschaften, die abgerufen werden können, finden Sie unter der **\_ \_ Eigenschaft \_ ID** -Enumeration für das EC-Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5660f-121">For more information about event source properties that can be retrieved, see the **EC\_SUBSCRIPTION\_PROPERTY\_ID** enumeration.</span></span>
4.  <span data-ttu-id="5660f-122">Löschen Sie die Ereignis Quelle aus dem Abonnement, indem Sie die [**ecremoveobjectarrayelement**](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5660f-122">Delete the event source from the subscription by calling the [**EcRemoveObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement) function.</span></span>
5.  <span data-ttu-id="5660f-123">Speichern Sie das Abonnement, indem Sie die [**ecsavesub-**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5660f-123">Save the subscription by calling the [**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription) function.</span></span>
6.  <span data-ttu-id="5660f-124">Schließen Sie das Abonnement, indem Sie die [**ecclose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5660f-124">Close the subscription by calling the [**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose) function.</span></span>

<span data-ttu-id="5660f-125">Im folgenden C++-Codebeispiel wird gezeigt, wie eine Ereignis Quelle aus einem Ereignis Sammler Abonnement entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="5660f-125">The following C++ code example shows how to remove an event source from an Event Collector subscription.</span></span>


```C++
#include <windows.h>
#include <EvColl.h>
#include <vector>
#include <string>
#include <strsafe.h>
#pragma comment(lib, "wecapi.lib")


// Subscription Information
DWORD GetSubscriptionProperty(EC_HANDLE hSubscription,  
    EC_SUBSCRIPTION_PROPERTY_ID propID, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vProperty);
DWORD GetEventSourceProperty(EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray, 
    EC_SUBSCRIPTION_PROPERTY_ID propID, 
    DWORD arrayIndex, 
    DWORD flags, 
    std::vector<BYTE>& buffer, 
    PEC_VARIANT& vProper);



void __cdecl wmain()
{
    EC_HANDLE hSubscription;
    std::wstring eventSource = L"localhost";
    BOOL foundEventSource = false;
    LPCWSTR lpSubname = L"TestSubscription-CollectorInitiated";
    DWORD dwEventSourceCount;
    DWORD deleteEvent = 0; 
    DWORD dwRetVal = ERROR_SUCCESS;
    PEC_VARIANT vProperty = NULL;
    std::vector<BYTE> buffer;
    LPVOID lpwszBuffer;
    EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray = NULL;

    // Step 1: Open an existing subscription.
    hSubscription = EcOpenSubscription(lpSubname,
        EC_READ_ACCESS | EC_WRITE_ACCESS,
        EC_OPEN_EXISTING);

    if (!hSubscription)
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 2: Get the event sources array to remove an event 
    // source from the subscription.
    dwRetVal = GetSubscriptionProperty(hSubscription, 
        EcSubscriptionEventSources,
        0,
        buffer,
        vProperty);
    if (ERROR_SUCCESS != dwRetVal)
    {
        goto Cleanup;
    }

    // Ensure that a handle to the event sources array has been obtained.
    if (vProperty->Type != EcVarTypeNull  && 
        vProperty->Type != EcVarObjectArrayPropertyHandle)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }

    hArray = (vProperty->Type == EcVarTypeNull)? NULL: 
        vProperty->PropertyHandleVal;
    if (!hArray)
    {
        dwRetVal = ERROR_INVALID_DATA;
        goto Cleanup;
    }

    if (!EcGetObjectArraySize(hArray, &dwEventSourceCount))
    {
        dwRetVal = GetLastError();
        goto Cleanup;
    }

    // Step 3: Search for the specified event source in the event source array.
    for (DWORD I = 0; I < dwEventSourceCount; I++)
    {
        dwRetVal = GetEventSourceProperty(hArray, 
            EcSubscriptionEventSourceAddress, 
            I,
            0,
            buffer,
            vProperty);
        if (ERROR_SUCCESS != dwRetVal)
        {
            goto Cleanup;
        }

        if (vProperty->StringVal == eventSource)
        {
            foundEventSource = true;
            deleteEvent = I;
            break;
        }
    }

    // Step 4: If the event source was found in the array, remove it.
    if (foundEventSource)
    {
        if (!EcRemoveObjectArrayElement(hArray, deleteEvent))
        {
            dwRetVal = GetLastError();
            goto Cleanup;
        }
    }
    else
    {
        wprintf(L"Could not remove the event source from the subscription.\n");
        goto Cleanup;
    }

    // Step 5: Save the subscription to finalize the removal of the event source.
    if( !EcSaveSubscription(hSubscription, NULL) )
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
                wprintf(L"Failed to FormatMessage.  Operation Error Code: %u." \
                    L"Error Code from FormatMessage: %u\n", dwRetVal, GetLastError());
                return;
            }

            wprintf(L"\nFailed to Perform Operation.\nError Code: %u\n" \
                L"Error Message: %s\n", dwRetVal, lpwszBuffer);

            LocalFree(lpwszBuffer);
        }
}

DWORD GetSubscriptionProperty(EC_HANDLE hSubscription, 
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

DWORD GetEventSourceProperty(EC_OBJECT_ARRAY_PROPERTY_HANDLE hArray, 
    EC_SUBSCRIPTION_PROPERTY_ID propID,
    DWORD arrayIndex,
    DWORD flags,
    std::vector<BYTE>& buffer,
    PEC_VARIANT& vProperty)
{
    UNREFERENCED_PARAMETER(flags);
    UNREFERENCED_PARAMETER(propID);
    
    DWORD  dwBufferSize, dwRetVal = ERROR_SUCCESS;
    buffer.resize(sizeof(EC_VARIANT));

    if (!hArray)
        return ERROR_INVALID_PARAMETER;

    // Obtain the value for the specified property. 
    if (!EcGetObjectArrayProperty(hArray,
        EcSubscriptionEventSourceAddress, 
        arrayIndex,
        0, 
        (DWORD) buffer.size(), 
        (PEC_VARIANT)&buffer[0],
        &dwBufferSize))
    {
        dwRetVal = GetLastError();

        if (ERROR_INSUFFICIENT_BUFFER == dwRetVal)
        {
            dwRetVal = ERROR_SUCCESS;
            buffer.resize(dwBufferSize);

            if (!EcGetObjectArrayProperty(hArray,
                EcSubscriptionEventSourceAddress,
                arrayIndex,
                0, 
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



## <a name="related-topics"></a><span data-ttu-id="5660f-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5660f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5660f-127">Anzeigen der Eigenschaften eines Ereignis Sammler Abonnements</span><span class="sxs-lookup"><span data-stu-id="5660f-127">Displaying the Properties of an Event Collector Subscription</span></span>](displaying-the-properties-of-an-event-collector-subscription.md)
</dt> <dt>

[<span data-ttu-id="5660f-128">Auflisten von Event Collector-Abonnements</span><span class="sxs-lookup"><span data-stu-id="5660f-128">Listing Event Collector Subscriptions</span></span>](listing-event-collector-subscriptions.md)
</dt> <dt>

[<span data-ttu-id="5660f-129">Referenz zur Windows-Ereignis Sammlung</span><span class="sxs-lookup"><span data-stu-id="5660f-129">Windows Event Collector Reference</span></span>](windows-event-collector-reference.md)
</dt> </dl>

 

 




