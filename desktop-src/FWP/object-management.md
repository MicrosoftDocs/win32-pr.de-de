---
title: Objekt Verwaltung
description: In diesem Abschnitt wird die korrekte Verwendung von API-Objekttypen der Windows-Filter Plattform (WFP) behandelt.
ms.assetid: 2625ef9a-0e62-4e21-ba93-047965d0d782
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc41560bb85a7e79c0262d77c0b34fe6c1d9bfd6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472908"
---
# <a name="object-management"></a>Objekt Verwaltung

In diesem Abschnitt wird die korrekte Verwendung von API-Objekttypen der Windows-Filter Plattform (WFP) behandelt.

## <a name="sessions"></a>Sitzungen

Die WFP-API ist Sitzungs orientiert, und die meisten Funktionsaufrufe werden innerhalb des Kontexts einer Sitzung durchgeführt. Eine neue Client Sitzung wird durch Aufrufen von [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)erstellt. Die Sitzung endet, wenn der Client [**FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0) aufruft oder der Client Prozess beendet wird. Wenn eine Sitzung entweder zum Zweck oder durch den RPC-Rundown zerstört wird, bricht die Basis Filter-Engine (BFE) zuerst jede vorhandene Transaktion ab.

Beim Erstellen einer neuen Sitzung kann der Aufrufer eine dynamische Sitzung erstellen, indem er das Flag für das [**dynamische fwpm- \_ \_ sitzungsflag \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0) an [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)übergibt. Alle Objekte, die während einer dynamischen Sitzung hinzugefügt werden, werden automatisch gelöscht, wenn die Sitzung beendet wird.

## <a name="transactions"></a>Transaktionen

Die WFP-API ist transaktional, und die meisten Funktionsaufrufe werden innerhalb des Kontexts einer Transaktion durchgeführt. Aufrufer können [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0), [**FwpmTransactionCommit0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactioncommit0)und [**FwpmTransactionAbort0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionabort0) verwenden, um Transaktionen explizit zu steuern. Wenn ein Funktions Aufrufvorgang jedoch außerhalb einer expliziten Transaktion erfolgt, wird er innerhalb einer impliziten Transaktion ausgeführt. Wenn eine Transaktion ausgeführt wird, wird Sie automatisch abgebrochen, wenn eine Sitzung beendet wird. Implizite Transaktionen werden nie erzwungen.

Transaktionen sind entweder schreibgeschützt oder Lese-/Schreibzugriff und erzwingen eine strikte atomarische konsistente isolierte dauerhafte Semantik ([Acid](../cossdk/acid-properties.md)).

Für jede Client Sitzung kann jeweils nur eine Transaktion ausgeführt werden. Wenn der Aufrufer versucht, eine zweite Transaktion zu starten, bevor er einen Commit oder Abbruch des ersten Vorgangs ausführt, gibt BFE einen Fehler zurück.

Wenn ein Vorgang im Verlauf einer Transaktion fehlschlägt, wirkt sich dies nicht auf den Gesamtstatus der Transaktion aus. Nehmen wir beispielsweise an, dass der Client eine Transaktion startet und [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0) dreimal erfolgreich aufruft, bevor ein vierter Aufruf fehlschlägt. Der Client hat jetzt die Option:

-   Abbrechen der Transaktion. in diesem Fall wird keiner der Filter hinzugefügt.
-   Commit für die Transaktion wird ausgeführt. in diesem Fall werden die ersten drei Filter hinzugefügt.
-   Fortfahren mit weiteren Vorgängen, einschließlich potenziell wiederholtem fehlgeschlagener [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0).

Wenn eine Transaktion gestartet wird, wartet BFE, bis die [**txnwaittimeoutinmsec**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0) der Sitzung abläuft, um die Sperre zu erhalten. Wenn die Sperre innerhalb dieses Zeitraums nicht abgerufen wird, schlagen die Sperr Abruf (und der [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) -Aufruf) fehl. Dadurch wird verhindert, dass Clients unbegrenzt reagieren. Wenn der Client kein Sperr Timeout angegeben hat, wird der Standardwert auf 15 Sekunden festgelegt.

Jede Transaktion verfügt auch über ein Sperr Timeout. Dies ist die maximale Zeitspanne, die die Sperre besitzen kann. Wenn der Besitzer die Sperre nicht innerhalb dieses Zeitraums freigibt, wird die Transaktion erzwungen, wodurch die Sperre aufgehoben wird. Das Sperr Timeout ist nicht konfigurierbar. Es ist unendlich für Aufrufer im Kernelmodus und eine Stunde für Aufrufer im Benutzermodus. Wenn eine Transaktion erzwungen wird, schlägt der nächste innerhalb dieser Transaktion vorgenommene-Vorgang fehl, und **FWP \_ E \_ TXn wird \_ abgebrochen**.

## <a name="object-lifetimes"></a>Objekt Lebensdauer

Objekte können eine von vier möglichen Lebens dauern aufweisen:

-   Dynamisch – ein Objekt ist nur dann dynamisch, wenn es mithilfe eines dynamischen Sitzungs Handles hinzugefügt wird. Dynamische Objekte sind so lange Live, bis Sie gelöscht werden oder die besitzende Sitzung beendet wird.
-   Statische –-Objekte sind standardmäßig statisch. Statische Objekte sind so lange Live, bis Sie gelöscht werden, BFE beendet oder das System heruntergefahren wird.
-   Persistente – persistente Objekte werden erstellt, indem das entsprechende **fwpm- \_ \* \_ Flag \_ persistentes** Flag an eine **fwpm \* Add0** -Funktion übergeben wird. Persistente Objekte sind Live, bis Sie gelöscht werden.
-   Integrierte – integrierte Objekte werden von BFE vordefiniert und können nicht hinzugefügt oder gelöscht werden. Sie leben immer wieder.

Filter in Kernel Modus-Schichten können als Start Zeitfilter gekennzeichnet werden, indem das entsprechende Flag an [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)übergeben wird. Start Zeitfilter werden dem System hinzugefügt, wenn der TCP/IP-Treiber gestartet wird, und entfernt, wenn die Initialisierung von BFE abgeschlossen ist. Persistente Objekte werden hinzugefügt, wenn BFE gestartet wird.

In vielen Fällen soll ein Richtlinien Anbieter die permanente Richtlinie möglicherweise nicht erzwingen, wenn der Anbieter deaktiviert wurde. Wenn Sie einen Anbieter hinzufügen, kann der Aufrufer einen optionalen Windows-Dienstnamen angeben. Beim Hinzufügen von permanenten Objekten kann der Aufrufer optional den Anbieter angeben, der das Objekt "besitzt". Beim Dienst Start fügt BFE nur persistente Objekte zum System hinzu, wenn Sie keinem Anbieter zugeordnet sind, oder der zugeordnete Anbieter hat keinen Windows-Dienstnamen, oder der zugehörige Windows-Dienst ist auf automatischen Start festgelegt.

## <a name="object-associations"></a>Objekt Zuordnungen

Einige Objekte verfügen über Verweise auf andere Objekte. Ein Filter verweist z. b. immer auf eine Ebene und verweist möglicherweise auf einen Legenden-und einen Anbieter Kontext. Objekte können nicht auf Objekte verweisen, die eine kürzere Lebensdauer aufweisen können. Folglich kann ein dynamisches Objekt nicht auf ein dynamisches Objekt aus einer anderen Sitzung verweisen. Ein statisches Objekt kann nicht auf ein dynamisches Objekt verweisen. Ein persistentes Objekt kann nicht auf ein dynamisches Objekt, ein statisches Objekt oder ein dauerhaftes Objekt verweisen, das im Besitz eines anderen Anbieters ist.

Ein Objekt kann erst gelöscht werden, wenn alle Objekte, die darauf verweisen, gelöscht wurden.

## <a name="luids-and-guids"></a>LUIDs und GUIDs

Alle Benutzermodus-WFP-API-Objekte (swpm) werden durch eine Globally Unique Identifier (**GUID**) identifiziert, und es wird über Ihre **GUID** s auf andere Objekte verwiesen. Der **GUID** muss nur innerhalb des Objekt Typs eindeutig sein. Beispielsweise können ein Filter und ein Anbieter Kontext dieselbe **GUID** aufweisen, aber zwei Filter sind nicht möglich. Beim Hinzufügen eines neuen Objekts können Aufrufer die **GUID** des Objekts zuweisen oder Sie mit 0 (null) initialisieren lassen, und die **GUID** kann von BFE zugewiesen werden.

Alle Kernelmodus-WFP-API-Objekte (SWPS) werden durch einen lokalen eindeutigen Bezeichner (**LUID**) identifiziert und über Ihre LUID auf andere Objekte verweisen. Der Switch von **GUID** zu **LUID** ermöglicht WFP, den nicht auslagerten Pool zu sparen und die Lauf Zeit Verarbeitung zu optimieren. Die Breite der **LUID** hängt von dem Objekttyp und den Bereichen von einem **UInt16** zu einem **UINT64** ab. **LUID** s werden immer von BFE zugewiesen.

 

 