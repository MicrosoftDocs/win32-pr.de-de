---
title: RPC-NDR-Engine (RPC)
description: Die RPC-Engine (Remote Procedure Call, Netzwerkdatendarstellung) ist die Marshalling-Engine der RPC- und DCOM-Komponenten.
ms.assetid: E452AA27-053D-4032-868B-CF2D5C0D4BE0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0dd01ae40562528ac89c8b9dcfb0b9009ead5ca1a92b2cde90c3274d574fc1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018420"
---
# <a name="rpc-ndr-engine-rpc"></a>RPC-NDR-Engine (RPC)

Die RPC-Engine (Remote Procedure Call, Netzwerkdatendarstellung) ist die Marshalling-Engine der RPC- und DCOM-Komponenten. Die NDR-Engine behandelt alle Stubprobleme eines Remoteaufrufs. Als Prozess wird das NDR-Marshalling durch den C-Code von MIDL-generierten Stubs, einem MIDL-JIT-Generator oder von Stubs gesteuert, die von anderen Tools generiert oder manuell geschrieben wurden. Die NDR-Engine steuert wiederum die zugrunde liegende Laufzeit (DCOM oder RPC), die mit bestimmten Transporten kommuniziert.

Obwohl Stubs C-Code sind, der von MIDL generiert wird, wird Anwendungen empfohlen, Stubs als nicht transparent zu behandeln, und es wird dringend davon abgeraten, etwas innerhalb des Stubs zu ändern. Das Verhalten ist nicht definiert, wenn diese NDR-Routinen aus dem Kontext heraus aufgerufen werden.

Die RPC-NDR-Engine wird in den folgenden Themen ausführlicher beschrieben:

-   [Übertragungssyntax und NDR64](transfer-syntax-and-ndr64.md)
-   [RPC-NDR-Formatzeichenfolgen](rpc-ndr-format-strings.md)
-   [REFERENZ ZUR RPC-NDR-Schnittstelle](rpc-ndr-interface-reference.md)

 

 




