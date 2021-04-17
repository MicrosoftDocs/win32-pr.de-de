---
description: 'Schritt 3: wieder verwenden von Komponenten'
ms.assetid: d9c14cf8-5bc9-4a6c-9421-c16c3f41b10d
title: 'Schritt 3: wieder verwenden von Komponenten'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f44446ee20baa6dc8c947ef0650f4478847a1c
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104559992"
---
# <a name="step-3-reusing-components"></a><span data-ttu-id="ecf92-103">Schritt 3: wieder verwenden von Komponenten</span><span class="sxs-lookup"><span data-stu-id="ecf92-103">Step 3: Reusing Components</span></span>

## <a name="objectives"></a><span data-ttu-id="ecf92-104">Ziele</span><span class="sxs-lookup"><span data-stu-id="ecf92-104">Objectives</span></span>

<span data-ttu-id="ecf92-105">In diesem Schritt erfahren Sie mehr über Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ecf92-105">In this step, you will learn about the following:</span></span>

-   <span data-ttu-id="ecf92-106">Wiederverwendbare Komponenten.</span><span class="sxs-lookup"><span data-stu-id="ecf92-106">Reusable components.</span></span>
-   <span data-ttu-id="ecf92-107">Planen der Wiederverwendbarkeit.</span><span class="sxs-lookup"><span data-stu-id="ecf92-107">How to plan for reusability.</span></span>

## <a name="description"></a><span data-ttu-id="ecf92-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ecf92-108">Description</span></span>

<span data-ttu-id="ecf92-109">Zwei vorherige Teile dieses com+-Diensts: [Schritt 1: Erstellen einer Transaktions Komponente](step-1--creating-a-transactional-component.md) und [Schritt 2: Erweitern einer Transaktion über mehrere Komponenten](step-2--extending-a-transaction-across-multiple-components.md) erfahren, wie eine Komponente geschrieben wird, die eine zweite Komponente aufruft, um den Abschluss einiger Aufgaben zu unterstützen und die Autoreninformationen in der Microsoft SQL Server pubs-Datenbank zu aktualisieren. Alle Arbeiten werden durch eine einzelne Transaktion geschützt.</span><span class="sxs-lookup"><span data-stu-id="ecf92-109">Two previous parts of this COM+ services primer, [Step 1: Creating a Transactional Component](step-1--creating-a-transactional-component.md) and [Step 2: Extending a Transaction Across Multiple Components](step-2--extending-a-transaction-across-multiple-components.md) show how to write one component that calls a second component to assist in completing some work, updating author information in the Microsoft SQL Server Pubs database; all work is protected by a single transaction.</span></span> <span data-ttu-id="ecf92-110">Die Beispiel Komponenten konzentrieren sich auf das Aktualisieren der Daten eines Autors und das Überprüfen der Adresse des Autors, und com+ hat die Transaktionsverarbeitung, [JIT-Aktivierung](com--just-in-time-activation.md)und Parallelitäts [Schutz](com--synchronization.md)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ecf92-110">The sample components focused on the work of updating an author's data and verifying the author's address, and COM+ provided transaction processing, [JIT activation](com--just-in-time-activation.md), and [concurrency protection](com--synchronization.md).</span></span>

<span data-ttu-id="ecf92-111">In diesem Schritt wird veranschaulicht, wie die in den Schritten 1 und 2 erstellten Komponenten wieder verwendet werden, und es wird erläutert, was dies für den Entwurf dieser Komponenten bedeutet.</span><span class="sxs-lookup"><span data-stu-id="ecf92-111">This step demonstrates how to reuse the components created in steps 1 and 2 and looks at what this means to the design of those components.</span></span> <span data-ttu-id="ecf92-112">Wie in der folgenden Abbildung gezeigt, bedeutet dies, dass eine neue Komponente erstellt wird, `AddNewAuthor` die der Datenbank neue Autoren hinzufügt, indem aufgerufen wird `UpdateAuthorAddress` .</span><span class="sxs-lookup"><span data-stu-id="ecf92-112">As shown in the following illustration, this means creating a new component, `AddNewAuthor`, that adds new authors to the database by calling `UpdateAuthorAddress`.</span></span>

![Diagramm, das den Flow anzeigt, wenn Komponenten wieder verwendet werden.](images/e746f50e-2e86-4e59-82f9-f407d2b0325c.png)

<span data-ttu-id="ecf92-114">Zusätzlich zur Wiederverwendung vorhandener Komponenten Funktionen `AddNewAuthor` Ruft eine weitere neue Komponente mit dem Namen auf `ValidateAuthorName` .</span><span class="sxs-lookup"><span data-stu-id="ecf92-114">In addition to reusing existing component functionality, `AddNewAuthor` calls another new component called `ValidateAuthorName`.</span></span> <span data-ttu-id="ecf92-115">Wie die vorherige Abbildung zeigt, `ValidateAuthorName` ist nicht transaktional.</span><span class="sxs-lookup"><span data-stu-id="ecf92-115">As the preceding illustration shows, `ValidateAuthorName` is non-transactional.</span></span> <span data-ttu-id="ecf92-116">Der Wert des Transaktions Attributs für diese Komponente bleibt bei der Standardeinstellung (**nicht unterstützt**), um die Arbeit von der Transaktion auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="ecf92-116">The transaction attribute value for this component is left at its default setting (**Not Supported**) to exclude its work from the transaction.</span></span> <span data-ttu-id="ecf92-117">Wie im Beispielcode Schritt 3 gezeigt, werden schreibgeschützte `ValidateAuthorName` Abfragen für die Datenbank durchführt, und der Fehler dieser kleinen Aufgabe sollte nicht die Möglichkeit haben, die Transaktion abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="ecf92-117">As shown in the step 3 sample code, `ValidateAuthorName` performs read-only queries on the database, and the failure of this minor task should not have the potential to abort the transaction.</span></span> <span data-ttu-id="ecf92-118">Allerdings ist der Wert des Transaktions Attributs der `AddNewAuthor` Komponente auf **Required** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ecf92-118">However, the transaction attribute value of the `AddNewAuthor` component is set to **Required**.</span></span>

<span data-ttu-id="ecf92-119">Die `AddNewAuthor` `UpdateAuthorAddress` Komponenten, und `ValidateAuthorAddress` Stimmen in der Transaktion ab.</span><span class="sxs-lookup"><span data-stu-id="ecf92-119">The `AddNewAuthor`, `UpdateAuthorAddress`, and `ValidateAuthorAddress` components all vote in the transaction.</span></span> <span data-ttu-id="ecf92-120">In dieser Transaktion `AddNewAuthor` ist das Stamm Objekt.</span><span class="sxs-lookup"><span data-stu-id="ecf92-120">In this transaction, `AddNewAuthor` is the root object.</span></span> <span data-ttu-id="ecf92-121">Com+ macht das erste Objekt, das in der Transaktion erstellt wird, immer zum Stamm Objekt.</span><span class="sxs-lookup"><span data-stu-id="ecf92-121">COM+ always makes the first object created in the transaction the root object.</span></span>

<span data-ttu-id="ecf92-122">In diesem Beispiel ist die Wiederverwendung der `UpdateAuthorAddress` Komponente einfach – durch com + werden die erwarteten Dienste automatisch bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ecf92-122">In this example, reusing the `UpdateAuthorAddress` component is easy—COM+ automatically delivers the expected services.</span></span> <span data-ttu-id="ecf92-123">Die Ergebnisse unterscheiden sich jedoch, wenn der Wert des Transaktions Attributs der `UpdateAuthorAddress` Komponente anfänglich auf " **neu** " anstatt " **erforderlich**" festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="ecf92-123">However, the results would be different if the transaction attribute value of the `UpdateAuthorAddress` component were initially set to **Requires New** instead of **Required**.</span></span> <span data-ttu-id="ecf92-124">Auf der-Oberfläche erscheinen beide Einstellungen ähnlich. Beide garantieren eine Transaktion.</span><span class="sxs-lookup"><span data-stu-id="ecf92-124">On the surface, both settings appear similar; both guarantee a transaction.</span></span> <span data-ttu-id="ecf92-125">**Erfordert New, erfordert** jedoch immer eine neue Transaktion, während **erforderlich** eine neue Transaktion nur dann startet, wenn der Aufrufer des Objekts nicht transaktional ist.</span><span class="sxs-lookup"><span data-stu-id="ecf92-125">**Requires New**, however, always starts a new transaction, while **Required** starts a new transaction only when the object's caller is non-transactional.</span></span> <span data-ttu-id="ecf92-126">Sie sehen, wie wichtig es ist, `UpdateAuthorAddress` sorgfältig und sorgfältig zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ecf92-126">You can see from this how important it was to configure `UpdateAuthorAddress` carefully and thoughtfully.</span></span> <span data-ttu-id="ecf92-127">Andernfalls könnte com+ die Service Request anders interpretieren und dabei zwei nicht verknüpfte Transaktionen erzeugen, wie in der folgenden Abbildung dargestellt, anstelle von einer.</span><span class="sxs-lookup"><span data-stu-id="ecf92-127">Otherwise, COM+ might have interpreted the service request differently, generating two unrelated transactions, as shown in the following illustration, instead of one.</span></span>

![Diagramm, das den Flow anzeigt, wenn Komponenten mit "erfordert New" wieder verwendet werden.](images/24b9edf6-af00-4994-8fa1-cee4ace16379.png)

> [!Note]  
> <span data-ttu-id="ecf92-129">Wenn Sie Komponenten wieder verwenden, stellen Sie sicher, dass die Dienste für die Unterstützung des gewünschten Ergebnisses konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="ecf92-129">When you reuse components, make sure the services are configured to support your desired outcome.</span></span>

 

## <a name="sample-code"></a><span data-ttu-id="ecf92-130">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="ecf92-130">Sample code</span></span>

<span data-ttu-id="ecf92-131">Die Komponente addnewauthor führt Batch Ergänzungen neuer Autoren durch, indem das Objekt so lange aktiv bleibt, bis der Client seinen Verweis auf das Objekt freigibt.</span><span class="sxs-lookup"><span data-stu-id="ecf92-131">The AddNewAuthor component performs batch additions of new authors by allowing the object to remain active until the client releases its reference to the object.</span></span>


```VB
Option Explicit
'
'   Purpose:   This class is used for adding a new author.
'
'   Notes:    IMPT:  This component implicitly assumes that it will
'             always run in a transaction. Undefined results may 
'             otherwise occur.
'
'  AddNewAuthor
'
Public Sub AddNewAuthor( _
                        ByVal strAuthorFirstName As String, _
                        ByVal strAuthorLastName As String, _
                        ByVal strPhone As String, _
                        ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String, _
                        ByVal boolContracted As Boolean)
  ' Handle any errors.
  On Error GoTo UnexpectedError

  ' Verify component is in a transaction.
  ' The VerifyInTxn subroutine is described in Step 1.
  VerifyInTxn

  ' Get our object context.
  Dim objcontext As COMSVCSLib.ObjectContext
  Set objcontext = GetObjectContext

  ' Get the IContextState object.
  Dim contextstate As COMSVCSLib.IContextState
  Set contextstate = objcontext

  ' Validate that the author is OK.
  ' The ValidateAuthorName function is described after this function.
  Dim oValidateAuthName As Object
  Dim bValidAuthor As Boolean
  Set oValidateAuthName = CreateObject("ComplusPrimer.ValidateAuthorName")
  bValidAuthor = oValidateAuthName.ValidateAuthorName( _
    strAuthorFirstName, strAuthorLastName)
  If Not bValidAuthor Then
    Err.Raise 999999, "The AddNewAuthor component", _
      "You tried to add an author on the banned list!"
  End If
  
  ' Open the connection to the database.
  Dim conn As ADODB.Connection
  Set conn = CreateObject("ADODB.Connection")

  ' Specify the OLE DB provider.
  conn.Provider = "SQLOLEDB"

  ' Connect using Windows Authentication.
  Dim strProv As String
  strProv = "Server=MyDBServer;Database=pubs;Trusted_Connection=yes"

  ' Open the database.
  conn.Open strProv

  ' Tell the database to actually add the author; use empty strings 
  ' for this part and rely on the UpdateAuthorAddress 
  ' component to validate the address/phone/etc data.
  ' Default Contract flag is off.
  Dim strUpdateString As String
  strUpdateString = "insert into authors values(_
                     '789-65-1234'," & _
                     strAuthorLastName & ", " & _
                     strAuthorFirstName & ", " & _
                     "'(555) 555-5555', ', ', ', '98765', "

  If boolContracted Then
    strUpdateString = strUpdateString + "1)"
  Else
    strUpdateString = strUpdateString + "0)"
  End If

  conn.Execute strUpdateString
  
  ' Close the connection; this potentially allows 
  ' another component in the same transaction to
  ' reuse the connection from the connection pool.
  conn.Close
  Set conn = Nothing
  
  ' Create the UpdateAuthorAddress component.
  Dim oUpdateAuthAddr As Object
  Set oUpdateAuthAddr = CreateObject("ComplusPrimer.UpdateAuthorAddress")
  
  ' The component throws an error if anything goes wrong.
  oUpdateAuthAddr.UpdateAuthorAddress "", strPhone, _
    strAddress, strCity, strState, strZip
    
  Set oUpdateAuthAddr = Nothing
  
  ' Everything works--commit the transaction.
  contextstate.SetMyTransactionVote TxCommit
  
  '  Design issue:  Allow batch additions of new
  '  authors in one transaction, or should each new author be added
  '  in a single new transaction?
  contextstate.SetDeactivateOnReturn False
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
  
End Sub
```



<span data-ttu-id="ecf92-132">Die `ValidateAuthorName` Komponente überprüft Autorennamen, bevor `AddNewAuthor` der Name der Datenbank hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="ecf92-132">The `ValidateAuthorName` component validates author names before `AddNewAuthor` adds the name to the database.</span></span> <span data-ttu-id="ecf92-133">Diese Komponente löst einen Fehler an den Aufrufer aus, wenn etwas unerwartetes Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="ecf92-133">This component throws an error back to its caller if something unexpected happens.</span></span>


```VB
Option Explicit
'
'   Purpose:   This class is used for validating authors before
'              adding them to the database.
'
'   Notes:   This component doesn't need to be in a transaction because
'            it is performing read-only queries on the database,
'            especially since these queries are not overlapping with
'            any updates of end-user data. If an unexpected error
'            happens, let the error go back to the caller who
'            needs to handle it.
'

Public Function ValidateAuthorName( _
                        ByVal strAuthorFirstName As String, _
                        ByVal strAuthorLastName As String _
                        ) As Boolean
  ValidateAuthorName = False

  ' Open the connection to the database.
  Dim conn As ADODB.Connection
  Set conn = CreateObject("ADODB.Connection")

  ' Specify the OLE DB provider.
  conn.Provider = "SQLOLEDB"

  ' Connect using Windows Authentication.
  Dim strProv As String
  strProv = "Server=MyDBServer;Database=pubs;Trusted_Connection=yes"

  ' Open the database.
  conn.Open strProv

  ' Suppose another hypothetical table has been added to the Pubs 
  ' database, one that contains a list of banned authors.
  Dim rs As ADODB.Recordset
  Set rs = conn.Execute("select * from banned_authors")
  
  ' Loop through the banned-author list looking for the specified
  ' author.
  While Not rs.EOF
    If rs.Fields("FirstName") = strAuthorFirstName And _
      rs.Fields("LastName") = strAuthorLastName Then
        ' This is a banned author.
        conn.Close
        Set conn = Nothing
        Set rs = Nothing
        Exit Function
    End If
    rs.MoveNext
  Wend
  
  ' None of the added authors found in the banned list.
  ValidateAuthorName = True
  conn.Close
  Set conn = Nothing
  Set rs = Nothing
End Function
```



## <a name="summary"></a><span data-ttu-id="ecf92-134">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ecf92-134">Summary</span></span>

-   <span data-ttu-id="ecf92-135">Es gibt Zeiten, in denen eine Komponente nicht in der Transaktion abstimmen soll.</span><span class="sxs-lookup"><span data-stu-id="ecf92-135">There are times when you don't want a component to vote in the transaction.</span></span>
-   <span data-ttu-id="ecf92-136">Com+ erzwingt nicht die JIT-Aktivierung oder den Parallelitäts Schutz für nicht transaktionale Komponenten.</span><span class="sxs-lookup"><span data-stu-id="ecf92-136">COM+ does not enforce JIT activation or concurrency protection on non-transactional components.</span></span> <span data-ttu-id="ecf92-137">Diese Dienste können separat konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="ecf92-137">You may configure these services separately.</span></span>
-   <span data-ttu-id="ecf92-138">Die Konfiguration einer aufrufenden Komponente wirkt sich darauf aus, wie com+ die Service Requests der aufgerufenen Komponente interpretiert.</span><span class="sxs-lookup"><span data-stu-id="ecf92-138">A calling component's configuration affects how COM+ interprets the service requests of the called component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ecf92-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ecf92-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecf92-140">Schritt 1: Erstellen einer transaktionalen Komponente</span><span class="sxs-lookup"><span data-stu-id="ecf92-140">Step 1: Creating a Transactional Component</span></span>](step-1--creating-a-transactional-component.md)
</dt> <dt>

[<span data-ttu-id="ecf92-141">Schritt 2: Erweitern einer Transaktion über mehrere Komponenten hinweg</span><span class="sxs-lookup"><span data-stu-id="ecf92-141">Step 2: Extending a Transaction Across Multiple Components</span></span>](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[<span data-ttu-id="ecf92-142">Konfigurieren von Transaktionen</span><span class="sxs-lookup"><span data-stu-id="ecf92-142">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="ecf92-143">Entwerfen von Skalierbarkeit</span><span class="sxs-lookup"><span data-stu-id="ecf92-143">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> </dl>

 

 



