---
title: Objektverwaltung
description: In diesem Abschnitt wird die korrekte Verwendung von Windows WFP-API-Objekttypen (Filtering Platform) behandelt.
ms.assetid: 2625ef9a-0e62-4e21-ba93-047965d0d782
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5cb51d4e78049d7911a4a5ed265091e05bc1cbb00ce470e332d59dd23c6026d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068850"
---
# <a name="object-management"></a>Objektverwaltung

In diesem Abschnitt wird die korrekte Verwendung von Windows WFP-API-Objekttypen (Filtering Platform) behandelt.

## <a name="sessions"></a>Sitzungen

Die WFP-API ist sitzungsorientiert, und die meisten Funktionsaufrufe werden im Kontext einer Sitzung vorgenommen. Eine neue Clientsitzung wird durch Aufrufen von [**FwpmEngineOpen0 erstellt.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0) Die Sitzung endet entweder, wenn der [**Client FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0) aufruft oder der Clientprozess beendet wird. Wenn eine Sitzung entweder zwecks oder durch den RPC-Rundown zerstört wird, bricht die Basisfilterungs-Engine (Base Filtering Engine, BFE) zuerst alle vorhandenen Transaktionen ab.

Beim Erstellen einer neuen Sitzung kann der Aufrufer eine dynamische Sitzung erstellen, indem er das [**Flag FWPM \_ SESSION FLAG \_ \_ DYNAMIC**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0) an [**FwpmEngineOpen0 über gibt.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0) Alle Objekte, die während einer dynamischen Sitzung hinzugefügt werden, werden automatisch gelöscht, wenn die Sitzung beendet wird.

## <a name="transactions"></a>Transaktionen

Die WFP-API ist transaktional, und die meisten Funktionsaufrufe werden im Kontext einer Transaktion ausgeführt. Aufrufer können [**FwpmTransactionBegin0,**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) [**FwpmTransactionCommit0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactioncommit0)und [**FwpmTransactionAbort0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionabort0) verwenden, um Transaktionen explizit zu steuern. Wenn ein Funktionsaufruf jedoch außerhalb einer expliziten Transaktion erfolgt, wird er innerhalb einer impliziten Transaktion ausgeführt. Wenn eine Transaktion ausgeführt wird und eine Sitzung beendet wird, wird sie automatisch abgebrochen. Implizite Transaktionen werden nie abgebrochen.

Transaktionen sind entweder schreibgeschützt oder lesen/schreiben und erzwingen strenge ACID-Semantik (Atomic Consistent Isolated Durable).[](../cossdk/acid-properties.md)

Für jede Clientsitzung kann jeweils nur eine Transaktion ausgeführt werden. Wenn der Aufrufer versucht, vor dem Committen oder Abbrechen der ersten Transaktion eine zweite Transaktion zu starten, gibt BFE einen Fehler zurück.

Wenn ein Vorgang während einer Transaktion fehlschlägt, wirkt sich dies nicht auf den Gesamtzustand der Transaktion aus. Angenommen, der Client startet eine Transaktion und ruft [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0) dreimal erfolgreich auf, bevor ein vierter Aufruf fehlschlägt. Der Client verfügt jetzt über die folgenden Optionen:

-   Abbrechen der Transaktion. In diesem Fall wird keiner der Filter hinzugefügt.
-   Committen der Transaktion. In diesem Fall werden die ersten drei Filter hinzugefügt.
-   Fortsetzen mit weiteren Vorgängen, einschließlich potenzieller Wiederholung des fehlerhaften [**FwpmFilterAdd0.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)

Beim Starten einer Transaktion wartet BFE, bis [**txnWaitTimeoutInMSec**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0) der Sitzung abläuft, um die Sperre zu erhalten. Wenn die Sperre nicht innerhalb dieser Zeit übernommen wird, kann die Sperrung (und der [**FwpmTransactionBegin0-Aufruf)**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) nicht verwendet werden. Dadurch wird verhindert, dass Clients unbegrenzt nicht reagieren. Wenn der Client kein Sperrzeitüberschreitung angegeben hat, beträgt der Standardwert 15 Sekunden.

Für jede Transaktion gilt auch ein Sperrzeitüberschreitungs-Timeout. Dies ist die maximale Zeitdauer, in der sie die Sperre besitzen kann. Wenn der Besitzer die Sperre nicht innerhalb dieser Zeit frei gibt, wird die Transaktion gesperrt, wodurch die Sperre freigegeben wird. Das Sperrzeitout kann nicht konfiguriert werden. Es ist unendlich für Aufrufer im Kernelmodus und eine Stunde für Aufrufer im Benutzermodus. Wenn eine Transaktion abgebrochen wird, wird beim nächsten Aufruf innerhalb dieser Transaktion ein Fehler mit **FWP \_ E \_ TXN \_ ABORTED angezeigt.**

## <a name="object-lifetimes"></a>Objektlebensdauer

Objekte können eine von vier möglichen Lebensdauern haben:

-   Dynamisch: Ein Objekt ist nur dynamisch, wenn es mithilfe eines dynamischen Sitzungshandpunkts hinzugefügt wird. Dynamische Objekte sind so lange leblos, bis sie gelöscht werden oder die besitzende Sitzung beendet wird.
-   Statisch – Objekte sind standardmäßig statisch. Statische Objekte werden geschaltet, bis sie gelöscht, BFE beendet oder das System heruntergefahren wird.
-   Persistent: Persistente Objekte werden erstellt, indem das entsprechende **Flag FWPM \_ \* \_ FLAG \_ PERSISTENT** an eine **Fwpm \* Add0-Funktion übergeben** wird. Persistente Objekte sind so lange leblos, bis sie gelöscht werden.
-   Integriert: Integrierte Objekte sind von BFE vordefiniert und können nicht hinzugefügt oder gelöscht werden. Sie leben für immer.

Filter in Kernelmodusebenen können als Startzeitfilter markiert werden, indem das entsprechende Flag an [**FwpmFilterAdd0 übergeben wird.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0) Startzeitfilter werden dem System hinzugefügt, wenn der TCP/IP-Treiber gestartet wird, und entfernt, wenn BFE die Initialisierung abgeschlossen hat. Persistente Objekte werden hinzugefügt, wenn BFE gestartet wird.

In vielen Fällen möchte ein Richtlinienanbieter seine persistente Richtlinie möglicherweise nicht erzwingen, wenn der Anbieter deaktiviert wurde. Beim Hinzufügen eines Anbieters kann der Aufrufer einen optionalen Windows angeben. Beim Hinzufügen persistenter Objekte kann der Aufrufer optional den Anbieter angeben, der dieses Objekt "besitzt". Beim Dienststart fügt BFE dem System nur persistente Objekte hinzu, wenn sie keinem Anbieter zugeordnet sind, der zugeordnete Anbieter keinen Windows-Dienstnamen hat oder der zugeordnete Windows-Dienst auf automatischen Start festgelegt ist.

## <a name="object-associations"></a>Objektzuordnungen

Einige Objekte verfügen über Verweise auf andere Objekte. Beispielsweise verweist ein Filter immer auf eine Ebene und kann auf eine Callout und einen Anbieterkontext verweisen. Objekte können nicht auf Objekte verweisen, die möglicherweise eine kürzere Lebensdauer haben. Daher kann ein dynamisches Objekt nicht auf ein dynamisches Objekt aus einer anderen Sitzung verweisen. Ein statisches Objekt kann nicht auf ein dynamisches Objekt verweisen. Ein persistentes Objekt kann nicht auf ein dynamisches Objekt, ein statisches Objekt oder ein persistentes Objekt verweisen, das sich im Besitz eines anderen Anbieters befindet.

Ein Objekt kann erst gelöscht werden, wenn alle Objekte, die darauf verweisen, zuerst gelöscht wurden.

## <a name="luids-and-guids"></a>LUIDs und GUIDs

Alle WFP-API-Objekte im Benutzermodus (FWPM) werden durch einen global eindeutigen Bezeichner **(GUID)** identifiziert und verweisen über ihre **GUID** auf andere Objekte. Die **GUID** muss nur innerhalb des Objekttyps eindeutig sein. Beispielsweise können ein Filter und ein Anbieterkontext dieselbe **GUID** haben, zwei Filter jedoch nicht. Wenn Sie ein neues -Objekt hinzufügen, können Aufrufer die **GUID** des Objekts zuweisen oder es nullinitialisiert lassen und BFE die **GUID zuweisen lassen.**

Alle WFP-API-Objekte im Kernelmodus (FWPS) werden durch einen lokal eindeutigen Bezeichner **(LUID)** identifiziert und verweisen über ihre LUID auf andere Objekte. Der Wechsel von **GUID** zu **LUID** ermöglicht es WFP, nicht seitenbasierte Pools zu sparen und die Laufzeitverarbeitung zu optimieren. Die Breite der **LUID** hängt vom Objekttyp ab und reicht von **UINT16** bis **UINT64.** **LUID-S** werden immer von BFE zugewiesen.

 

 