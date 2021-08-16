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

Die COM+-Registrierungsdatenbank (RegDB) ist ein transaktiver Ressourcen-Manager, der an COM+-Transaktionen teilnehmen kann. Auf diese Weise können Sie Verwaltungsvorgänge innerhalb einer Transaktion ausführen und alle Konfigurationsänderungen selbst auf mehreren Computern als atomaren Vorgang übertragen oder abgebrochen werden. In einigen Fällen kann es sehr vorteilhaft sein, dies zu tun, obwohl Sie isolations- und blockierungsverhalten berücksichtigen sollten, und das Ausführen von Verwaltungsaufgaben innerhalb von Transaktionen bringt geringfügige Änderungen am normalen Verwaltungsprogrammiermodell mit sich.

## <a name="benefits-of-doing-administration-operations-within-transactions"></a>Vorteile von Verwaltungsvorgängen innerhalb von Transaktionen

-   **Datenkonsistenz:** Verwaltungsvorgänge, die innerhalb einer Transaktion ausgeführt werden, werden als Ganzes ausgeführt oder abgebrochen, obwohl es einige nicht transaktionale COM+-Katalogressourcen gibt, für die dies möglicherweise nicht der Fall ist. (Siehe nicht transaktionale COM+-Katalogressourcen weiter unten.)
-   **Konsistente Bereitstellung auf mehreren Computern:** Wenn Sie COM+-Anwendungen auf mehreren Servern bereitstellen, können Sie sicherstellen, dass alle Server identische Konfigurationen haben.
-   **Skalierung und Leistung:** Wenn Sie mehrere Vorgänge innerhalb einer Transaktion durchführen, werden alle Schreibvorgänge in RegDB gleichzeitig ausgeführt. Persistente Schreibvorgänge in RegDB sind ein relativ aufwendiger Vorgang. Wenn Sie viele Schreibvorgänge in RegDB durchführen, können Sie einen großen Leistungsvorteil erzielen, wenn Sie sie alle gleichzeitig durchführen, anstatt jedes Mal, wenn Sie [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)aufrufen.

## <a name="isolation-behavior-of-regdb"></a>Isolationsverhalten von RegDB

Um eine ordnungsgemäße Datenkonsistenz und serialisierbare Transaktionen sicherzustellen, erzwingt RegDB ein bestimmtes Blockierungs- und Isolationsverhalten, wenn Verwaltungsvorgänge innerhalb von Transaktionen ausgeführt werden.

Immer wenn eine Komponente, die innerhalb einer Transaktion arbeitet, eine Methode aufruft, die einen Schreibvorgang in den COM+-Katalog verursacht , z. B. [**SaveChanges,**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication)oder [**InstallComponent,**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent)wird eine Writersperre für COM+-Katalogservercode eingerichtet, die verhindert, dass alle anderen Writer eingehen, bis die aktuelle Transaktion committet oder abgebrochen wird. Das heißt, Writer können nur dann eintreffen, wenn sie über die richtige Transaktionsaffinität verfügen und an der aktuellen Transaktion teilnehmen.

Leser werden nicht blockiert. Die Daten, die lesern angezeigt werden, spiegeln jedoch keine Zwischenänderungen wider, die innerhalb der Transaktion vorgenommen wurden, bis diese Transaktion tatsächlich einen Commit ausgeführt hat. Alle Komponenten, die an dieser Transaktion teilnehmen, sehen Zwischendatenzustände, wenn sie Daten lesen, aber alle Komponenten außerhalb der Transaktion sehen diese Änderungen erst nach Abschluss der Transaktion.

## <a name="savechanges-behavior"></a>SaveChanges-Verhalten

Um das oben beschriebene Isolationsverhalten zu erreichen, stellt RegDB effektiv einen Cache bereit, auf den von Komponenten innerhalb der Transaktion reagiert wird. Dadurch wird das Verhalten der [**SaveChanges-Methode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) geändert.

Normalerweise werden alle ausstehenden Änderungen ohne Vorhandensein einer Transaktion in den Katalog geschrieben, wenn Sie [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)aufrufen, und **SaveChanges** gibt erst dann zurück, wenn alle Schreibvorgänge abgeschlossen sind. Dadurch wird sichergestellt, dass Sie [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) aufrufen können, wenn ein Aufruf von **SaveChanges** erfolgreich zurückgegeben wird, und die Anwendung mit neuen Daten aktiviert wird.

Innerhalb einer Transaktion wirkt sich [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) jedoch nur auf den Cache und nicht auf die RegDB selbst aus, und **SaveChanges** gibt sofort zurück, ob für alle Änderungen ein Commit an RegDB ausgeführt wurde. Es gibt keine Garantie dafür, dass [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) nach der Rückgabe von **SaveChanges** neue Daten verwendet. Wenn Sie **StartApplication** in diesem Kontext aufrufen müssen, ist es ratsam, einige Zeit zu warten, bevor Sie dies tun.

## <a name="transaction-time-out-period"></a>Transaktion Time-Out Zeitraum

Wenn Sie zahlreiche Verwaltungsvorgänge innerhalb einer Transaktion ausführen, kann es sich um eine Transaktion mit langer Ausführungslaufzeit handeln. In diesem Fall kann der Transaktionstime out-Wert ein Problem sein. Dies wird entweder durch den Transaktionstime out-Wert bestimmt, der für die Komponente festgelegt ist, die die Transaktion initiiert, oder durch die computerweite Time out-Einstellung für den Computer, auf dem diese Komponente ausgeführt wird. Wenn Sie zahlreiche Vorgänge innerhalb einer Transaktion ausführen, empfiehlt es sich, den entsprechenden Transaktionstime out-Zeitraum auf einen ausreichend langen Wert festzulegen und ggf. die ursprüngliche Einstellung wiederherzustellen, wenn Sie fertig sind.

## <a name="non-transactional-com-catalog-resources"></a>Nicht transaktionale COM+-Katalogressourcen

Die Registrierung, das Dateisystem und Windows Installer (MSI) sind COM+-Katalogressourcen, die nicht transaktional sind.

> [!Note]  
> Wenn ein Fehler auftritt, der eine Transaktion abbricht, wird für Änderungen an diesen Ressourcen möglicherweise kein Rollback ausgeführt.

 

Wenn beim Installieren einer vorhandenen COM+-Anwendung aus einer .msi-Datei ein Fehler auftritt, wird die Anwendung nicht im Komponentendienste-Snap-In angezeigt, aber möglicherweise unter Programme hinzufügen/entfernen. In diesem Fall müssen Sie sie manuell entfernen.

## <a name="recovering-in-the-event-of-system-hangs"></a>Wiederherstellung bei Systemhängen

Wenn eine Komponente, die Verwaltungsvorgänge innerhalb einer Transaktion vornimmt, hängen bleibt, während sie eine Writer-Sperre für den Katalogservercode enthält, würde sie alle anderen Benutzer daran hindern, Änderungen am Katalog vorzunehmen. In diesem Fall können Sie die Sperre für den Katalog deaktivieren, indem Sie die Systemanwendung herunterfahren und neu starten.

## <a name="scripting-with-a-transactioncontext-object"></a>Skripterstellung mit einem TransactionContext-Objekt

Eine einfache Möglichkeit zum Ausführen von Verwaltungsvorgängen innerhalb von Transaktionen ist die Verwendung eines [**TransactionContext-Objekts,**](transactioncontext.md) um die Transaktion zu steuern. Im folgenden Visual Basic Skript wird beispielsweise veranschaulicht, wie zwei neue Anwendungen transaktional hinzugefügt werden, sodass entweder beide Anwendungen oder keine Anwendung erstellt wird:


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

[Einführungsbeispiel für die Verwendung des COM+-Verwaltungskatalogs](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Übersicht über die COMAdmin-Objekte](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Abrufen von Sammlungen im COM+-Katalog](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Festlegen von Eigenschaften und Speichern von Änderungen im COM+-Katalog](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



