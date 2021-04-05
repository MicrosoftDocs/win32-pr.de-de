---
title: Fehler Semantik für Kontext Handles
description: In diesem Thema wird die Fehler Semantik für Kontext Handles erläutert.
ms.assetid: fcf28519-39ad-4823-bc27-f3502e4d540c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4528b3f5160b92a4e6f10dbcf877e9fec59f81b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037025"
---
# <a name="failure-semantics-for-context-handles"></a>Fehler Semantik für Kontext Handles

In diesem Thema wird die Fehler Semantik für Kontext Handles erläutert.

## <a name="failure-semantics-when-closing-the-context-handle-fails"></a>Fehler Semantik beim Schließen des Kontext Handles schlägt fehl

Stellen Sie sich vor, eine Client Anwendung versucht, ein auf dem Server geöffnetes Kontext Handle zu schließen, ohne den Client Prozess zu schließen. Gehen Sie außerdem davon aus, dass beim Server zum Schließen des Kontext Handles ein Fehler auftritt (z. b. wenn der Client nicht über genügend Arbeitsspeicher verfügt). Die richtige Vorgehensweise zum Behandeln dieser Situation besteht darin, die [**rpcssdestroyclientcontext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) -Funktion aufzurufen. In einem solchen Fall bereinigt der Client seine Seite des Kontext Handles und schließt die Verbindung mit dem Server abgebrochen. Da es sich bei der Verbindung tatsächlich um einen Verbindungspool handelt (siehe [RPC und das Netzwerk](rpc-and-the-network.md)), bei dem es sich um eine Verweis Zählung mit einem Verweis für jede geöffnete Bindung oder ein geöffnetes Kontext Handle handelt, wird die Verbindung durch den Aufruf der **rpcssdestroyclientcontext** -Funktion nicht zerstört. Stattdessen wird der Verweis Zähler für den Verbindungspool verringert. Damit Verbindungen im Pool geschlossen werden können, muss der Client alle Bindungs Handles und Kontext Handles für diesen Server aus dem Client Prozess schließen. Anschließend werden alle Verbindungen im Pool geschlossen, und der Server-Lauf zeitmechanismus wird initiiert und bereinigt.

## <a name="failure-semantics-during-change-of-state-of-the-context-handle"></a>Fehler Semantik beim Ändern des Zustands des Kontext Handles

Die Informationen in diesem Abschnitt beziehen sich auf Windows XP-und spätere Plattformen.

Kontext Handles sind einfach Parameter für eine Funktion. Alle Änderungen im Zustand eines Kontext Handles treten auf, wenn Parameter gemarshallt oder nicht gemarshallt werden. Wenn ein Client z. b. ein Kontext Handle öffnet (von **null** in einen nicht-**null**-Wert geändert wird), öffnet die RPC-Laufzeit den RPC-Teil des Handles nicht, bis die Argumente für das Senden an den Client gemarshallt werden. Während der Zwischenzeit können Fehler auftreten. Aufgrund einer Vielzahl möglicher Netzwerk-oder geringer Ressourcen Bedingungen kann die Übertragung des Pakets an den Client fehlschlagen. Oder die Server Routine löst eine Ausnahme aus, wenn versucht wird, ein Kontext Handle zu ändern. In diesen oder anderen Fehlersituationen erhalten der Client und der Server möglicherweise inkonsistente Sichten des Kontext Handles. In diesem Abschnitt wird die Regel für den Status des Kontext Handles und die Verantwortung des Client-und Server Codes bei verschiedenen Fehlerbedingungen erläutert.

-   Ein **null** -Kontext Handle kommt an, aber die Server Routine stößt auf einen Fehler und löst eine Ausnahme aus.

    Es liegt in der Verantwortung der Server Routine, alle Kontext Handles – den Zustand, den Sie möglicherweise erstellt hat, zu bereinigen. Der Status der RPC-Laufzeit wird bereinigt.

-   Nicht-**null** -Kontext Handles werden empfangen, aber die Server Routine stößt auf einen Fehler und löst eine Ausnahme aus.

    Wenn die Server Routine das Kontext Handle geschlossen hat, weiß der Client es nicht, da der-Vorgang nicht erfolgreich ist. die weitere Verwendung des Kontext Handles führt zu einem RPC- \_ X- \_ SS-Kontext Konflikt \_ \_ Fehler auf dem Client. Wenn die Server Routine das Kontext Handle nicht ändert, kann Sie vom Client weiterhin verwendet werden. Wenn die Server Routine die im Server Kontext gespeicherten Informationen ändert, werden diese Informationen von neuen Aufrufen des Clients verwendet.

-   Ein Kontext Handle, das nicht **null** ist, wird erreicht, und die Server Routine schließt den Handle, aber entweder nach dem Marshalling des Kontext Handles oder bei der Verarbeitung nach dem Mars Hallen ist ein Fehler aufgetreten.

    Das Kontext Handle ist geschlossen, und weitere Aufrufe dieses Clients mit diesem Kontext Handle führen zu einem Fehler im RPC \_ X \_ SS-Kontext Konflikt \_ \_ auf dem Client.

-   Ein **null** -Kontext Handle wird erreicht, und der Server erstellt seinen Kontext für dieses Handle, aber entweder nach dem Marshalling des Kontext Handles oder nach dem Fehler bei der Verarbeitung nach dem Mars Hallen.

    In diesem Fall ruft die RPC-Laufzeit den Testlauf für dieses Kontext Handle auf und bereinigt den RPC-Status für dieses Kontext handle. Das Kontext Handle wird nicht auf der Clientseite erstellt.

-   Ein Kontext Handle, das nicht **null** ist, wird erreicht, und der Server ändert weder das Kontext Handle noch die im Server Kontext gespeicherten Informationen, und das Marshalling schlägt fehl, nachdem das Kontext Handle gemarshallt wurde.

    Neue Aufrufe vom Client verwenden das Kontext Handle, das der Server hat.

-   Ein **null** -Kontext Handle wird erreicht, und der Server legt ihn nicht auf einen anderen Wert als **null** fest, aber der-Rückruf schlägt fehl, bevor das Kontext Handle gemarshallt wird.

    In diesem Fall wird kein Kontext Handle auf dem Client erstellt.

-   Ein Kontext Handle, das nicht **null** ist, wird erreicht, und der Server legt den Wert auf **null** fest, aber das Marshalling schlägt fehl, bevor das Kontext Handle gemarshallt wird.

    In diesem Fall bleibt das Kontext Handle auf dem Server geschlossen, und der Client erhält \_ \_ \_ \_ beim Versuch, das Kontext Handle zu verwenden, nicht übereinstimmende RPC X SS-Kontext Fehler.

-   Ein **null** -Kontext Handle kommt auf dem Server an, und der Server legt ihn auf einen nicht-**null**-Wert fest, aber das Marshalling schlägt fehl, bevor das Kontext Handle gemarshallt wird.

    Das Kontext Handle wird aufgerufen, sodass der Server bereinigt werden kann, und auf dem Client wird kein Kontext Handle erstellt.

-   Ein Kontext Handle, das nicht **null** ist, wird erreicht, und der Server ändert weder das Kontext Handle noch die im Server Kontext gespeicherten Informationen, und das Marshalling schlägt fehl, bevor das Kontext Handle gemarshallt wird.

    Neue Aufrufe vom Client verwenden den Status auf dem Server.

-   Ein Kontext Handle wird als Rückgabewert deklariert, und die Server Routine gibt für das Kontext Handle **null** zurück, und das Marshalling schlägt fehl, bevor das Kontext Handle gemarshallt wird.

    In diesem Fall wird kein neuer Kontext auf dem Client erstellt.

-   Ein Kontext Handle wird als Rückgabewert deklariert, und die Server Routine gibt für das Kontext Handle einen Wert zurück, der nicht **null** ist, und das Marshalling schlägt fehl, bevor das Kontext Handle gemarshallt wird.

    Die RPC-Laufzeit ruft die-Kontext Handle-Lauf Zeit Routine auf, um eine Bereinigung zu erhalten, und auf dem Client wird kein neuer Kontext erstellt.

 

 




