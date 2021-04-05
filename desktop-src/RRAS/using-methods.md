---
title: Verwenden von Methoden
description: Wenn ein Client beim Routing Tabellen-Manager registriert wird, kann er eine Reihe von Methoden exportieren. Diese Methoden werden von anderen Clients zum Abrufen von Client spezifischen Informationen verwendet. Methoden ermöglichen die private Kommunikation zwischen Clients des Routing Tabellen-Managers.
ms.assetid: 6d984a02-d005-43ad-81c4-968ae9c1a105
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33bd895fbb3f8f54224522786b5794c5c6c57a9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947797"
---
# <a name="using-methods"></a>Verwenden von Methoden

Wenn ein Client beim Routing Tabellen-Manager registriert wird, kann er eine Reihe von Methoden exportieren. Diese Methoden werden von anderen Clients zum Abrufen von Client spezifischen Informationen verwendet. Methoden ermöglichen die private Kommunikation zwischen Clients des Routing Tabellen-Managers.

Ein Client kann die Liste der von einem anderen Client exportierten Methoden abrufen. Der Client ruft die [**rtmgetentitymethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods) -Funktion auf und stellt das Handle des Ziel Clients bereit.

Jede Methode, die von einem Client exportiert wird, wird durch den Methoden Bezeichner eindeutig identifiziert. Jeder Client kann bis zu 32 Methoden exportieren. Jede Methode entspricht einem Bit, das im **methodType** -Member der Struktur der [**RTM- \_ Entitäts \_ Export \_ Methode**](/windows/win32/api/rtmv2/nc-rtmv2-_entity_method) festgelegt ist. Um mehrere Methoden aufzurufen, muss der Client eine logische OR-ID für diese Methoden ausführen. Die Syntax und Semantik der Eingabe-und Ausgabe Strukturen für jedes Protokoll muss angegeben werden, wenn das Protokoll implementiert wird.

> [!Note]  
> Methodenbezeichnerwerte, die einem Bit entsprechen, das in der unteren Hälfte des **methodType** -Members (die unteren 16 Bits) festgelegt ist, sind von Microsoft reserviert.

 

Um die-Methode eines zweiten Clients aufzurufen, Ruft ein Client die [**rtminvokemethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) -Funktion auf. Der Routing Tabellen-Manager gibt alle Anforderungen zum Aufrufen der Methoden eines Clients ein. Der Routing Tabellen-Manager führt zwei Funktionen aus, wenn er zwischen Clients unterscheidet:

-   Verhindern, dass der zweite Client eine Methode für einen Client aufruft, dessen Registrierung aufgehoben wird.
-   Eine Aufruf Anforderung, wenn Methoden blockiert werden und die Anforderung fortgesetzt werden kann, wenn die Blockierung der Methoden aufgehoben wird.

Wenn ein Client die Ausführung seiner Methoden durch andere Clients verhindern muss, kann der Client [**rtmblockmethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods)aufzurufen. Der Routing Tabellen-Manager lässt die Verarbeitung von [**rtminvokemethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) erst dann zu, wenn der Client die Blockierung seiner Methoden wieder aufhebt.

Clients blockieren in der Regel Methoden, wenn Änderungen an den privaten Daten vorgenommen werden, die zwischen Clients ausgetauscht werden. Blockierungs Methoden sind eine optionale Aktion. Ein Client kann auch interne Sperren verwenden, um zu verhindern, dass andere Clients Methoden aufrufen.

Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden Sie unter Abrufen [und Abrufen der exportierten Methoden für einen Client](obtain-and-call-the-exported-methods-for-a-client.md).

 

 




