---
title: Enumerationen (Peer Infrastruktur)
description: Mithilfe von Enumerationen können Sie eine Liste aller spezifischen Peer Entitäten abrufen, die Ihren Kriterien entsprechen.
ms.assetid: 81391e4f-aea1-4f5e-a32b-436a3856993b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c90a6806c9fdf7b776980abbaaa3f28643c49360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362236"
---
# <a name="enumerations-peer-infrastructure"></a><span data-ttu-id="d058b-103">Enumerationen (Peer Infrastruktur)</span><span class="sxs-lookup"><span data-stu-id="d058b-103">Enumerations (Peer Infrastructure)</span></span>

<span data-ttu-id="d058b-104">Mithilfe von Enumerationen können Sie eine Liste aller spezifischen Peer Entitäten abrufen, die Ihren Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d058b-104">By using Enumerations, you can obtain a list of all the specific peer entities that match your criteria.</span></span>

<span data-ttu-id="d058b-105">**So rufen Sie eine Enumeration ab und rufen die Ergebnisse ab**</span><span class="sxs-lookup"><span data-stu-id="d058b-105">**To obtain an enumeration and retrieve the results**</span></span>

1.  <span data-ttu-id="d058b-106">Abrufen eines Handles für die-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="d058b-106">Obtain a handle to the enumeration.</span></span> <span data-ttu-id="d058b-107">Ruft eine **peerenum** -Funktion auf, z. b. die Peer Graphfunktion [**peergraphenumrecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords) .</span><span class="sxs-lookup"><span data-stu-id="d058b-107">Call a **PeerEnum** function, for example, call the [**PeerGraphEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords) Peer Graphing function.</span></span> <span data-ttu-id="d058b-108">Die **Peer Enumerationsfunktionen** erstellen die-Enumeration und geben ein Handle für diese Enumeration an die aufrufenden Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="d058b-108">The **PeerEnum** functions create the enumeration, and return a handle to that enumeration to the calling application.</span></span> <span data-ttu-id="d058b-109">Dieses Handle muss zum Abrufen der Ergebnisse verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d058b-109">This handle must be used to retrieve the results.</span></span>
2.  <span data-ttu-id="d058b-110">Optional können Sie die Anzahl der Entitäten in der-Enumeration abrufen.</span><span class="sxs-lookup"><span data-stu-id="d058b-110">Optionally, obtain the number of entities in the enumeration.</span></span> <span data-ttu-id="d058b-111">Aufrufen einer **GetItemCount** -Funktion, z. b. Aufrufen von " [**Peer graphgetitemcount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount) " oder " [**Peer-GetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount)".</span><span class="sxs-lookup"><span data-stu-id="d058b-111">Call a **GetItemCount** function, for example, call [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount) or [**PeerGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount).</span></span>
    > [!Note]  
    > <span data-ttu-id="d058b-112">Sie können den von der **GetItemCount** -Funktion zurückgegebenen Wert verwenden, um die Anzahl der abzurufenden Elemente zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="d058b-112">You can use the value returned by the **GetItemCount** function to determine the number of items available to retrieve.</span></span>

     

3.  <span data-ttu-id="d058b-113">Ruft eine Gruppe von Ergebnissen ab.</span><span class="sxs-lookup"><span data-stu-id="d058b-113">Retrieve a group of results.</span></span> <span data-ttu-id="d058b-114">Aufrufen einer **GetNextItem** -Funktion, z. b. Aufrufen von " [**Peer graphgetnextitem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem)".</span><span class="sxs-lookup"><span data-stu-id="d058b-114">Call a **GetNextItem** function, for example, call [**PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem).</span></span>
    > [!Note]  
    > <span data-ttu-id="d058b-115">Wenn eine Anwendung eine **GetNextItem** -Funktion aufruft, gibt Sie die Anzahl der zurück zugebende Entitäten an, und anschließend gibt die Funktion einen Zeiger auf ein Array von Zeigern auf die Entitäten und die Anzahl der Entitäten zurück, die immer kleiner oder gleich der angegebenen Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="d058b-115">When an application calls a **GetNextItem** function, it specifies the number of entities to return, and then the function returns a pointer to an array of pointers to the entities, and the number of entities, which is always less than or equal to the number specified.</span></span> <span data-ttu-id="d058b-116">Eine Anwendung muss diese Funktion möglicherweise mehrmals aufzurufen – bis die Anzahl der zurückgegebenen Entitäten kleiner ist als die angeforderte Anzahl.</span><span class="sxs-lookup"><span data-stu-id="d058b-116">An application might need to call this function many times—until the number of entities returned is less than the number requested.</span></span>

     

4.  <span data-ttu-id="d058b-117">Wenn die Daten nicht benötigt werden, können Sie den Zeiger auf die Daten freigeben.</span><span class="sxs-lookup"><span data-stu-id="d058b-117">After the data is not needed, free the pointer to the data.</span></span> <span data-ttu-id="d058b-118">Greifen Sie auf eine " **fredata** "-Funktion zu, z. b. " [**Peer Diagramm-Daten**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) " oder " [**Peer-fredata**](/windows/desktop/api/P2P/nf-p2p-peerfreedata)"</span><span class="sxs-lookup"><span data-stu-id="d058b-118">Call a **FreeData** function, for example, call [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) or [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).</span></span>
    > [!Note]  
    > <span data-ttu-id="d058b-119">Weitere Informationen finden Sie unter [Freigeben von Peer Daten](freeing-peer-data.md).</span><span class="sxs-lookup"><span data-stu-id="d058b-119">For more information, see [Freeing Peer Data](freeing-peer-data.md).</span></span>

     

5.  <span data-ttu-id="d058b-120">Wenn die Anwendung das Handle für die-Enumeration nicht benötigt, geben Sie Sie frei.</span><span class="sxs-lookup"><span data-stu-id="d058b-120">After the application does not need the handle to the enumeration, release it.</span></span> <span data-ttu-id="d058b-121">Aufrufen einer **EndEnumeration** -Funktion, z. b. Aufrufen von " [**Peer Enumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) " oder " [**Peer graphendenumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration)".</span><span class="sxs-lookup"><span data-stu-id="d058b-121">Call an **EndEnumeration** function, for example, call [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) or [**PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration).</span></span>

## <a name="example-of-an-enumeration"></a><span data-ttu-id="d058b-122">Beispiel für eine Enumeration</span><span class="sxs-lookup"><span data-stu-id="d058b-122">Example of an Enumeration</span></span>

<span data-ttu-id="d058b-123">Der folgende Code Ausschnitt zeigt, wie Sie die verfügbaren Identitäten aufzählen.</span><span class="sxs-lookup"><span data-stu-id="d058b-123">The following code snippet shows you how to enumerate through available identities.</span></span>


```C++
#include <p2p.h>
#include <stdio.h>

#pragma comment(lib, "p2p.lib")

//-----------------------------------------------------------------------------
// Function: EnumIdentities
//
// Purpose:  Demonstrate how to enumerate identities.
//
// Returns:  HRESULT
//

HRESULT EnumIdentities(void)
{
    HPEERENUM hPeerEnum = NULL;
    HRESULT hr = PeerEnumIdentities(&hPeerEnum);

    if (SUCCEEDED(hr))
    {
        ULONG cIdentities = 0;
        hr = PeerGetItemCount(hPeerEnum, &cIdentities);

        if (SUCCEEDED(hr))
        {
            ULONG i;

            for (i = 0; i < cIdentities; i++)
            {
                ULONG cItem = 1; // process one result at a time
                PEER_NAME_PAIR ** ppNamePair = NULL; // pointer to an array of pointers

                hr = PeerGetNextItem(hPeerEnum, &cItem, (PVOID**) &ppNamePair);

                if (SUCCEEDED(hr) && (1 == cItem))
                {
                    wprintf(L"%s [%s]\r\n", (*ppNamePair)->pwzFriendlyName, (*ppNamePair)->pwzPeerName);
                    PeerFreeData(ppNamePair);
                }
            }
        }
        PeerEndEnumeration(hPeerEnum);
    }
 
    return hr;
}
```



 

 



