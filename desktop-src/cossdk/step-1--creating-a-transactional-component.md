---
description: 'Schritt 1: Erstellen einer transaktionalen Komponente'
ms.assetid: 9ab9ac2d-bf1d-419c-8f6b-e2ee80a4bf20
title: 'Schritt 1: Erstellen einer transaktionalen Komponente'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdc378d85e628504e8724b765362b3397826f5e5
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104350929"
---
# <a name="step-1-creating-a-transactional-component"></a><span data-ttu-id="adecb-103">Schritt 1: Erstellen einer transaktionalen Komponente</span><span class="sxs-lookup"><span data-stu-id="adecb-103">Step 1: Creating a Transactional Component</span></span>

## <a name="objectives"></a><span data-ttu-id="adecb-104">Ziele</span><span class="sxs-lookup"><span data-stu-id="adecb-104">Objectives</span></span>

<span data-ttu-id="adecb-105">In diesem Schritt erfahren Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="adecb-105">In this step, you will learn the following:</span></span>

-   <span data-ttu-id="adecb-106">So schreiben Sie eine transaktionale Komponente in Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="adecb-106">How to write a transactional component in Microsoft Visual Basic</span></span>
-   <span data-ttu-id="adecb-107">Die Standardeinstellungen für COM+-Dienste sind</span><span class="sxs-lookup"><span data-stu-id="adecb-107">What the default settings for COM+ services are</span></span>
-   <span data-ttu-id="adecb-108">Konfigurieren von COM+-Diensten</span><span class="sxs-lookup"><span data-stu-id="adecb-108">How to configure COM+ services</span></span>

## <a name="description"></a><span data-ttu-id="adecb-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="adecb-109">Description</span></span>

<span data-ttu-id="adecb-110">Mit der Komponente updateauthoraddress, der in diesem Abschnitt zu erstellenden Komponente, wird die Adresse eines vorhandenen Autors in der pubs-Datenbank aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="adecb-110">The UpdateAuthorAddress component, the component to be created in this section, updates the address of an existing author in the Pubs database.</span></span> <span data-ttu-id="adecb-111">Die pubs-Datenbank ist eine Beispieldatenbank, die im Lieferumfang von Microsoft SQL Server enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="adecb-111">The Pubs database is a sample database that ships with Microsoft SQL Server.</span></span> <span data-ttu-id="adecb-112">Sie enthält Veröffentlichungsinformationen, wie z. b. Autorennamen, Adressen und Buchtitel.</span><span class="sxs-lookup"><span data-stu-id="adecb-112">It contains publishing information such as author names, addresses, and book titles.</span></span>

> [!Note]  
> <span data-ttu-id="adecb-113">Pubs ist der Datenspeicher, der in dieser Einführung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="adecb-113">Pubs is the data store that is used throughout this primer.</span></span>

 

<span data-ttu-id="adecb-114">Da updateauthoraddress einen Datenspeicher aktualisiert, empfiehlt es sich, die Arbeit in eine Transaktion einzubeziehen, wie in der folgenden Abbildung dargestellt, sodass com+ automatisch eine Transaktion startet und die Datenbank (Resource Manager) in diese Transaktion eingetragen, wenn ein Client die Komponente aufruft.</span><span class="sxs-lookup"><span data-stu-id="adecb-114">Because UpdateAuthorAddress updates a data store, it is advisable to include the work in a transaction, as shown in the following illustration, so that when a client calls the component, COM+ automatically starts a transaction and enlists the database (resource manager) in that transaction.</span></span> <span data-ttu-id="adecb-115">(Ausführliche Informationen zu Transaktionen in com+ finden Sie unter [com+-Transaktionen](com--transactions.md).)</span><span class="sxs-lookup"><span data-stu-id="adecb-115">(For detailed information about transactions in COM+, see [COM+ Transactions](com--transactions.md).)</span></span>

![Diagramm, das eine COM+-Transaktion mit updateauthoraddress anzeigt.](images/d5a47e03-c07e-4db3-b328-111ca9e50bef.png)

<span data-ttu-id="adecb-117">Damit updateauthoraddress eine transaktionale Komponente ist, sind die folgenden Schritte erforderlich:</span><span class="sxs-lookup"><span data-stu-id="adecb-117">To make UpdateAuthorAddress a transactional component, the following steps are required:</span></span>

1.  <span data-ttu-id="adecb-118">Die Komponente muss geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="adecb-118">The component must be written.</span></span> <span data-ttu-id="adecb-119">Für zusätzlichen Schutz wird eine Unterroutine hinzugefügt, die überprüft, ob com+ das Objekt in einer Transaktion erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="adecb-119">For extra protection, a subroutine is added, verifying that COM+ created the object in a transaction.</span></span> <span data-ttu-id="adecb-120">Außerdem ist die grundlegende Fehlerbehandlung in der Komponente enthalten, um die Fehlerwiederherstellung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="adecb-120">Also, basic error handling is included in the component to simplify error recovery.</span></span> <span data-ttu-id="adecb-121">Die Transaktions Überprüfung und die Fehlerbehandlung verbessern die Zuverlässigkeit der Komponente.</span><span class="sxs-lookup"><span data-stu-id="adecb-121">Transaction verification and error handling enhance the reliability of the component.</span></span> <span data-ttu-id="adecb-122">(Siehe Schritt 1 Beispiel Code für eine komplette Liste der Komponente updateauthoraddress.)</span><span class="sxs-lookup"><span data-stu-id="adecb-122">(See Step 1 Sample Code for a complete listing of the UpdateAuthorAddress component.)</span></span>
2.  <span data-ttu-id="adecb-123">Nachdem Sie die Komponente zu einer COM+-Anwendung hinzugefügt und die Anwendung installiert haben, muss das Transaktions Attribut auf " **erforderlich**" festgelegt werden, wodurch sichergestellt wird, dass com+ jedes updateauthoraddress-Objekt in einer Transaktion erstellt.</span><span class="sxs-lookup"><span data-stu-id="adecb-123">After adding the component to a COM+ application and installing the application, the transaction attribute must be set to **Required**, which guarantees that COM+ creates each UpdateAuthorAddress object in a transaction.</span></span> <span data-ttu-id="adecb-124">Anweisungen zum Festlegen des Transaktions Attributs für eine Komponente finden Sie unter [Festlegen des Transaktions Attributs](setting-the-transaction-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="adecb-124">For instructions on how to set the transaction attribute for a component, see [Setting the Transaction Attribute](setting-the-transaction-attribute.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="adecb-125">Das Festlegen des Transaction-Attributs für eine Komponente definiert, wie com+ jedes Objekt in Bezug auf Transaktionen erstellt.</span><span class="sxs-lookup"><span data-stu-id="adecb-125">Setting the transaction attribute on a component defines how COM+ creates each object with regard to transactions.</span></span> <span data-ttu-id="adecb-126">Transaktions Attributwerte werden **ignoriert**, **nicht unter** stützt, **unterstützt**, **erforderlich** und müssen **neu** sein.</span><span class="sxs-lookup"><span data-stu-id="adecb-126">Transaction attribute values are **Ignored**, **Not Supported**, **Supported**, **Required**, and **Requires New**.</span></span> <span data-ttu-id="adecb-127">Der **erforderliche** Wert ist keiner der Standard Attributwerte einer Komponente.</span><span class="sxs-lookup"><span data-stu-id="adecb-127">The **Required** value is not one of a component's default attribute values.</span></span>

     

<span data-ttu-id="adecb-128">Com+ bindet den Transaktions Dienst mit Just-in-time (JIT)-Aktivierung und Parallelität.</span><span class="sxs-lookup"><span data-stu-id="adecb-128">COM+ binds the transaction service with just-in-time (JIT) activation and concurrency.</span></span> <span data-ttu-id="adecb-129">Wenn Sie eine Komponente als transaktional deklarieren, erzwingt com+ auch die JIT-Aktivierung und den Parallelitäts Schutz (Synchronisierung).</span><span class="sxs-lookup"><span data-stu-id="adecb-129">When you declare a component to be transactional, COM+ also enforces JIT activation and concurrency protection (synchronization).</span></span>

## <a name="sample-code"></a><span data-ttu-id="adecb-130">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="adecb-130">Sample code</span></span>

<span data-ttu-id="adecb-131">Die Komponente updateauthoraddress öffnet eine Verbindung mit der pubs-Datenbank und ermöglicht dem Benutzer, den Namen, die Adresse oder den Vertragsstatus eines Autors zu ändern.</span><span class="sxs-lookup"><span data-stu-id="adecb-131">The UpdateAuthorAddress component opens a connection to the Pubs database, allowing the user to modify an author's name, address, or contract status.</span></span> <span data-ttu-id="adecb-132">Außerdem wird eine zweite Komponente aufgerufen, die in [Schritt 2: Erweitern einer Transaktion über mehrere Komponenten](step-2--extending-a-transaction-across-multiple-components.md)erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="adecb-132">It also calls a second component, which is discussed in [Step 2: Extending a Transaction Across Multiple Components](step-2--extending-a-transaction-across-multiple-components.md).</span></span>

<span data-ttu-id="adecb-133">Um den folgenden Code in einem Microsoft Visual Basic-Projekt zu verwenden, öffnen Sie ein neues ActiveX.dll-Projekt, und fügen Sie Verweise auf die Microsoft ActiveX Data Objects-Bibliothek und die Typbibliothek für COM+-Dienste hinzu.</span><span class="sxs-lookup"><span data-stu-id="adecb-133">To use the following code in a Microsoft Visual Basic project, open a new ActiveX.dll project and add references to the Microsoft ActiveX Data Objects Library and the COM+ Services Type Library.</span></span>

> [!Note]  
> <span data-ttu-id="adecb-134">Der Beispielcode in dieser Einführung dient zur Veranschaulichung und ist möglicherweise nicht die effizienteste Lösung für die tatsächliche Staging-und Produktionsumgebung.</span><span class="sxs-lookup"><span data-stu-id="adecb-134">The sample code in this primer is for purposes of illustration and may not be the most efficient for actual staging and production.</span></span>

 


```VB
Option Explicit
'
'  Purpose:   This class is used for updating an author's address.
'
'  Notes:     IMPT:  This component implicitly assumes that it will 
'             always run in a transaction. Undefined results may 
'             otherwise occur.
'

'----------------------------------------------------------
'  VerifyInTxn subroutine
'      Verifies that this component is in a transaction.
'      Throws an error if it is not.
'
Private Sub VerifyInTxn()
  If Not GetObjectContext.IsInTransaction Then
    ' Transactions turned off. 
    Err.Raise 99999, "This component", "I need a transaction!"
  End If
  ' Component is in a transaction.
End Sub

'----------------------------------------------------------
'  UpdateAuthorAddress subroutine
'      Procedure to update an author's address.
'
Public Sub UpdateAuthorAddress( _
                        ByVal strAuthorID As String, _
                        ByVal strPhone As String, _
                       ByVal strAddress As String, _
                        ByVal strCity As String, _
                        ByVal strState As String, _
                        ByVal strZip As String)
  ' Handle any errors.
  On Error GoTo UnexpectedError
  
  ' Verify that component is in a transaction.
  VerifyInTxn
  
  ' Get object context.
  Dim objcontext As COMSVCSLib.ObjectContext
  Set objcontext = GetObjectContext
  
  ' Get the IContextState object.
  Dim contextstate As COMSVCSLib.IContextState
  Set contextstate = objcontext
  
  ' Validate the new address information.
  ' The ValidateAuthorAddress function is described in Step 2.
  Dim oValidateAuthAddr As Object
  Dim bValidAddr As Boolean
  Set oValidateAuthAddr = _
    CreateObject("ComplusPrimer.ValidateAuthorAddress") 
  bValidAddr = oValidateAuthAddr.ValidateAuthorAddress( _
    strAddress, strCity, strState, strZip)
  If Not bValidAddr Then
    Err.Raise 99999, "The UpdateAuthorAddress component", _
      "The address of the author is incorrect!"
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

  ' Execute the query.
  conn.Execute "update authors set phone= '" & strPhone & "'" & _
               " set address= '" & strAddress & "'" & _
               " set city= '" & strCity & "'" & _
               " set state= '" & strState & "'" & _
               " set zip= '" & strZip & "'" & _
               " where au_id = '" & strAuthorID & "'"
               
  ' Close the connection.
  conn.Close
  
  ' Get rid of the connection.
  Set conn = Nothing
                 
  ' Everything works--commit the transaction.
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn True
  Exit Sub
  
UnexpectedError:
  ' There's an error.
  contextstate.SetMyTransactionVote TxAbort
  contextstate.SetDeactivateOnReturn True
End Sub

```



## <a name="summary"></a><span data-ttu-id="adecb-135">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="adecb-135">Summary</span></span>

-   <span data-ttu-id="adecb-136">Com+ weist Standard Attributwerte zu.</span><span class="sxs-lookup"><span data-stu-id="adecb-136">COM+ assigns default attribute values.</span></span> <span data-ttu-id="adecb-137">Die meisten Dienst Attribute können neu konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="adecb-137">You can reconfigure most service attributes.</span></span>
-   <span data-ttu-id="adecb-138">Durch Festlegen des Transaktions Attributs für eine Komponente auf " **erforderlich** " wird sichergestellt, dass com+ jede Instanz dieser Komponente in einer Transaktion erstellen muss, aber nicht notwendigerweise eine neue Transaktion startet.</span><span class="sxs-lookup"><span data-stu-id="adecb-138">Setting a component's transaction attribute to **Required** guarantees that COM+ must create each instance of that component in a transaction but doesn't necessarily start a new transaction.</span></span>
-   <span data-ttu-id="adecb-139">Das Überprüfen des Vorhandenseins einer Transaktion bestätigt, dass der Wert des Transaktions Attributs der Komponente nicht versehentlich auf einen nicht transaktionalen Wert zurückgesetzt wurde, wie z. b. **Ignore** oder **nicht unterstützt**.</span><span class="sxs-lookup"><span data-stu-id="adecb-139">Verifying the presence of a transaction confirms that the component's transaction attribute value wasn't inadvertently reset to a non-transactional value, such as **Ignore** or **Not Supported**.</span></span>
-   <span data-ttu-id="adecb-140">Durch die Behandlung von Fehlern wird Ihre Komponente zuverlässiger und leichter zu beheben.</span><span class="sxs-lookup"><span data-stu-id="adecb-140">Handling errors makes your component more reliable and easier to troubleshoot.</span></span>
-   <span data-ttu-id="adecb-141">Com+ erzwingt [JIT-Aktivierungs](com--just-in-time-activation.md) -und Parallelitäts [Schutz](com--synchronization.md) -Dienste für Transaktions Komponenten.</span><span class="sxs-lookup"><span data-stu-id="adecb-141">COM+ enforces [JIT activation](com--just-in-time-activation.md) and [concurrency protection](com--synchronization.md) services for transactional components.</span></span>
-   <span data-ttu-id="adecb-142">Wenn Sie die Datenbankverbindung schließen, wenn Sie damit abgeschlossen sind, kann eine andere Komponente in derselben Transaktion die Verbindung aus dem Verbindungspool wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="adecb-142">Closing the database connection when you are done with it allows another component in the same transaction to reuse the connection from the connection pool.</span></span> <span data-ttu-id="adecb-143">(Das Verbindungspooling sollte nicht mit dem [Objekt Pooling](com--object-pooling.md)verwechselt werden.)</span><span class="sxs-lookup"><span data-stu-id="adecb-143">(Connection pooling should not be confused with [object pooling](com--object-pooling.md).)</span></span>

## <a name="related-topics"></a><span data-ttu-id="adecb-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="adecb-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adecb-145">Schritt 2: Erweitern einer Transaktion über mehrere Komponenten hinweg</span><span class="sxs-lookup"><span data-stu-id="adecb-145">Step 2: Extending a Transaction Across Multiple Components</span></span>](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[<span data-ttu-id="adecb-146">Schritt 3: wieder verwenden von Komponenten</span><span class="sxs-lookup"><span data-stu-id="adecb-146">Step 3: Reusing Components</span></span>](step-3--reusing-components.md)
</dt> <dt>

[<span data-ttu-id="adecb-147">Just-in-Time-Aktivierung von com+</span><span class="sxs-lookup"><span data-stu-id="adecb-147">COM+ Just-in-Time Activation</span></span>](com--just-in-time-activation.md)
</dt> <dt>

[<span data-ttu-id="adecb-148">Com+-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="adecb-148">COM+ Synchronization</span></span>](com--synchronization.md)
</dt> <dt>

[<span data-ttu-id="adecb-149">Konfigurieren von Transaktionen</span><span class="sxs-lookup"><span data-stu-id="adecb-149">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="adecb-150">Com+-Anwendungen werden erstellt.</span><span class="sxs-lookup"><span data-stu-id="adecb-150">Creating COM+ Applications</span></span>](creating-com--applications.md)
</dt> <dt>

[<span data-ttu-id="adecb-151">Festlegen des Transaktions Attributs</span><span class="sxs-lookup"><span data-stu-id="adecb-151">Setting the Transaction Attribute</span></span>](setting-the-transaction-attribute.md)
</dt> </dl>

 

 



