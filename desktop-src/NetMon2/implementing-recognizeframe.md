---
description: Netzwerkmonitore rufen die RecognizeFrame-Funktion eines Parsers auf, um zu bestimmen, ob der Parser die nicht beanspruchten Daten eines Frames erkennt.
ms.assetid: 6d0574da-f0ec-4ed9-bfb0-023dff2ac6fe
title: Implementieren von RecognizeFrame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d3f9a79325c0c75a7a83cfb99a34ff3de1f073573dee13d39a846b575f6285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890495"
---
# <a name="implementing-recognizeframe"></a>Implementieren von RecognizeFrame

Netzwerkmonitore rufen die [**RecognizeFrame-Funktion**](recognizeframe.md) eines Parsers auf, um zu bestimmen, ob der Parser die nicht beanspruchten Daten eines Frames erkennt. Die nicht beanspruchten Daten können sich am Anfang eines Frames befinden, aber in der Regel befinden sich nicht beanspruchte Daten in der Mitte eines Frames. Die folgende Abbildung zeigt nicht beanspruchte Daten, die sich in der Mitte eines Frames befinden.

![Nicht beanspruchte Daten, die sich in der Mitte eines Frames befinden](images/recognizeframe1.png)

Netzwerkmonitor stellt beim Aufrufen der [**RecognizeFrame-Funktion**](recognizeframe.md) die folgenden Informationen bereit:

-   Ein Handle für den Frame.
-   Ein Zeiger auf den Anfang des Frames.
-   Ein Zeiger auf den Anfang der nicht beanspruchten Daten.
-   Der MAC-Wert des ersten Protokolls im Frame.
-   Die Anzahl der Bytes in den nicht beanspruchten Daten. Das heißt, die im Frame verbleibenden Bytes.
-   Ein Handle für das vorherige Protokoll.
-   Der Offset des vorherigen Protokolls.

Wenn die Parser-DLL ermittelt, dass nicht beanspruchte Daten mit dem Parserprotokoll beginnen, bestimmt die Parser-DLL, wo das nächste Protokoll beginnt und welches Protokoll folgt. Die Parser-DLL funktioniert auf folgende bedingte Weise:

-   Wenn die Parser-DLL nicht beanspruchte Daten erkennt, legt die Parser-DLL den *pProtocolStatus-Parameter* fest und gibt einen Zeiger auf das nächste Protokoll im Frame oder **NULL** zurück. **NULL** wird zurückgegeben, wenn das aktuelle Protokoll das letzte Protokoll im Frame ist.
-   Wenn die Parser-DLL nicht beanspruchte Daten erkennt und das folgende Protokoll identifiziert (anhand der im Protokoll bereitgestellten Informationen), gibt die Parser-DLL einen Zeiger auf das Handle des nächsten Protokolls im *phNextProtocol-Parameter* der Funktion zurück.
-   Wenn die Parser-DLL nicht beanspruchte Daten nicht erkennt, gibt die Parser-DLL den Zeiger auf den Anfang der nicht beanspruchten Daten zurück, und Netzwerkmonitor versucht weiterhin, die nicht beanspruchten Daten zu analysieren.

**So implementieren Sie RecognizeFrame**

1.  Testen Sie, um zu ermitteln, ob Sie das Protokoll erkennen.
2.  Wenn Sie nicht beanspruchte Daten erkennen und wissen, welches Protokoll folgt, legen Sie *pProtocolStatus* auf PROTOCOL \_ STATUS NEXT PROTOCOL \_ \_ fest, legen Sie *phNextProtocol* auf einen Zeiger fest, der auf das Handle für das nächste Protokoll zeigt, und geben Sie dann einen Zeiger auf das nächste Protokoll zurück.

    – oder –

    Wenn Sie nicht beanspruchte Daten erkennen und nicht wissen, welches Protokoll folgt, legen Sie *pProtocolStatus* auf PROTOCOL STATUS RECOGNIZED fest, und geben Sie \_ dann einen Zeiger auf das nächste Protokoll \_ zurück.

    – oder –

    Wenn Sie nicht beanspruchte Daten erkennen und Ihr Protokoll das letzte Protokoll in einem Frame ist, legen Sie *pProtocolStatus* auf PROTOCOL STATUS CLAIMED fest, und geben Sie \_ dann \_ **NULL** zurück.

    – oder –

    Wenn Sie nicht beanspruchte Daten nicht erkennen, legen Sie *pProtocolStatus* auf PROTOCOL \_ STATUS NOT RECOGNIZED \_ \_ fest, und geben Sie dann den Zeiger zurück, der in *pProtocol* an Sie übergeben wird.

Im Folgenden sehen Sie eine grundlegende Implementierung von [**RecognizeFrame**](recognizeframe.md).

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

 

 



