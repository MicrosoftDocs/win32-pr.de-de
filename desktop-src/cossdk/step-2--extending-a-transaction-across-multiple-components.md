---
description: 'Schritt 2: Erweitern einer Transaktion über mehrere Komponenten hinweg'
ms.assetid: 20a30e87-e209-45ae-bf1b-722568758c47
title: 'Schritt 2: Erweitern einer Transaktion über mehrere Komponenten hinweg'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c6fc80016904a3ea51b7aea7fa0ec93edc47a6
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104350938"
---
# <a name="step-2-extending-a-transaction-across-components"></a><span data-ttu-id="56207-103">Schritt 2: Erweitern einer Transaktion über Komponenten hinweg</span><span class="sxs-lookup"><span data-stu-id="56207-103">Step 2: Extending a Transaction Across Components</span></span>

## <a name="objectives"></a><span data-ttu-id="56207-104">Ziele</span><span class="sxs-lookup"><span data-stu-id="56207-104">Objectives</span></span>

<span data-ttu-id="56207-105">In diesem Schritt erfahren Sie mehr über Folgendes:</span><span class="sxs-lookup"><span data-stu-id="56207-105">In this step, you will learn about the following:</span></span>

-   <span data-ttu-id="56207-106">Transaktions Fluss</span><span class="sxs-lookup"><span data-stu-id="56207-106">Transaction flow</span></span>
-   <span data-ttu-id="56207-107">Abstimmen von mehreren Objekten in einer Transaktion</span><span class="sxs-lookup"><span data-stu-id="56207-107">How multiple objects vote in a transaction</span></span>

## <a name="description"></a><span data-ttu-id="56207-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56207-108">Description</span></span>

<span data-ttu-id="56207-109">[Schritt 1: Erstellen einer transaktionalen Komponente](step-1--creating-a-transactional-component.md) zeigt, wie Sie eine einfache Transaktions Komponente schreiben, die Autoreninformationen in der Microsoft SQL Server pubs-Datenbank aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="56207-109">[Step 1: Creating a Transactional Component](step-1--creating-a-transactional-component.md) shows how to write a simple transactional component that updates author information in the Microsoft SQL Server Pubs database.</span></span> <span data-ttu-id="56207-110">Schritt 2 zeigt, was geschieht, wenn eine Transaktion über mehrere Komponenten hinweg erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="56207-110">Step 2 shows what happens when a transaction is extended across multiple components.</span></span>

<span data-ttu-id="56207-111">Unter Beibehaltung des com+-Programmiermodells `UpdateAuthorAddress` Ruft eine andere Komponente im Verlauf der Arbeit auf.</span><span class="sxs-lookup"><span data-stu-id="56207-111">In keeping with the COM+ programming model, `UpdateAuthorAddress` calls another component in the course of completing its work.</span></span> <span data-ttu-id="56207-112">Die zweite Komponente, `ValidateAuthorAddress` , überprüft die Adresse des Autors und gibt die Ergebnisse an den Aufrufer zurück `UpdateAuthorAddress` .</span><span class="sxs-lookup"><span data-stu-id="56207-112">The second component, `ValidateAuthorAddress`, validates the author's address and returns the results to its caller, `UpdateAuthorAddress`.</span></span>

<span data-ttu-id="56207-113">Im Gegensatz zum Aufrufer ist `ValidateAuthorAddress` keine Transaktion erforderlich, kann aber dennoch an der Transaktion des Aufrufers teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="56207-113">Unlike its caller, `ValidateAuthorAddress` does not require a transaction, but it can still participate in its caller's transaction.</span></span> <span data-ttu-id="56207-114">In diesem Schritt wird der Wert des Transaktions Attributs auf **unterstützt** festgelegt, wie in der folgenden Abbildung gezeigt, die die vorhandene Transaktion auf das neue Objekt erweitert.</span><span class="sxs-lookup"><span data-stu-id="56207-114">In this step, its transaction attribute value is set to **Supported**, as shown in the following illustration, which extends the existing transaction to the new object.</span></span>

![Diagramm, das die Erweiterung der vorhandenen Transaktion auf das neue Objekt anzeigt.](images/f58acb34-55db-40a4-8c48-f51ad024ff7e.png)

<span data-ttu-id="56207-116">Der **unterstützte** Attribut Wert erweitert (oder fließt) eine vorhandene Transaktion nur, wenn der Aufrufer transaktional ist.</span><span class="sxs-lookup"><span data-stu-id="56207-116">The **Supported** attribute value extends (or flows) an existing transaction only when the caller is transactional.</span></span> <span data-ttu-id="56207-117">Bei `UpdateAuthorAddress` Aufrufen von `ValidateAuthorAddress` prüft com+ zuerst den Kontext des Aufrufers, um zu sehen, ob er transaktional ist.</span><span class="sxs-lookup"><span data-stu-id="56207-117">When `UpdateAuthorAddress` calls `ValidateAuthorAddress`, COM+ first looks at the caller's context to see whether it is transactional.</span></span> <span data-ttu-id="56207-118">Com+ prüft dann die Dienst Attribute, die für festgelegt sind, `ValidateAuthorAddress` und weist das neue-Objekt dem gleichen Transaktions Bezeichner zu, der dem Aufruferobjekt zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="56207-118">COM+ then looks at the service attributes that are set on `ValidateAuthorAddress` and assigns the new object the same transaction identifier that is assigned to the caller object.</span></span> <span data-ttu-id="56207-119">Informationen zum besseren Verständnis dieses Prozesses finden Sie unter [Kontext Aktivierung](context-activation.md).</span><span class="sxs-lookup"><span data-stu-id="56207-119">To better understand this process, see [Context Activation](context-activation.md).</span></span>

<span data-ttu-id="56207-120">Da Sie denselben Transaktions Bezeichner gemeinsam nutzen, müssen beide Objekte ihre Arbeit erfolgreich abgeschlossen haben, oder com+ bricht die Transaktion ab (macht Änderungen an der pubs-Datenbank nicht mehr erforderlich).</span><span class="sxs-lookup"><span data-stu-id="56207-120">Because they share the same transaction identifier, both objects must complete their work successfully or COM+ aborts the transaction (undoing any changes made to the Pubs database).</span></span>

<span data-ttu-id="56207-121">Alle Objekte, die an einer Transaktion teilnehmen, Stimmen ab, um die Transaktion zu committen oder abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="56207-121">All objects participating in a transaction vote to either commit or abort the transaction.</span></span> <span data-ttu-id="56207-122">Die Abstimmung erfolgt explizit, wenn Sie Abstimmungsanweisungen in Ihren Code einschließen, wie in der folgenden Extraktion aus dem Schritt 1-Beispielcode gezeigt, der die- `UpdateAuthorAddress` Komponente erstellt:</span><span class="sxs-lookup"><span data-stu-id="56207-122">Voting occurs explicitly when you include voting instructions in your code, as shown in the following extraction from the Step 1 Sample Code, which creates the `UpdateAuthorAddress` component:</span></span>


```VB
  ' Everything works.
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn True
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
```



<span data-ttu-id="56207-123">Die Abstimmung erfolgt auch implizit, wie es in der Komponente der Fall ist `ValidateAuthorAddress` .</span><span class="sxs-lookup"><span data-stu-id="56207-123">Voting also occurs implicitly, as is done in the `ValidateAuthorAddress` component.</span></span> <span data-ttu-id="56207-124">Wenn das-Objekt nicht anderweitig deklariert, geht com+ davon aus, dass ein Objekt seine Arbeit erfolgreich abgeschlossen hat, aber nicht für die Deaktivierung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="56207-124">Unless the object declares otherwise, COM+ assumes an object has completed its work successfully but that it is not ready to be deactivated.</span></span> <span data-ttu-id="56207-125">Com+ nimmt die folgende Annahme an:</span><span class="sxs-lookup"><span data-stu-id="56207-125">COM+ makes the following assumption:</span></span>


```VB
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn False
```



<span data-ttu-id="56207-126">Wenn `ValidateAuthorAddress` an seinen Aufrufer zurückkehrt, liest com+ seine Stimme als Commit.</span><span class="sxs-lookup"><span data-stu-id="56207-126">When `ValidateAuthorAddress` returns to its caller, COM+ reads its vote as a commit.</span></span> <span data-ttu-id="56207-127">Com+ zählt die Stimmen erst, wenn das Stamm Objekt deaktiviert wird, das das erste Objekt in der Transaktion ist, in diesem Fall das- `UpdateAuthorAddress` Objekt.</span><span class="sxs-lookup"><span data-stu-id="56207-127">COM+ doesn't count the votes until it deactivates the root object, which is the first object in the transaction in this case, the `UpdateAuthorAddress` object.</span></span>

## <a name="sample-code"></a><span data-ttu-id="56207-128">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="56207-128">Sample code</span></span>

<span data-ttu-id="56207-129">Die `ValidateAuthorAddress` Komponente führt eine einfache Überprüfung der Adresse des Autors durch.</span><span class="sxs-lookup"><span data-stu-id="56207-129">The `ValidateAuthorAddress` component makes a simple check of the author's address.</span></span> <span data-ttu-id="56207-130">Da `UpdateAuthorAddress` nicht explizit abgestimmt, verwendet com+ die standardmäßigen Abstimmungs Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="56207-130">Because `UpdateAuthorAddress` does not vote explicitly, COM+ uses the default vote settings.</span></span>


```VB
Option Explicit
'
'   Purpose:   This class is used for validating an author's address
'              (presumably right before updating that address in the
'              database).
'
'   Notes:   This component could be in a transaction or not; it doesn't 
'            matter because it doesn't touch any data in a database.
'
Public Function ValidateAuthorAddress( _
                        ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String) As Boolean
  ' Default is to validate unless something is found to be wrong.
  ValidateAuthorAddress = True
                                                  
  '  Invalidate authors who live in New York City
  '  and authors who live in Montana.
  '
  If strCity = "New York" And strState = "New York" Then
    ValidateAuthorAddress = False
  ElseIf strState = "Montana" Then
    ValidateAuthorAddress = False
  End If
  ' Done
End Function
```



## <a name="summary"></a><span data-ttu-id="56207-131">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="56207-131">Summary</span></span>

-   <span data-ttu-id="56207-132">Das Festlegen des Transaktions Attributs für eine Komponente auf " **unterstützt** " kann dazu führen, dass das neue Objekt in der Transaktion des aufrufenden Objekts erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="56207-132">Setting a component's transaction attribute to **Supported** can result in the new object being created in the calling object's transaction.</span></span> <span data-ttu-id="56207-133">Com+ prüft den Kontext des Aufrufers, um den Transaktionsstatus des neuen Objekts zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="56207-133">COM+ looks at the caller's context to determine the transactional status of the new object.</span></span> <span data-ttu-id="56207-134">Wenn der Aufrufer transaktional ist, fließt com+ die Transaktion an das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="56207-134">If the caller is transactional, COM+ flows the transaction to the new object.</span></span>
-   <span data-ttu-id="56207-135">Alle Objekte, die an derselben Transaktion teilnehmen, haben eine gemeinsame Transaktions-ID, die von com+ aus dem Kontext des Objekts gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="56207-135">All objects participating in the same transaction share a common transaction identifier, which COM+ reads from the object's context.</span></span>
-   <span data-ttu-id="56207-136">Jedes Objekt in einer Transaktion Stimmen unabhängig von anderen Objekten ab.</span><span class="sxs-lookup"><span data-stu-id="56207-136">Each object in a transaction votes independently of other objects.</span></span> <span data-ttu-id="56207-137">Com+ zählt die Stimmen, wenn das Stamm Objekt deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="56207-137">COM+ counts the votes when the root object is deactivated.</span></span>
-   <span data-ttu-id="56207-138">Sie können die Transaktions Stimme eines Objekts zwischen Commit und Abbrechen umschalten, bis com+ das Objekt deaktiviert oder das Stamm Objekt von com+ deaktiviert und die Transaktion beendet wird.</span><span class="sxs-lookup"><span data-stu-id="56207-138">You can toggle an object's transaction vote between commit and abort until COM+ deactivates the object or until COM+ deactivates the root object and ends the transaction.</span></span> <span data-ttu-id="56207-139">Nur die Einstellung für die letzte Stimme wird gezählt.</span><span class="sxs-lookup"><span data-stu-id="56207-139">Only the last vote setting counts.</span></span> <span data-ttu-id="56207-140">Die Schnittstellen [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) und [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) stellen Methoden bereit, die ähnliche Abstimmungsergebnisse wie in der folgenden Tabelle dargestellt erstellen.</span><span class="sxs-lookup"><span data-stu-id="56207-140">The [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) and [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) interfaces provide methods and that produce similar voting results as shown in the following table.</span></span> <span data-ttu-id="56207-141">Sie können beide Schnittstellen verwenden, um in einer Transaktion explizit abzustimmen.</span><span class="sxs-lookup"><span data-stu-id="56207-141">You can use either interface to vote explicitly in a transaction.</span></span> 

    | <span data-ttu-id="56207-142">[**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) -Kombinations Methoden</span><span class="sxs-lookup"><span data-stu-id="56207-142">[**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) combination methods</span></span>                                                                                                                                                      | <span data-ttu-id="56207-143">[**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) -äquivalente Methode</span><span class="sxs-lookup"><span data-stu-id="56207-143">[**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) equivalent method</span></span>       |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
    | <span data-ttu-id="56207-144">[**Setmytransaktionvote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txvote*-  =  **txcommit**</span><span class="sxs-lookup"><span data-stu-id="56207-144">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxCommit**</span></span><br/> <span data-ttu-id="56207-145">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeaktivieren*  =  **true**</span><span class="sxs-lookup"><span data-stu-id="56207-145">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **True**</span></span><br/>  | [<span data-ttu-id="56207-146">**SetComplete**</span><span class="sxs-lookup"><span data-stu-id="56207-146">**SetComplete**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     |
    | <span data-ttu-id="56207-147">[**Setmytransaktionvote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txvote*-  =  **txcommit**</span><span class="sxs-lookup"><span data-stu-id="56207-147">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxCommit**</span></span><br/> <span data-ttu-id="56207-148">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeaktivieren*  =  **false**</span><span class="sxs-lookup"><span data-stu-id="56207-148">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **False**</span></span><br/> | [<span data-ttu-id="56207-149">**EnableCommit**</span><span class="sxs-lookup"><span data-stu-id="56207-149">**EnableCommit**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   |
    | <span data-ttu-id="56207-150">[**Setmytransaktionvote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txvote*  =  **txabort**</span><span class="sxs-lookup"><span data-stu-id="56207-150">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxAbort**</span></span><br/> <span data-ttu-id="56207-151">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeaktivieren*  =  **true**</span><span class="sxs-lookup"><span data-stu-id="56207-151">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **True**</span></span><br/>   | [<span data-ttu-id="56207-152">**SetAbort**</span><span class="sxs-lookup"><span data-stu-id="56207-152">**SetAbort**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           |
    | <span data-ttu-id="56207-153">[**Setmytransaktionvote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txvote*  =  **txabort**</span><span class="sxs-lookup"><span data-stu-id="56207-153">[**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = **TxAbort**</span></span><br/> <span data-ttu-id="56207-154">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeaktivieren*  =  **false**</span><span class="sxs-lookup"><span data-stu-id="56207-154">[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = **False**</span></span><br/>  | [<span data-ttu-id="56207-155">**DisableCommit**</span><span class="sxs-lookup"><span data-stu-id="56207-155">**DisableCommit**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> |

    

     

-   <span data-ttu-id="56207-156">Com+ legt die Stimme eines Objekts auf das Äquivalent von [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) fest, es sei denn, die Komponente stimmt explizit überein.</span><span class="sxs-lookup"><span data-stu-id="56207-156">COM+ sets an object's vote to the equivalent of [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) unless the component votes explicitly.</span></span>
-   <span data-ttu-id="56207-157">Wenn Sie explizit abstimmen, kann die Gesamtdauer der Transaktion reduziert und teure Ressourcen Sperren freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="56207-157">Voting explicitly can reduce the overall duration of the transaction and release expensive resource locks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56207-158">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="56207-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56207-159">Schritt 1: Erstellen einer transaktionalen Komponente</span><span class="sxs-lookup"><span data-stu-id="56207-159">Step 1: Creating a Transactional Component</span></span>](step-1--creating-a-transactional-component.md)
</dt> <dt>

[<span data-ttu-id="56207-160">Schritt 3: wieder verwenden von Komponenten</span><span class="sxs-lookup"><span data-stu-id="56207-160">Step 3: Reusing Components</span></span>](step-3--reusing-components.md)
</dt> <dt>

[<span data-ttu-id="56207-161">Kontext Aktivierung</span><span class="sxs-lookup"><span data-stu-id="56207-161">Context Activation</span></span>](context-activation.md)
</dt> <dt>

[<span data-ttu-id="56207-162">Verwalten von automatischen Transaktionen in com+</span><span class="sxs-lookup"><span data-stu-id="56207-162">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 




