---
title: Enumerationen (Peerinfrastruktur)
description: Mithilfe von Enumerationen können Sie eine Liste aller spezifischen Peerentitäten abrufen, die Ihren Kriterien entsprechen.
ms.assetid: 81391e4f-aea1-4f5e-a32b-436a3856993b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6514866001734fb0ba0d73c94d5d4d8f8b4cfc6987d121f058a6bfcb00f792c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887630"
---
# <a name="enumerations-peer-infrastructure"></a>Enumerationen (Peerinfrastruktur)

Mithilfe von Enumerationen können Sie eine Liste aller spezifischen Peerentitäten abrufen, die Ihren Kriterien entsprechen.

**So rufen Sie eine Enumeration ab und rufen die Ergebnisse ab**

1.  Abrufen eines Handles für die Enumeration. Rufen Sie **beispielsweise eine PeerEnum-Funktion** auf, und rufen Sie die [**PeerGraphEnumRecords-Peer**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords) graphing-Funktion auf. Die **PeerEnum-Funktionen** erstellen die Enumeration und geben ein Handle für diese Enumeration an die aufrufende Anwendung zurück. Dieses Handle muss verwendet werden, um die Ergebnisse abzurufen.
2.  Optional können Sie die Anzahl der Entitäten in der -Enumeration abrufen. Rufen Sie **eine GetItemCount-Funktion** auf, z. B. [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount) oder [**PeerGetItemCount.**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount)
    > [!Note]  
    > Sie können den von der **GetItemCount-Funktion** zurückgegebenen Wert verwenden, um die Anzahl der abzurufenden Elemente zu bestimmen.

     

3.  Ruft eine Gruppe von Ergebnissen ab. Rufen Sie **eine GetNextItem-Funktion** auf, z. B. [**PeerGraphGetNextItem.**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem)
    > [!Note]  
    > Wenn eine Anwendung eine **GetNextItem-Funktion** aufruft, gibt sie die Anzahl der zurückzahlenden Entitäten an. Anschließend gibt die Funktion einen Zeiger auf ein Array von Zeigern auf die Entitäten und die Anzahl der Entitäten zurück, die immer kleiner oder gleich der angegebenen Zahl ist. Eine Anwendung muss diese Funktion möglicherweise mehrmals aufrufen, bis die Anzahl der zurückgegebenen Entitäten kleiner als die angeforderte Anzahl ist.

     

4.  Wenn die Daten nicht benötigt werden, geben Sie den Zeiger auf die Daten frei. Rufen Sie eine **FreeData-Funktion** auf, z. B. [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) oder [**PeerFreeData.**](/windows/desktop/api/P2P/nf-p2p-peerfreedata)
    > [!Note]  
    > Weitere Informationen finden Sie unter [Freeing Peer Data](freeing-peer-data.md).

     

5.  Nachdem die Anwendung das Handle für die Enumeration nicht benötigt, geben Sie es frei. Rufen Sie **eine EndEnumeration-Funktion** auf, z. B. [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) oder [**PeerGraphEndEnumeration.**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration)

## <a name="example-of-an-enumeration"></a>Beispiel für eine Enumeration

Der folgende Codeausschnitt zeigt, wie Sie verfügbare Identitäten aufzählen.


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



 

 



