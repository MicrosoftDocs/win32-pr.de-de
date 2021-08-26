---
title: Funktionsattribute
description: Die Attribute \callback\ und \local\ können als Funktionsattribute angewendet werden.
ms.assetid: 05e19164-072c-4a5a-878d-845273975854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be36cac561a10ae2e1177c29dfc0e1219f650daf26af8154c47cdbd7e3d2bd57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021020"
---
# <a name="function-attributes"></a>Funktionsattribute

Die **\[** [**Rückrufe**](/windows/desktop/Midl/callback) **\]** und **\[** [**lokalen**](/windows/desktop/Midl/local) Attribute **\]** können als Funktionsattribute angewendet werden.

Ein Rückruf ist ein Remoteaufruf vom Server zum Client, der als Teil eines konzeptionellen Single-Execution-Threads ausgeführt wird. Ein Rückruf wird immer im Kontext eines Remoteaufrufs (oder Rückrufs) ausgegeben und von dem Thread ausgeführt, der den ursprünglichen Remoteaufruf (oder Rückruf) ausgegeben hat.

Es ist häufig wünschenswert, eine lokale Prozedurdeklaration in der IDL-Datei zu platzieren, da dies der logische Ort zum Beschreiben von Schnittstellen zu einem Paket ist. Das **\[** [**lokale Attribut**](/windows/desktop/Midl/local) **\]** gibt an, dass eine Prozedurdeklaration eigentlich keine Remotefunktion, sondern eine lokale Prozedur ist. Der MIDL-Compiler generiert keine Stubs für Funktionen mit dem **\[ lokalen \]** Attribut.

Beachten Sie, dass die Verwendung von Rückrufen bei der **\[** [](/windows/desktop/Midl/callback) **\]** Multithreadprogrammierung nicht empfohlen wird. Als Singlethread-Programmierfunktion ist sie nicht für die Unterstützung der Sicherheitsanforderungen einer Multithreadumgebung ausgestattet.

 

 