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
# <a name="enumerations-peer-infrastructure"></a>Enumerationen (Peer Infrastruktur)

Mithilfe von Enumerationen können Sie eine Liste aller spezifischen Peer Entitäten abrufen, die Ihren Kriterien entsprechen.

**So rufen Sie eine Enumeration ab und rufen die Ergebnisse ab**

1.  Abrufen eines Handles für die-Enumeration. Ruft eine **peerenum** -Funktion auf, z. b. die Peer Graphfunktion [**peergraphenumrecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords) . Die **Peer Enumerationsfunktionen** erstellen die-Enumeration und geben ein Handle für diese Enumeration an die aufrufenden Anwendung zurück. Dieses Handle muss zum Abrufen der Ergebnisse verwendet werden.
2.  Optional können Sie die Anzahl der Entitäten in der-Enumeration abrufen. Aufrufen einer **GetItemCount** -Funktion, z. b. Aufrufen von " [**Peer graphgetitemcount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount) " oder " [**Peer-GetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount)".
    > [!Note]  
    > Sie können den von der **GetItemCount** -Funktion zurückgegebenen Wert verwenden, um die Anzahl der abzurufenden Elemente zu bestimmen.

     

3.  Ruft eine Gruppe von Ergebnissen ab. Aufrufen einer **GetNextItem** -Funktion, z. b. Aufrufen von " [**Peer graphgetnextitem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem)".
    > [!Note]  
    > Wenn eine Anwendung eine **GetNextItem** -Funktion aufruft, gibt Sie die Anzahl der zurück zugebende Entitäten an, und anschließend gibt die Funktion einen Zeiger auf ein Array von Zeigern auf die Entitäten und die Anzahl der Entitäten zurück, die immer kleiner oder gleich der angegebenen Zahl ist. Eine Anwendung muss diese Funktion möglicherweise mehrmals aufzurufen – bis die Anzahl der zurückgegebenen Entitäten kleiner ist als die angeforderte Anzahl.

     

4.  Wenn die Daten nicht benötigt werden, können Sie den Zeiger auf die Daten freigeben. Greifen Sie auf eine " **fredata** "-Funktion zu, z. b. " [**Peer Diagramm-Daten**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) " oder " [**Peer-fredata**](/windows/desktop/api/P2P/nf-p2p-peerfreedata)"
    > [!Note]  
    > Weitere Informationen finden Sie unter [Freigeben von Peer Daten](freeing-peer-data.md).

     

5.  Wenn die Anwendung das Handle für die-Enumeration nicht benötigt, geben Sie Sie frei. Aufrufen einer **EndEnumeration** -Funktion, z. b. Aufrufen von " [**Peer Enumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) " oder " [**Peer graphendenumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration)".

## <a name="example-of-an-enumeration"></a>Beispiel für eine Enumeration

Der folgende Code Ausschnitt zeigt, wie Sie die verfügbaren Identitäten aufzählen.


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



 

 



