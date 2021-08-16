---
description: Ruft die AttachProperties-Funktion auf, um die Eigenschaften zuzuordnen, die in einem Teil der erkannten Daten vorhanden sind.
ms.assetid: f1949904-ceb2-4650-847f-01f597ff3620
title: Implementieren von AttachProperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbb3571cf655e07b2879513f826192711992fb49a02cc7a4954d5322a948caf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365349"
---
# <a name="implementing-attachproperties"></a>Implementieren von AttachProperties

Netzwerkmonitor ruft die [**AttachProperties-Funktion**](attachproperties.md) auf, um die Eigenschaften zuzuordnen, die in einem Teil der erkannten Daten vorhanden sind. Die [**AttachProperties-Funktion**](attachproperties.md) ordnet die Eigenschaften einem bestimmten Speicherort zu.

Netzwerkmonitor verwendet den folgenden Prozess, um die Daten in einem Frame zu analysieren.

-   Zuerst ruft Netzwerkmonitor [RecognizeFrame](recognizeframe.md) auf, um alle Protokolle zu erkennen, die in einem Frame vorhanden sind.
-   Anschließend ruft Netzwerkmonitor [**AttachProperties**](attachproperties.md) für jeden Parser auf, der ein Datenteil erkennt.

Wenn Netzwerkmonitor die [AttachProperties-Funktion](attachproperties.md) für die erkannten Daten aufruft, muss der aufgerufene Parser die Daten analysieren und dann jede vorhandene Eigenschaft einem Speicherort in den erkannten Daten zuordnen. Der Parser bestimmt, welche Eigenschaften vorhanden sind und wo sich die einzelnen Eigenschaften in den Daten befinden. Die folgende Abbildung zeigt vom Parser erkannte Daten.

![Vom Parser erkannte Daten](images/attachproperties1.png)

Während der Implementierung von [**AttachProperties**](attachproperties.md)müssen Sie eine der folgenden Funktionen für jede Eigenschaft aufrufen, die in einem Datenrahmen vorhanden ist.

-   Rufen Sie die [**AttachPropertyInstanceEx-Funktion**](attachpropertyinstanceex.md) auf, wenn Sie die Eigenschaftsdaten in einem Frame ändern möchten.
-   Rufen Sie die [**AttachPropertyInstance-Funktion**](attachpropertyinstance.md) auf, wenn Sie die Eigenschaftsdaten in einem Frame nicht ändern möchten.

> [!Note]  
> Es wird empfohlen, die Daten so zu verwenden, wie sie in der Erfassung vorhanden sind.

 

Mit dem folgenden Verfahren werden die Schritte identifiziert, die zum Implementieren von [**AttachProperties**](attachproperties.md)erforderlich sind.

**So implementieren Sie AttachProperties**

1.  Bestimmen Sie, welche Eigenschaften vorhanden sind und welche Eigenschaften sich in den Daten befinden.
2.  Rufen Sie [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) für jede Eigenschaft mit einem Wert auf, den Sie ändern möchten.
3.  Rufen Sie [**AttachPropertyInstance**](attachpropertyinstance.md) für jede Eigenschaft mit einem Wert auf, den Sie nicht ändern möchten. In der Regel ist dies die einzige Funktion, die Sie aufrufen müssen.

Im Folgenden ist eine grundlegende Implementierung von [**AttachProperties .**](attachproperties.md) Beachten Sie, dass das Beispiel weder den Code enthält, um zu bestimmen, welche Eigenschaften vorhanden sind, noch den Code, um die Eigenschaften zu suchen.

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

 

 



