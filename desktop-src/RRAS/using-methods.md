---
title: Verwenden von Methoden
description: Wenn sich ein Client beim Routingtabellen-Manager registriert, kann er eine Reihe von Methoden exportieren. Diese Methoden werden von anderen Clients verwendet, um clientspezifische Informationen abzurufen. Methoden ermöglichen die private Kommunikation zwischen Clients des Routingtabellen-Managers.
ms.assetid: 6d984a02-d005-43ad-81c4-968ae9c1a105
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 150edb6435e0021c13e129f7c1e7a3016dc0974283fcdd138189f7d1c4a3184a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025100"
---
# <a name="using-methods"></a>Verwenden von Methoden

Wenn sich ein Client beim Routingtabellen-Manager registriert, kann er eine Reihe von Methoden exportieren. Diese Methoden werden von anderen Clients verwendet, um clientspezifische Informationen abzurufen. Methoden ermöglichen die private Kommunikation zwischen Clients des Routingtabellen-Managers.

Ein Client kann die Liste der Methoden abrufen, die von einem anderen Client exportiert werden. Der Client ruft die [**RtmGetEntityMethods-Funktion**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods) auf und stellt das Handle des Zielclients zur Verfügung.

Jede methode, die von einem Client exportiert wird, wird durch ihren Methodenbezeichner eindeutig identifiziert. Jeder Client kann bis zu 32 Methoden exportieren. Jede Methode entspricht einem Bitsatz im **MethodType-Member** der [**RTM \_ ENTITY EXPORT \_ \_ METHOD-Struktur.**](/windows/win32/api/rtmv2/nc-rtmv2-_entity_method) Um mehrere Methoden aufzurufen, sollte der Client ein logisches OR der Bezeichner für diese Methoden ausführen. Die Syntax und Semantik von Eingabe- und Ausgabestrukturen für jedes Protokoll muss angegeben werden, wenn das Protokoll implementiert wird.

> [!Note]  
> Methodenbezeichnerwerte, die einem in der unteren Hälfte des **MethodType-Members** festgelegten Bit entsprechen (die unteren 16 Bits), werden von Microsoft reserviert.

 

Um die -Methode eines zweiten Clients aufzurufen, ruft ein Client die [**RtmInvokeMethod-Funktion**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) auf. Der Routingtabellen-Manager vermittelt alle Anforderungen, um die Methoden eines Clients aufzurufen. Der Routingtabellen-Manager führt zwei Funktionen aus, wenn er zwischen Clients vermittelt:

-   Verhindern, dass der zweite Client eine Methode für einen Client aufruft, der die Registrierung aufgehoben hat.
-   Halten einer "Invoke"-Anforderung, wenn Methoden blockiert werden, und zulassen, dass die Anforderung fortgesetzt wird, wenn die Blockierung der Methoden aufgehoben wird.

Wenn ein Client verhindern muss, dass andere Clients seine Methoden ausführen, kann der Client [**RtmBlockMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods)aufrufen. Der Routingtabellen-Manager lässt die Verarbeitung eines Aufrufs von [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) erst zu, wenn der Client die Blockierung seiner Methoden wieder aufgehoben hat.

Clients blockieren Methoden in der Regel, wenn Sie Änderungen an den privaten Daten vornehmen, die zwischen Clients ausgetauscht werden. Blockierende Methoden sind eine optionale Aktion. Ein Client kann auch interne Sperren verwenden, um zu verhindern, dass andere Clients Methoden aufrufen.

Beispielcode, der zeigt, wie diese Funktionen verwendet werden, finden Sie unter [Abrufen und Aufrufen der exportierten Methoden für einen Client.](obtain-and-call-the-exported-methods-for-a-client.md)

 

 




