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
# <a name="com-administration-operations-within-transactions"></a><span data-ttu-id="95f59-103">Com+-Verwaltungsvorgänge in Transaktionen</span><span class="sxs-lookup"><span data-stu-id="95f59-103">COM+ Administration Operations Within Transactions</span></span>

<span data-ttu-id="95f59-104">Bei der COM+-Registrierungsdatenbank (RegDB) handelt es sich um einen transaktiven Ressourcen-Manager, der an com+-Transaktionen beteiligt sein kann.</span><span class="sxs-lookup"><span data-stu-id="95f59-104">The COM+ registration database (RegDB) is a transacted resource manager that can participate in COM+ transactions.</span></span> <span data-ttu-id="95f59-105">Auf diese Weise können Sie Verwaltungsvorgänge innerhalb einer Transaktion ausführen und alle Konfigurationsänderungen per Commit oder Abbruch als atomarer Vorgang ausführen, sogar über mehrere Computer hinweg.</span><span class="sxs-lookup"><span data-stu-id="95f59-105">This enables you to perform administration operations within a transaction and have all configuration changes committed or aborted as an atomic operation, even across multiple computers.</span></span> <span data-ttu-id="95f59-106">In einigen Fällen kann dies sehr vorteilhaft sein, obwohl es ein Isolierungs-und Blockierungs Verhalten gibt, das Sie berücksichtigen sollten, und die Ausführung von Verwaltungsaufgaben innerhalb von Transaktionen geringfügige Änderungen am normalen Verwaltungs Programmiermodell beinhaltet.</span><span class="sxs-lookup"><span data-stu-id="95f59-106">In some circumstances, it can be very beneficial to do this, although there is isolation and blocking behavior that you should take into account, and performing administration tasks within transactions does involve slight changes to the normal administration programming model.</span></span>

## <a name="benefits-of-doing-administration-operations-within-transactions"></a><span data-ttu-id="95f59-107">Vorteile der Ausführung von Verwaltungs Vorgängen in Transaktionen</span><span class="sxs-lookup"><span data-stu-id="95f59-107">Benefits of Doing Administration Operations Within Transactions</span></span>

-   <span data-ttu-id="95f59-108">**Konsistenz des Data –** Verwaltungsvorgänge, die innerhalb einer Transaktion ausgeführt werden, werden als Ganzes committet oder abgebrochen, obwohl einige nicht transaktionale com+-Katalog Ressourcen vorhanden sind, für die dies möglicherweise nicht der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="95f59-108">**Consistency of data—** Administration operations performed within a transaction are committed or aborted as a whole, although there are some non-transactional COM+ catalog resources for which this may not be the case.</span></span> <span data-ttu-id="95f59-109">(Weitere Informationen finden Sie weiter unten unter nicht transaktionale com+-Katalog Ressourcen.)</span><span class="sxs-lookup"><span data-stu-id="95f59-109">(See Non-Transactional COM+ Catalog Resources below.)</span></span>
-   <span data-ttu-id="95f59-110">**Konsistente Bereitstellung über mehrere Computer hinweg –** Wenn Sie com+-Anwendungen auf mehreren Servern bereitstellen, können Sie sicherstellen, dass alle Server mit identischen Konfigurationen verbleiben.</span><span class="sxs-lookup"><span data-stu-id="95f59-110">**Consistent deployment across multiple machines—** If you are deploying COM+ applications across multiple servers, you can guarantee that all servers are left with identical configurations.</span></span>
-   <span data-ttu-id="95f59-111">**Skalierung und Leistung –** Wenn Sie mehrere Vorgänge innerhalb einer Transaktion ausführen, werden alle Schreibvorgänge in RegDB gleichzeitig durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="95f59-111">**Scaling and performance—** When you do multiple operations within a transaction, all writes to RegDB are performed at once.</span></span> <span data-ttu-id="95f59-112">Persistente Schreibvorgänge in RegDB sind ein relativ kostspieliger Vorgang. Wenn Sie viele Schreibvorgänge in RegDB durchführen, können Sie einen großen Leistungsvorteil erzielen, indem Sie Sie auf einmal ausführen, statt jedes Mal, wenn Sie [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="95f59-112">Persisted writes to RegDB are a relatively expensive operation; if you are making many writes to RegDB, you can get a big performance benefit from doing them all at once instead of every time you call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges).</span></span>

## <a name="isolation-behavior-of-regdb"></a><span data-ttu-id="95f59-113">Isolations Verhalten von RegDB</span><span class="sxs-lookup"><span data-stu-id="95f59-113">Isolation Behavior of RegDB</span></span>

<span data-ttu-id="95f59-114">Um ordnungsgemäße Datenkonsistenz und serialisierbare Transaktionen sicherzustellen, erzwingt RegDB ein bestimmtes Blockierungs-und Isolations Verhalten, wenn Verwaltungsvorgänge in Transaktionen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="95f59-114">To ensure proper data consistency and serializable transactions, RegDB enforces particular blocking and isolation behavior when administration operations are being performed within transactions.</span></span>

<span data-ttu-id="95f59-115">Wenn eine Komponente, die innerhalb einer Transaktion ausgeführt wird, eine Methode aufruft, die einen Schreibvorgang in den com+-Katalog bewirkt – z. b. " [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)", " [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication)" oder " [**installcomponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent)" – wird eine Schreibsperre für den com+-Katalogserver Code übernommen, der alle anderen Writer blockiert, bis die aktuelle Transaktion ein Commit oder Abbruch durchführt.</span><span class="sxs-lookup"><span data-stu-id="95f59-115">Whenever a component that is doing work within a transaction calls any method that will cause a write to the COM+ catalog—such as [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication), or [**InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent)—a writer lock is taken on COM+ catalog server code that will block any other writers from coming in until the current transaction commits or aborts.</span></span> <span data-ttu-id="95f59-116">Das heißt, dass Writer nur dann eingehen können, wenn Sie über die richtige Transaktions Affinität verfügen und an der aktuellen Transaktion teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="95f59-116">That is, writers can come in only if they have the correct transaction affinity and are participating in the current transaction.</span></span>

<span data-ttu-id="95f59-117">Leser sind nicht blockiert.</span><span class="sxs-lookup"><span data-stu-id="95f59-117">Readers are not blocked.</span></span> <span data-ttu-id="95f59-118">Die Daten, die in den Lesern angezeigt werden, spiegeln jedoch keine zwischen Änderungen dar, die innerhalb der Transaktion vorgenommen wurden, bis die Transaktion tatsächlich einen Commit ausführt.</span><span class="sxs-lookup"><span data-stu-id="95f59-118">However, the data that readers see does not reflect any interim changes made within the transaction until that transaction actually commits.</span></span> <span data-ttu-id="95f59-119">Alle Komponenten, die an dieser Transaktion teilnehmen, sehen beim Lesen von Daten zwischen Daten Zuständen, aber alle Komponenten außerhalb der Transaktion sehen diese Änderungen erst, nachdem die Transaktion abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="95f59-119">Any components participating in that transaction sees interim data states when they read data, but all components outside the transaction see those changes only after the transaction has completed.</span></span>

## <a name="savechanges-behavior"></a><span data-ttu-id="95f59-120">SaveChanges-Verhalten</span><span class="sxs-lookup"><span data-stu-id="95f59-120">SaveChanges Behavior</span></span>

<span data-ttu-id="95f59-121">Um das oben beschriebene Isolations Verhalten zu erreichen, stellt RegDB effektiv einen Cache bereit, der von Komponenten innerhalb der Transaktion bearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="95f59-121">To achieve the isolation behavior described above, RegDB effectively provides a cache that is acted on by components within the transaction.</span></span> <span data-ttu-id="95f59-122">Dadurch wird das Verhalten der [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) -Methode geändert.</span><span class="sxs-lookup"><span data-stu-id="95f59-122">This changes the behavior of the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method.</span></span>

<span data-ttu-id="95f59-123">Normalerweise werden alle ausstehenden Änderungen, ohne dass eine Transaktion vorhanden ist, in den Katalog geschrieben, wenn Sie [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)aufzurufen, und **SaveChanges** gibt erst dann zurück, wenn alle Schreibvorgänge abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="95f59-123">Normally, without the presence of a transaction, any pending changes are written to the catalog when you call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), and **SaveChanges** doesn't return until all writes are completed.</span></span> <span data-ttu-id="95f59-124">Dadurch wird sichergestellt, dass bei erfolgreicher Rückgabe eines Aufrufens von **SaveChanges** [**startapplikation**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) aufgerufen werden kann, um die Anwendung mit neuen Daten zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="95f59-124">This guarantees that if a call to **SaveChanges** returns successfully, you can call [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) and it will activate the application with fresh data.</span></span>

<span data-ttu-id="95f59-125">Allerdings wirkt sich [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) innerhalb einer Transaktion nur auf den Cache aus, nicht auf RegDB selbst. **SaveChanges** gibt sofort zurück, ob alle Änderungen transaktional in RegDB übernommen wurden.</span><span class="sxs-lookup"><span data-stu-id="95f59-125">However, within a transaction, [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) affects only the cache, not the RegDB itself, and **SaveChanges** returns immediately whether all changes have been transactionally committed to RegDB.</span></span> <span data-ttu-id="95f59-126">Es gibt keine Garantie, dass bei der [**startapplikation**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) nach der Rückgabe von **SaveChanges** neue Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95f59-126">There is no guarantee that [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) is using fresh data subsequent to **SaveChanges** returning.</span></span> <span data-ttu-id="95f59-127">Wenn Sie in diesem Kontext **startapplikation** ausführen müssen, empfiehlt es sich, eine bestimmte Zeitspanne zu warten.</span><span class="sxs-lookup"><span data-stu-id="95f59-127">If you need to call **StartApplication** in this context, it is advisable to wait for some period of time before doing so.</span></span>

## <a name="transaction-time-out-period"></a><span data-ttu-id="95f59-128">Transaktions Time-Out Zeitraum</span><span class="sxs-lookup"><span data-stu-id="95f59-128">Transaction Time-Out Period</span></span>

<span data-ttu-id="95f59-129">Wenn Sie in einer Transaktion zahlreiche Verwaltungsvorgänge ausführen, kann dies eine Transaktion mit langer Laufzeit sein.</span><span class="sxs-lookup"><span data-stu-id="95f59-129">If you are doing numerous administration operations within a transaction, it may be a long running transaction.</span></span> <span data-ttu-id="95f59-130">In diesem Fall kann der Timeout Wert für Transaktionen ein Problem sein.</span><span class="sxs-lookup"><span data-stu-id="95f59-130">In this case, the transaction time-out value can be an issue.</span></span> <span data-ttu-id="95f59-131">Dies wird entweder durch den Transaktions Timeout Wert festgelegt, der für die Komponente festgelegt wurde, die die Transaktion initiiert, oder durch die Computer weite Timeout Einstellung für den Computer, auf dem die Komponente ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="95f59-131">This is determined either by the transaction time-out value set for the component initiating the transaction or by the machine-wide time-out setting for the machine where that component is running.</span></span> <span data-ttu-id="95f59-132">Wenn Sie in einer Transaktion zahlreiche Vorgänge durchlaufen, empfiehlt es sich, den entsprechenden Transaktions Timeout Zeitraum auf einen ausreichend langen Wert festzulegen und ggf. die ursprüngliche Einstellung wiederherzustellen, wenn Sie fertig sind.</span><span class="sxs-lookup"><span data-stu-id="95f59-132">If you are doing numerous operations within a transaction, it is advisable to set the appropriate transaction time-out period to a sufficiently long value and, if necessary, to restore the original setting when you are finished.</span></span>

## <a name="non-transactional-com-catalog-resources"></a><span data-ttu-id="95f59-133">Nicht transaktionale com+-Katalog Ressourcen</span><span class="sxs-lookup"><span data-stu-id="95f59-133">Non-Transactional COM+ Catalog Resources</span></span>

<span data-ttu-id="95f59-134">Die Registrierung, das Dateisystem und die Windows Installer (MSI) sind com+-Katalog Ressourcen, die nicht transaktional sind.</span><span class="sxs-lookup"><span data-stu-id="95f59-134">The registry, the file system, and Windows Installer (MSI) are COM+ catalog resources that are not transactional.</span></span>

> [!Note]  
> <span data-ttu-id="95f59-135">Wenn ein Fehler auftritt, der eine Transaktion abbricht, werden für Änderungen an diesen Ressourcen möglicherweise keine Rollbacks ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95f59-135">If there is an error that aborts a transaction, changes to these resources may not be rolled back.</span></span>

 

<span data-ttu-id="95f59-136">Wenn ein Fehler auftritt, während eine vorhandene COM+-Anwendung aus einer MSI-Datei installiert wird, wird die Anwendung nicht im Snap-in "Komponenten Dienste" angezeigt, Sie kann jedoch unter "Software" angezeigt werden. in diesem Fall müssen Sie Sie manuell entfernen.</span><span class="sxs-lookup"><span data-stu-id="95f59-136">If there is an error while installing an existing COM+ application from an .msi file, the application doesn't appear in the Component Services snap-in but it might appear in Add/Remove programs, in which case you need to manually remove it.</span></span>

## <a name="recovering-in-the-event-of-system-hangs"></a><span data-ttu-id="95f59-137">Wiederherstellung im Falle eines System aufhangs</span><span class="sxs-lookup"><span data-stu-id="95f59-137">Recovering in the Event of System Hangs</span></span>

<span data-ttu-id="95f59-138">Wenn eine Komponente, die Verwaltungsvorgänge innerhalb einer Transaktion durchführt, während der Ausführung einer Writer-Sperre im Katalogserver Code daran gehindert würde, alle anderen Änderungen am Katalog vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="95f59-138">If a component doing administration operations within a transaction were to hang while it holds a writer lock on the catalog server code, it would block everyone else from making any changes to the catalog.</span></span> <span data-ttu-id="95f59-139">Wenn dies der Fall ist, können Sie die Sperre für den Katalog löschen, indem Sie die System Anwendung Herunterfahren und neu starten.</span><span class="sxs-lookup"><span data-stu-id="95f59-139">Should this happen, you can clear the lock on the catalog by shutting down and restarting the System application.</span></span>

## <a name="scripting-with-a-transactioncontext-object"></a><span data-ttu-id="95f59-140">Skripterstellung mit einem transaktioncontext-Objekt</span><span class="sxs-lookup"><span data-stu-id="95f59-140">Scripting with a TransactionContext Object</span></span>

<span data-ttu-id="95f59-141">Eine einfache Möglichkeit zum Ausführen von Verwaltungs Vorgängen in Transaktionen ist die Verwendung eines [**transaktioncontext**](transactioncontext.md) -Objekts zum Steuern der Transaktion.</span><span class="sxs-lookup"><span data-stu-id="95f59-141">A simple way to do administration operations within transactions is to use a [**TransactionContext**](transactioncontext.md) object to control the transaction.</span></span> <span data-ttu-id="95f59-142">Beispielsweise wird im folgenden Visual Basic Skript veranschaulicht, wie zwei neue Anwendungen transaktional hinzugefügt werden, sodass entweder sowohl Anwendungen als auch keine der Anwendungen erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="95f59-142">For example, the following Visual Basic script demonstrates how to transactionally add two new applications so that either both applications or neither application is created:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="95f59-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="95f59-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95f59-144">Behandeln von com+-Verwaltungsfehlern</span><span class="sxs-lookup"><span data-stu-id="95f59-144">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="95f59-145">Einführ Endes Beispiel mit dem com+-Verwaltungs Katalog</span><span class="sxs-lookup"><span data-stu-id="95f59-145">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="95f59-146">Übersicht über die COMAdmin-Objekte</span><span class="sxs-lookup"><span data-stu-id="95f59-146">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="95f59-147">Abrufen von Auflistungen im com+-Katalog</span><span class="sxs-lookup"><span data-stu-id="95f59-147">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="95f59-148">Festlegen von Eigenschaften und Speichern von Änderungen am com+-Katalog</span><span class="sxs-lookup"><span data-stu-id="95f59-148">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



