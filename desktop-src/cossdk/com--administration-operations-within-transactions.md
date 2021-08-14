---
description: COM+-Verwaltungsvorgänge innerhalb von Transaktionen
ms.assetid: 832f2e6d-26ff-416e-a92e-ebaa33d4e7e5
title: COM+-Verwaltungsvorgänge innerhalb von Transaktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4182b143de38d838aea7c5aabd2d91bdb84f94480b2bed4c4441e204412ac834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308249"
---
# <a name="com-administration-operations-within-transactions"></a>COM+-Verwaltungsvorgänge innerhalb von Transaktionen

Die COM+-Registrierungsdatenbank (RegDB) ist ein transaktiver Ressourcen-Manager, der an COM+-Transaktionen teilnehmen kann. Auf diese Weise können Sie Verwaltungsvorgänge innerhalb einer Transaktion ausführen und alle Konfigurationsänderungen als atomaren Vorgang ausführen oder abbrechen, auch auf mehreren Computern. In einigen Fällen kann es sehr vorteilhaft sein, dies zu tun, obwohl es Isolations- und Blockierungsverhalten gibt, das Sie berücksichtigen sollten, und das Ausführen von Verwaltungsaufgaben innerhalb von Transaktionen umfasst geringfügige Änderungen am normalen Verwaltungsprogrammiermodell.

## <a name="benefits-of-doing-administration-operations-within-transactions"></a>Vorteile von Verwaltungsvorgängen innerhalb von Transaktionen

-   **Konsistenz der Daten–** Verwaltungsvorgänge, die innerhalb einer Transaktion ausgeführt werden, werden als Ganzes ausgeführt oder abgebrochen, obwohl es einige nicht transaktionale COM+-Katalogressourcen gibt, für die dies möglicherweise nicht der Fall ist. (Siehe nicht transaktionale COM+-Katalogressourcen weiter unten.)
-   **Konsistente Bereitstellung auf mehreren Computern–** Wenn Sie COM+-Anwendungen auf mehreren Servern bereitstellen, können Sie garantieren, dass alle Server identische Konfigurationen haben.
-   **Skalierung und Leistung–** Wenn Sie mehrere Vorgänge innerhalb einer Transaktion ausführen, werden alle Schreibvorgänge in RegDB gleichzeitig ausgeführt. Persistente Schreibvorgänge in RegDB sind relativ aufwändig. Wenn Sie viele Schreibvorgänge in RegDB ausführen, können Sie einen großen Leistungsvorteil erzielen, wenn Sie alle gleichzeitig ausführen, anstatt jedes Mal, wenn [**Sie SaveChanges aufrufen.**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)

## <a name="isolation-behavior-of-regdb"></a>Isolationsverhalten von RegDB

Um eine ordnungsgemäße Datenkonsistenz und serialisierbare Transaktionen sicherzustellen, erzwingt RegDB ein bestimmtes Blockierungs- und Isolationsverhalten, wenn Verwaltungsvorgänge innerhalb von Transaktionen ausgeführt werden.

Jedes Mal, wenn eine Komponente, die innerhalb einer Transaktion arbeitet, eine Methode aufruft, die einen Schreibzugriff auf den COM+-Katalog verursacht , z. B. [**SaveChanges,**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication)oder [**InstallComponent,**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent)wird eine Writersperre für COM+-Katalogservercode verwendet, der das Einlassen anderer Writer blockiert, bis die aktuelle Transaktion commits oder abbricht. Das heißt, Writer können nur in kommen, wenn sie über die richtige Transaktionsaffinität verfügen und an der aktuellen Transaktion teilnehmen.

Leser werden nicht blockiert. Die Daten, die Lesern angezeigt werden, spiegeln jedoch keine Zwischenänderungen wider, die innerhalb der Transaktion vorgenommen wurden, bis diese Transaktion tatsächlich einen Commit ausgeführt hat. Alle An dieser Transaktion beteiligten Komponenten sehen beim Lesen von Daten Zwischendatenzustände, aber alle Komponenten außerhalb der Transaktion sehen diese Änderungen erst, nachdem die Transaktion abgeschlossen wurde.

## <a name="savechanges-behavior"></a>SaveChanges-Verhalten

Um das oben beschriebene Isolationsverhalten zu erreichen, stellt RegDB effektiv einen Cache zur Anwendung, der von Komponenten innerhalb der Transaktion ausgeführt wird. Dadurch wird das Verhalten der [**SaveChanges-Methode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) geändert.

Normalerweise werden alle ausstehenden Änderungen ohne das Vorhandensein einer Transaktion in den Katalog geschrieben, wenn Sie [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)aufrufen, und **SaveChanges** gibt erst dann zurück, wenn alle Schreibvorgänge abgeschlossen sind. Dadurch wird sichergestellt, dass Sie [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) aufrufen können, wenn ein Aufruf von **SaveChanges** erfolgreich zurückgegeben wird, und die Anwendung mit neuen Daten aktiviert wird.

Innerhalb einer Transaktion wirkt sich [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) jedoch nur auf den Cache aus, nicht auf die RegDB selbst, und **SaveChanges** gibt sofort zurück, ob alle Änderungen transaktional in RegDB übertragen wurden. Es gibt keine Garantie, [**dass StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) nach der Rückgabe von **SaveChanges** neue Daten verwendet. Wenn Sie in diesem Kontext **StartApplication** aufrufen müssen, ist es ratsam, einige Zeit zu warten, bevor Sie dies tun.

## <a name="transaction-time-out-period"></a>Transaktionszeit Time-Out Zeitraum

Wenn Sie innerhalb einer Transaktion zahlreiche Verwaltungsvorgänge ausführen, kann es sich um eine Transaktion mit langer Ausführungslauf handelt. In diesem Fall kann der Wert für das Transaktions-Time out ein Problem sein. Dies wird entweder durch den Transaktions-Time out-Wert bestimmt, der für die Komponente festgelegt wurde, die die Transaktion initiiert, oder durch die computerweite Time out-Einstellung für den Computer, auf dem diese Komponente ausgeführt wird. Wenn Sie innerhalb einer Transaktion zahlreiche Vorgänge unternehmen, ist es ratsam, den entsprechenden Time outzeitraum für Transaktionen auf einen ausreichend langen Wert zu setzen und bei Bedarf die ursprüngliche Einstellung wiederherzustellen, wenn Sie fertig sind.

## <a name="non-transactional-com-catalog-resources"></a>Nicht transaktionale COM+-Katalogressourcen

Die Registrierung, das Dateisystem und Windows Installer (MSI) sind COM+-Katalogressourcen, die nicht transaktional sind.

> [!Note]  
> Wenn ein Fehler auftritt, der eine Transaktion abbricht, wird für Änderungen an diesen Ressourcen möglicherweise kein Rollback ausgeführt.

 

Wenn beim Installieren einer vorhandenen COM+-Anwendung aus einer .msi-Datei ein Fehler auftritt, wird die Anwendung nicht im Komponentendienste-Snap-In angezeigt. Sie wird jedoch möglicherweise unter Softwareprogramme hinzufügen/entfernen angezeigt. In diesem Fall müssen Sie sie manuell entfernen.

## <a name="recovering-in-the-event-of-system-hangs"></a>Wiederherstellung bei Hängen des Systems

Wenn eine Komponente, die Verwaltungsvorgänge innerhalb einer Transaktion ausgeführt hat, nicht mehr reagieren würde, während sie eine Writersperre für den Katalogservercode auftrat, würde sie alle anderen am Vornehmen von Änderungen am Katalog blockieren. In diesem Fall können Sie die Sperre für den Katalog löschen, indem Sie die Systemanwendung herunterfahren und neu starten.

## <a name="scripting-with-a-transactioncontext-object"></a>Skripterstellung mit einem TransactionContext-Objekt

Eine einfache Möglichkeit zum Durchführen von Verwaltungsvorgängen innerhalb von Transaktionen ist die Verwendung eines [**TransactionContext-Objekts**](transactioncontext.md) zum Steuern der Transaktion. Das folgende Skript Visual Basic veranschaulicht beispielsweise, wie zwei neue Anwendungen transaktional hinzugefügt werden, sodass entweder beide Anwendungen oder keine Anwendung erstellt wird:


```VB
Dim txctx
Dim cat
Dim apps
Dim app1
Dim app2
  
WScript.Echo "Starting"
Set txctx = CreateObject("TxCtx.TransactionContext")
Set cat = txctx.CreateInstance("COMAdmin.COMAdminCatalog")
Set apps = cat.GetCollection("Applications")
Set app1 = apps.Add
app1.Value("Name") = "Test App #1"
apps.SaveChanges
Set app2 = apps.Add
app2.Value("Name") = "Test App #2"
apps.SaveChanges
  
WScript.Echo "Ending"
txctx.Commit

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Behandeln von COM+-Verwaltungsfehlern](handling-com--administration-errors.md)
</dt> <dt>

[Einführendes Beispiel mit dem COM+-Verwaltungskatalog](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Übersicht über die COMAdmin-Objekte](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Abrufen von Sammlungen im COM+-Katalog](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Festlegen von Eigenschaften und Speichern von Änderungen am COM+-Katalog](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



