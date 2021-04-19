---
description: Ruft die attachproperties-Funktion auf, um die Eigenschaften zuzuordnen, die in einem erkannten Datenobjekt vorhanden sind.
ms.assetid: f1949904-ceb2-4650-847f-01f597ff3620
title: Implementieren von attachproperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9cc032826a8749630c4951b46d456ca807fd37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350511"
---
# <a name="implementing-attachproperties"></a>Implementieren von attachproperties

Netzwerkmonitor Ruft die [**attachproperties**](attachproperties.md) -Funktion auf, um die Eigenschaften zuzuordnen, die in einem erkannten Datenobjekt vorhanden sind. Die [**attachproperties**](attachproperties.md) -Funktion ordnet die Eigenschaften einem bestimmten Speicherort zu.

Netzwerkmonitor verwendet den folgenden Prozess, um die Daten in einem Frame zu analysieren.

-   Zuerst ruft Netzwerkmonitor [erkenzeframe](recognizeframe.md) auf, um alle Protokolle zu erkennen, die in einem Frame vorhanden sind.
-   Dann ruft Netzwerkmonitor [**attachproperties**](attachproperties.md) für jeden Parser auf, der ein Datenelement erkennt.

Wenn Netzwerkmonitor die [attachproperties](attachproperties.md) -Funktion für die erkannten Daten aufruft, muss der aufgerufene Parser die Daten analysieren und dann jede vorhandene Eigenschaft einem Speicherort in den erkannten Daten zuordnen. Der Parser bestimmt, welche Eigenschaften vorhanden sind und wo sich jede Eigenschaft in den Daten befindet. In der folgenden Abbildung werden vom Parser erkannte Daten angezeigt.

![vom Parser erkannte Daten](images/attachproperties1.png)

Während der Implementierung von [**attachproperties**](attachproperties.md)müssen Sie eine der folgenden Funktionen für jede Eigenschaft, die in einem Datenrahmen vorhanden ist, aufruft.

-   Wenn Sie die Eigenschaften Daten in einem Frame ändern möchten, können Sie die [**attachpropertyinstanceex**](attachpropertyinstanceex.md) -Funktion aufrufen.
-   Wenn Sie die Eigenschaften Daten in einem Frame nicht ändern möchten, können Sie die [**attachpropertyinstance**](attachpropertyinstance.md) -Funktion aufrufen.

> [!Note]  
> Es wird empfohlen, die Daten zu verwenden, wie Sie in der Erfassung vorhanden sind.

 

Im folgenden Verfahren werden die erforderlichen Schritte zum Implementieren von [**attachproperties**](attachproperties.md)beschrieben.

**So implementieren Sie attachproperties**

1.  Bestimmen Sie, welche Eigenschaften vorhanden sind, und die Eigenschaften Position in den Daten.
2.  Aufrufen von [**attachpropertyinstanceex**](attachpropertyinstanceex.md) für jede Eigenschaft mit einem Wert, den Sie ändern möchten.
3.  Aufrufen von [**attachpropertyinstance**](attachpropertyinstance.md) für jede Eigenschaft mit einem Wert, den Sie nicht ändern möchten. In der Regel ist dies die einzige Funktion, die aufgerufen werden muss.

Im folgenden finden Sie eine grundlegende Implementierung von " [**attachproperties**](attachproperties.md)". Beachten Sie, dass das Beispiel weder den Code zum Bestimmen der vorhandenen Eigenschaften noch den Code zum Suchen der Eigenschaften enthält.

``` syntax
#include <windows.h>

LPBYTE BHAPI MyProtocolAttachProperties( HFRAME   hFrame,
                                         LPBYTE   pMacFrame,
                                         LPBYTE   pBLRPLATEFrame,
                                         DWORD    MacType,
                                         DWORD    BytesLeft,
                                         HPROTOCOL  hPreviousProtocol,
                                         DWORD    nPrevProtocolOffset,
                                         DWORD    InstData)
{
  PBLRPLATEHDR pBLRPLATEHdr = (PBLRPLATEHDR)pBLRPLATEFrame;

  // Attach summary property.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_SUMMARY].hProperty,
                          (WORD)BytesLeft,
                          (LPBYTE)pBLRPLATEFrame,
                          0,        // No Help file.
                          0,        // Indent level.
                          0);      // Data flag.

  // Attach signature property.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_SIGNATURE].hProperty,
                          sizeof(DWORD),
                          &(pBLRPLATEHdr->Signature),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);        // Data flag.


  // Attach opcode.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_OPCODE].hProperty,
                          sizeof(WORD),
                          &(pBLRPLATEHdr->Opcode),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);        // Data flag.

  // Attach flags summary.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_FLAGS_SUMMARY].hProperty,
                          sizeof(BYTE),
                          &(pBLRPLATEHdr->Flags),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);       // Data flag.

// Attach flags decode.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_FLAGS_FLAGS].hProperty,
                          sizeof(BYTE),
                          &(pBLRPLATEHdr->Flags),
                          0,        // No Help file.
                          2,        // Indent level.
                          0);       // Data flag.

  RETURN null;

}
```

 

 



