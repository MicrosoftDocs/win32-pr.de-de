---
description: Netzwerk Monitore rufen die erkenzeframe-Funktion eines Parsers auf, um zu bestimmen, ob der Parser die nicht beanspruchten Daten eines Frames erkennt.
ms.assetid: 6d0574da-f0ec-4ed9-bfb0-023dff2ac6fe
title: Implementieren von "erkenzeframe"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d970eee80a04168b3fa06b117c2c219c506da7ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348948"
---
# <a name="implementing-recognizeframe"></a>Implementieren von "erkenzeframe"

Netzwerk Monitore rufen die [**erkenzeframe**](recognizeframe.md) -Funktion eines Parsers auf, um zu bestimmen, ob der Parser die nicht beanspruchten Daten eines Frames erkennt. Die nicht beanspruchten Daten können sich am Anfang eines Frames befinden, aber in der Regel befinden sich nicht beanspruchte Daten in der Mitte eines Frames. Die folgende Abbildung zeigt nicht beanspruchte Daten, die sich in der Mitte eines Frames befinden.

![nicht beanspruchte Daten, die sich in der Mitte eines Frames befinden](images/recognizeframe1.png)

Netzwerkmonitor stellt beim Aufrufen der Funktion " [**erkenzeframe**](recognizeframe.md) " die folgenden Informationen bereit:

-   Ein Handle für den Frame.
-   Ein Zeiger auf den Anfang des Frames.
-   Ein Zeiger auf den Anfang der nicht beanspruchten Daten.
-   Der Mac-Wert des ersten Protokolls im Frame.
-   Die Anzahl der Bytes in den nicht beanspruchten Daten; Das heißt, die Bytes verbleiben im Frame.
-   Ein Handle für das vorherige Protokoll.
-   Der Offset des vorherigen Protokolls.

Wenn die Parser-DLL ermittelt, dass nicht beanspruchte Daten mit dem parserprotokoll beginnen, bestimmt die Parser-DLL, wo das nächste Protokoll beginnt und welches Protokoll folgt. Die Parser-DLL funktioniert wie folgt:

-   Wenn die Parser-DLL nicht beanspruchte Daten erkennt, legt die Parser-DLL den *pprotocolstatus* -Parameter fest und gibt einen Zeiger auf das nächste Protokoll im Frame oder auf **null** zurück. **Null** wird zurückgegeben, wenn das aktuelle Protokoll das letzte Protokoll im Frame ist.
-   Wenn die Parser-DLL nicht beanspruchte Daten erkennt und das folgende Protokoll identifiziert (aus den im Protokoll bereitgestellten Informationen), gibt die Parser-DLL einen Zeiger auf das Handle des nächsten Protokolls im Parameter *phnextprotocol* der Funktion zurück.
-   Wenn die Parser-DLL keine nicht beanspruchten Daten erkennt, gibt die Parser-DLL den Zeiger auf den Anfang der nicht beanspruchten Daten zurück, und Netzwerkmonitor versucht weiterhin, die nicht beanspruchten Daten zu analysieren.

**So implementieren Sie "erkenzeframe"**

1.  Testen Sie, um zu ermitteln, dass Sie das Protokoll erkennen.
2.  Wenn Sie nicht beanspruchte Daten erkennen und wissen, welches Protokoll befolgt wird, legen Sie *pprotocolstatus* auf Protokoll \_ Status \_ Next \_ Protocol fest, legen Sie *phnextprotocol* auf einen Zeiger fest, der auf das Handle für das nächste Protokoll verweist, und geben Sie dann einen Zeiger auf das nächste Protokoll zurück.

    – oder –

    Wenn Sie nicht beanspruchte Daten erkennen und nicht wissen, welches Protokoll befolgt wird, legen Sie *pprotocolstatus* auf Protokoll \_ Status erkannt fest \_ , und geben Sie dann einen Zeiger auf das nächste Protokoll zurück.

    – oder –

    Wenn Sie nicht beanspruchte Daten erkennen und Ihr Protokoll das letzte Protokoll in einem Frame ist, legen Sie *pprotocolstatus* auf "Protokoll \_ Status beansprucht" fest \_ , und geben Sie dann **null** zurück.

    – oder –

    Wenn Sie keine nicht beanspruchten Daten erkennen, legen Sie *pprotocolstatus* auf "Protokoll \_ Status \_ nicht erkannt" fest \_ , und geben Sie dann den Zeiger zurück, der in " *pprotocol*" an Sie übergeben wird.

Im folgenden finden Sie eine grundlegende Implementierung von [**erkenzeframe**](recognizeframe.md).

``` syntax
#include <windows.h>

LPBYTE BHAPI MyProtocol_RecognizeFrame( HFRAME hFrame,
                                        LPBYTE        pMacFrame,
                                        LPBYTE        pProtocol,
                                        DWORD         MacType,
                                        DWORD         BytesLeft,
                                        HPROTOCOL     hPrevProtocol,
                                        DWORD         nPreviuosProtOffset,
                                        LPDWORD       pProtocolStatus,
                                        LPHPROTOCOL   phNextProtocol,
                                        LPDWORD       InstData)
  
  // Test unclaimed data. 
  
  // If unclaimed data is recognized, but you do not know what follows.
  *pProtocolStatus =  PROTOCOL_STATUS_RECOGNIZED;
  return pProtocol + MY_PROTOCOL_LENGTH;
  
  // If unclaimed data is recognized and you know what follows.
  *pProtocolStatus =  PROTOCOL_STATUS_NEXT_PROTOCOL;
  phNextProtocol = GetProtocolFromTable(
                                        hTable,
                                        ItemToFind,
                                        lpInstData);
  return  pProtocol + MY_PROTOCOL_LENGTH;
  
  // If unclaimed data is recognized and the protocol is the last 
  // protocol in the frame.
  *pProtocolStatus =  PROTOCOL_STATUS_CLAIMED;
  return NULL;
  
  // If the unclaimed data is not recognized.
  *pProtocolStatus =  PROTOCOL_STATUS_NOT_RECOGNIZED;
  return *pProtocol;

}
```

 

 



