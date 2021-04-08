---
description: Com+-Verwaltungsvorgänge in Transaktionen
ms.assetid: 832f2e6d-26ff-416e-a92e-ebaa33d4e7e5
title: Com+-Verwaltungsvorgänge in Transaktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21612ffec1b9f082dc6a91861882a71f18fb07be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749096"
---
# <a name="com-administration-operations-within-transactions"></a>Com+-Verwaltungsvorgänge in Transaktionen

Bei der COM+-Registrierungsdatenbank (RegDB) handelt es sich um einen transaktiven Ressourcen-Manager, der an com+-Transaktionen beteiligt sein kann. Auf diese Weise können Sie Verwaltungsvorgänge innerhalb einer Transaktion ausführen und alle Konfigurationsänderungen per Commit oder Abbruch als atomarer Vorgang ausführen, sogar über mehrere Computer hinweg. In einigen Fällen kann dies sehr vorteilhaft sein, obwohl es ein Isolierungs-und Blockierungs Verhalten gibt, das Sie berücksichtigen sollten, und die Ausführung von Verwaltungsaufgaben innerhalb von Transaktionen geringfügige Änderungen am normalen Verwaltungs Programmiermodell beinhaltet.

## <a name="benefits-of-doing-administration-operations-within-transactions"></a>Vorteile der Ausführung von Verwaltungs Vorgängen in Transaktionen

-   **Konsistenz des Data –** Verwaltungsvorgänge, die innerhalb einer Transaktion ausgeführt werden, werden als Ganzes committet oder abgebrochen, obwohl einige nicht transaktionale com+-Katalog Ressourcen vorhanden sind, für die dies möglicherweise nicht der Fall ist. (Weitere Informationen finden Sie weiter unten unter nicht transaktionale com+-Katalog Ressourcen.)
-   **Konsistente Bereitstellung über mehrere Computer hinweg –** Wenn Sie com+-Anwendungen auf mehreren Servern bereitstellen, können Sie sicherstellen, dass alle Server mit identischen Konfigurationen verbleiben.
-   **Skalierung und Leistung –** Wenn Sie mehrere Vorgänge innerhalb einer Transaktion ausführen, werden alle Schreibvorgänge in RegDB gleichzeitig durchgeführt. Persistente Schreibvorgänge in RegDB sind ein relativ kostspieliger Vorgang. Wenn Sie viele Schreibvorgänge in RegDB durchführen, können Sie einen großen Leistungsvorteil erzielen, indem Sie Sie auf einmal ausführen, statt jedes Mal, wenn Sie [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)aufzurufen.

## <a name="isolation-behavior-of-regdb"></a>Isolations Verhalten von RegDB

Um ordnungsgemäße Datenkonsistenz und serialisierbare Transaktionen sicherzustellen, erzwingt RegDB ein bestimmtes Blockierungs-und Isolations Verhalten, wenn Verwaltungsvorgänge in Transaktionen durchgeführt werden.

Wenn eine Komponente, die innerhalb einer Transaktion ausgeführt wird, eine Methode aufruft, die einen Schreibvorgang in den com+-Katalog bewirkt – z. b. " [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)", " [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication)" oder " [**installcomponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent)" – wird eine Schreibsperre für den com+-Katalogserver Code übernommen, der alle anderen Writer blockiert, bis die aktuelle Transaktion ein Commit oder Abbruch durchführt. Das heißt, dass Writer nur dann eingehen können, wenn Sie über die richtige Transaktions Affinität verfügen und an der aktuellen Transaktion teilnehmen.

Leser sind nicht blockiert. Die Daten, die in den Lesern angezeigt werden, spiegeln jedoch keine zwischen Änderungen dar, die innerhalb der Transaktion vorgenommen wurden, bis die Transaktion tatsächlich einen Commit ausführt. Alle Komponenten, die an dieser Transaktion teilnehmen, sehen beim Lesen von Daten zwischen Daten Zuständen, aber alle Komponenten außerhalb der Transaktion sehen diese Änderungen erst, nachdem die Transaktion abgeschlossen wurde.

## <a name="savechanges-behavior"></a>SaveChanges-Verhalten

Um das oben beschriebene Isolations Verhalten zu erreichen, stellt RegDB effektiv einen Cache bereit, der von Komponenten innerhalb der Transaktion bearbeitet wird. Dadurch wird das Verhalten der [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) -Methode geändert.

Normalerweise werden alle ausstehenden Änderungen, ohne dass eine Transaktion vorhanden ist, in den Katalog geschrieben, wenn Sie [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)aufzurufen, und **SaveChanges** gibt erst dann zurück, wenn alle Schreibvorgänge abgeschlossen sind. Dadurch wird sichergestellt, dass bei erfolgreicher Rückgabe eines Aufrufens von **SaveChanges** [**startapplikation**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) aufgerufen werden kann, um die Anwendung mit neuen Daten zu aktivieren.

Allerdings wirkt sich [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) innerhalb einer Transaktion nur auf den Cache aus, nicht auf RegDB selbst. **SaveChanges** gibt sofort zurück, ob alle Änderungen transaktional in RegDB übernommen wurden. Es gibt keine Garantie, dass bei der [**startapplikation**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) nach der Rückgabe von **SaveChanges** neue Daten verwendet werden. Wenn Sie in diesem Kontext **startapplikation** ausführen müssen, empfiehlt es sich, eine bestimmte Zeitspanne zu warten.

## <a name="transaction-time-out-period"></a>Transaktions Time-Out Zeitraum

Wenn Sie in einer Transaktion zahlreiche Verwaltungsvorgänge ausführen, kann dies eine Transaktion mit langer Laufzeit sein. In diesem Fall kann der Timeout Wert für Transaktionen ein Problem sein. Dies wird entweder durch den Transaktions Timeout Wert festgelegt, der für die Komponente festgelegt wurde, die die Transaktion initiiert, oder durch die Computer weite Timeout Einstellung für den Computer, auf dem die Komponente ausgeführt wird. Wenn Sie in einer Transaktion zahlreiche Vorgänge durchlaufen, empfiehlt es sich, den entsprechenden Transaktions Timeout Zeitraum auf einen ausreichend langen Wert festzulegen und ggf. die ursprüngliche Einstellung wiederherzustellen, wenn Sie fertig sind.

## <a name="non-transactional-com-catalog-resources"></a>Nicht transaktionale com+-Katalog Ressourcen

Die Registrierung, das Dateisystem und die Windows Installer (MSI) sind com+-Katalog Ressourcen, die nicht transaktional sind.

> [!Note]  
> Wenn ein Fehler auftritt, der eine Transaktion abbricht, werden für Änderungen an diesen Ressourcen möglicherweise keine Rollbacks ausgeführt.

 

Wenn ein Fehler auftritt, während eine vorhandene COM+-Anwendung aus einer MSI-Datei installiert wird, wird die Anwendung nicht im Snap-in "Komponenten Dienste" angezeigt, Sie kann jedoch unter "Software" angezeigt werden. in diesem Fall müssen Sie Sie manuell entfernen.

## <a name="recovering-in-the-event-of-system-hangs"></a>Wiederherstellung im Falle eines System aufhangs

Wenn eine Komponente, die Verwaltungsvorgänge innerhalb einer Transaktion durchführt, während der Ausführung einer Writer-Sperre im Katalogserver Code daran gehindert würde, alle anderen Änderungen am Katalog vorzunehmen. Wenn dies der Fall ist, können Sie die Sperre für den Katalog löschen, indem Sie die System Anwendung Herunterfahren und neu starten.

## <a name="scripting-with-a-transactioncontext-object"></a>Skripterstellung mit einem transaktioncontext-Objekt

Eine einfache Möglichkeit zum Ausführen von Verwaltungs Vorgängen in Transaktionen ist die Verwendung eines [**transaktioncontext**](transactioncontext.md) -Objekts zum Steuern der Transaktion. Beispielsweise wird im folgenden Visual Basic Skript veranschaulicht, wie zwei neue Anwendungen transaktional hinzugefügt werden, sodass entweder sowohl Anwendungen als auch keine der Anwendungen erstellt werden:


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

[Behandeln von com+-Verwaltungsfehlern](handling-com--administration-errors.md)
</dt> <dt>

[Einführ Endes Beispiel mit dem com+-Verwaltungs Katalog](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Übersicht über die COMAdmin-Objekte](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Abrufen von Auflistungen im com+-Katalog](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Festlegen von Eigenschaften und Speichern von Änderungen am com+-Katalog](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



