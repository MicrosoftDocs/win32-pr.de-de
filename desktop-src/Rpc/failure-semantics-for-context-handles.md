---
title: Fehlersemantik für Kontexthandles
description: In diesem Thema wird die Fehlersemantik für Kontexthandles erläutert.
ms.assetid: fcf28519-39ad-4823-bc27-f3502e4d540c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9549a659c56c4761de8df4f43c54b823d32f74786af928821ba82b6effc3bba7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021270"
---
# <a name="failure-semantics-for-context-handles"></a>Fehlersemantik für Kontexthandles

In diesem Thema wird die Fehlersemantik für Kontexthandles erläutert.

## <a name="failure-semantics-when-closing-the-context-handle-fails"></a>Fehlersemantik beim Schließen des Kontexthandle schlägt fehl

Imagine versucht eine Clientanwendung, ein Kontexthandle zu schließen, das sie auf dem Server geöffnet hat, ohne den Clientprozess herunterzufahren. Gehen Sie außerdem davon aus, dass der Aufruf des Servers zum Schließen des Kontexthandle fehlschlägt (z. B. ist der Client nicht genügend Arbeitsspeicher). Die richtige Methode zum Behandeln dieser Situation besteht darin, die [**RpcSsDestroyClientContext-Funktion**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) aufzurufen. In diesem Fall bereinigt der Client seine Seite des Kontexthandle und schließt die Verbindung mit dem Server abgebrochen. Da es sich bei der Verbindung tatsächlich um einen Verbindungspool handelt (siehe [RPC und das Netzwerk](rpc-and-the-network.md)), der mit einem Verweis für jede geöffnete Bindung oder jedes geöffnete Kontexthandle gezählt wird, zerstört das Zerstören des Kontexthandle durch Aufrufen der **RpcSsDestroyClientContext-Funktion** die Verbindung nicht tatsächlich. Stattdessen wird der Verweiszähler für den Verbindungspool dekrementt. Damit Verbindungen im Pool geschlossen werden, muss der Client alle Bindungshandles und Kontexthandles für diesen Server aus dem Clientprozess schließen. Anschließend werden alle Verbindungen im Pool geschlossen, und der Server-Run-Down-Mechanismus wird initiiert und bereinigt.

## <a name="failure-semantics-during-change-of-state-of-the-context-handle"></a>Fehlersemantik während der Zustandsänderung des Kontexthandle

Die Informationen in diesem Abschnitt beziehen sich auf Windows XP und höhere Plattformen.

Kontexthandles sind einfach Parameter für eine Funktion. Alle Änderungen im Zustand eines Kontexthandle erfolgen, wenn Parameter gemarshallt oder nicht gemarshallt werden. Wenn ein Client beispielsweise ein Kontexthandle öffnet (ändert es von **NULL** in nicht **NULL),** öffnet die RPC-Laufzeit den RPC-Teil des Handles erst, wenn die Argumente zum Senden an den Client gemarshallt werden. Fehler können während der Zwischenzeit auftreten. Aufgrund einer Vielzahl möglicher Netzwerk- oder ressourcenschwacher Bedingungen kann die Übertragung des Pakets an den Client fehlschlagen. Oder die Serverroutine löst beim Versuch, ein Kontexthandle zu ändern, eine Ausnahme aus. In diesen oder anderen Fehlersituationen erhalten Client und Server möglicherweise inkonsistente Ansichten des Kontexthandle. In diesem Abschnitt werden die Regel für den Zustand des Kontexthandle und die Verantwortung des Client- und Servercodes bei verschiedenen Fehlerbedingungen erläutert.

-   Ein **NULL-Kontexthandle** kommt an, aber die Serverroutine erkennt einen Fehler und löst eine Ausnahme aus.

    Es liegt in der Verantwortung der Serverroutine, alle kontextbezogenen Zustände zu bereinigen, die möglicherweise erstellt wurden. Die RPC-Laufzeit bereinigt ihren Zustand.

-   Ein **Nicht-NULL-Kontexthandles** kommt an, aber die Serverroutine erkennt einen Fehler und löst eine Ausnahme aus.

    Wenn die Serverroutine das Kontexthandle geschlossen hat, weiß der Client nicht, da der Aufruf nicht erfolgreich ist. Die weitere Verwendung des Kontexthandle führt zu einem RPC \_ X \_ SS \_ CONTEXT \_ MISMATCH-Fehler auf dem Client. Wenn die Serverroutine das Kontexthandle nicht ändert, kann sie vom Client weiterhin verwendet werden. Wenn die Serverroutine die im Serverkontext gespeicherten Informationen ändert, verwenden neue Aufrufe vom Client diese Informationen.

-   Ein Nicht-NULL-Kontexthandle kommt an, und die Serverroutine schließt das Handle, aber entweder wird gemarshallt, nachdem das Kontexthandle gemarshallt wurde, oder die Verarbeitung nach dem Marshalling fehlgeschlagen.

    Das Kontexthandle wird geschlossen, und weitere Aufrufe dieses Clients, die dieses Kontexthandle verwenden, führen zu einem RPC \_ X \_ SS \_ CONTEXT \_ MISMATCH-Fehler auf dem Client.

-   Ein **NULL-Kontexthandle** trifft ein, und der Server erstellt seinen Kontext für dieses Handle, aber entweder wird gemarshallt, nachdem das Kontexthandle gemarshallt wurde, oder die Verarbeitung nach dem Marshallingfehler.

    In diesem Fall ruft die RPC-Laufzeit das Run down für dieses Kontexthandle auf und bereinigt den RPC-Status für dieses Kontexthandle. Das Kontexthandle wird auf clientseitiger Seite nicht erstellt.

-   Ein **Nicht-NULL-Kontexthandle** kommt an, und der Server ändert entweder nicht das Kontexthandle, oder er ändert die im Serverkontext gespeicherten Informationen, und das Marshalling schlägt fehl, nachdem das Kontexthandle gemarshallt wurde.

    Neue Aufrufe vom Client verwenden das Kontexthandle, über das der Server verfügt.

-   Ein **NULL-Kontexthandle** kommt an, und der Server legt es nicht auf einen anderen Wert als **NULL** fest, aber der Aufruf schlägt fehl, bevor das Kontexthandle gemarshallt wird.

    In diesem Fall wird kein Kontexthandle auf dem Client erstellt.

-   Ein Nicht-NULL-Kontexthandle kommt an, und der Server legt es auf **NULL** fest. Das Marshalling schlägt jedoch fehl, bevor das Kontexthandle gemarshallt wird.

    In diesem Fall bleibt das Kontexthandle auf dem Server geschlossen, und der Client erhält RPC \_ X \_ SS \_ CONTEXT \_ MISMATCH-Fehler, wenn versucht wird, das Kontexthandle zu verwenden.

-   Ein **NULL-Kontexthandle** trifft auf dem Server ein, und der Server legt es auf ungleich **NULL** fest. Das Marshalling schlägt jedoch fehl, bevor das Kontexthandle gemarshallt wird.

    Das ausgeführte Kontexthandle muss aufgerufen werden, damit der Server bereinigt werden kann, und auf dem Client wird kein Kontexthandle erstellt.

-   Ein **Nicht-NULL-Kontexthandle** kommt an, und der Server ändert entweder nicht das Kontexthandle, oder er ändert die im Serverkontext gespeicherten Informationen, und das Marshalling schlägt fehl, bevor das Kontexthandle gemarshallt wird.

    Neue Aufrufe vom Client verwenden den Zustand auf dem Server.

-   Ein Kontexthandle wird als Rückgabewert deklariert, und die Serverroutine gibt **NULL** für das Kontexthandle zurück, und das Marshalling schlägt fehl, bevor das Kontexthandle gemarshallt wird.

    In diesem Fall wird kein neuer Kontext auf dem Client erstellt.

-   Ein Kontexthandle wird als Rückgabewert deklariert, und die Serverroutine gibt nicht **NULL** für das Kontexthandle zurück, und das Marshalling schlägt fehl, bevor das Kontexthandle gemarshallt wird.

    Die RPC-Laufzeit ruft die Run-Down-Routine des Kontexthandle auf, um eine Bereinigung zu ermöglichen, und es wird kein neuer Kontext auf dem Client erstellt.

 

 




