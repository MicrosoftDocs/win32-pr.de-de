---
title: Funktionsattribute
description: Die Attribute \ Callback \ und \ local \ können als Funktions Attribute angewendet werden.
ms.assetid: 05e19164-072c-4a5a-878d-845273975854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ef199b937d5a3e9a8444be9ed65749da007ced
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729641"
---
# <a name="function-attributes"></a>Funktionsattribute

Die **\[** Attribute [**Callback**](/windows/desktop/Midl/callback) **\]** und **\[** [**local**](/windows/desktop/Midl/local) **\]** können als Funktions Attribute angewendet werden.

Ein Rückruf ist ein Remote-Aufrufe von Server zu Client, der als Teil eines konzeptionellen Single-Execution-Threads ausgeführt wird. Ein Rückruf wird immer im Kontext eines Remote Aufrufs (oder eines Rückrufs) ausgegeben und von dem Thread ausgeführt, der den ursprünglichen Remote Rückruf (oder Rückruf) ausgegeben hat.

Häufig ist es wünschenswert, eine lokale Prozedur Deklaration in der IDL-Datei zu platzieren, da dies die logische Stelle ist, um Schnittstellen zu einem Paket zu beschreiben. Das **\[** [**local**](/windows/desktop/Midl/local) - **\]** Attribut gibt an, dass eine Prozedur Deklaration nicht tatsächlich eine Remote Funktion, sondern eine lokale Prozedur ist. Der mittlerer l-Compiler generiert keine stubfunktionen für Funktionen mit dem **\[ lokalen \]** Attribut.

Beachten Sie, dass die Verwendung von **\[** [**Callback**](/windows/desktop/Midl/callback) **\]** bei der Multithreadprogrammierung nicht empfohlen wird. Als Single Thread-Programmierfunktion ist Sie nicht für die Unterstützung der Sicherheitsanforderungen, die eine Multithreadumgebung bereitstellt, bereit.

 

 