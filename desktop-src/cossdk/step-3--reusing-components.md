---
description: 'Schritt 3: Wiederverwenden von Komponenten'
ms.assetid: d9c14cf8-5bc9-4a6c-9421-c16c3f41b10d
title: 'Schritt 3: Wiederverwenden von Komponenten'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf500746e7c9052a421691299903437e129108405b49c7753a841e8ca505518
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895809"
---
# <a name="step-3-reusing-components"></a>Schritt 3: Wiederverwenden von Komponenten

## <a name="objectives"></a>Ziele

In diesem Schritt lernen Sie Folgendes kennen:

-   Wiederverwendbare Komponenten.
-   Planen der Wiederverwendebarkeit

## <a name="description"></a>BESCHREIBUNG

Zwei vorherige Teile dieser COM+-Dienstprimierung, [Schritt 1: Erstellen einer Transaktionskomponente](step-1--creating-a-transactional-component.md) und [Schritt 2: Erweitern einer Transaktion über mehrere Komponenten hinweg,](step-2--extending-a-transaction-across-multiple-components.md) zeigen, wie eine Komponente geschrieben wird, die eine zweite Komponente aufruft, um beim Abschließen einiger Arbeit zu helfen und Die Autorinformationen in der Microsoft SQL Server Pubs-Datenbank zu aktualisieren. alle Arbeiten werden durch eine einzelne Transaktion geschützt. Die Beispielkomponenten konzentrierten sich auf die Aktualisierung der Daten eines Autors und die Überprüfung der Adresse des Autors, und COM+ hat Transaktionsverarbeitung, [JIT-Aktivierung](com--just-in-time-activation.md)und [Parallelitätsschutz](com--synchronization.md)bereitgestellt.

In diesem Schritt wird veranschaulicht, wie die in den Schritten 1 und 2 erstellten Komponenten wiederverwendet werden, und es wird erläutert, was dies für den Entwurf dieser Komponenten bedeutet. Wie in der folgenden Abbildung gezeigt, bedeutet dies das Erstellen einer neuen Komponente, `AddNewAuthor` , die der Datenbank durch Aufrufen von neue Autoren hinzufügt. `UpdateAuthorAddress`

![Diagramm, das den Ablauf beim Wiederverwenden von Komponenten zeigt.](images/e746f50e-2e86-4e59-82f9-f407d2b0325c.png)

Zusätzlich zur Wiederverwendung vorhandener Komponentenfunktionen `AddNewAuthor` ruft eine weitere neue Komponente mit dem Namen `ValidateAuthorName` auf. Wie die obige Abbildung zeigt, `ValidateAuthorName` ist nicht transaktional. Der Transaktionsattributwert für diese Komponente bleibt bei der Standardeinstellung (**Nicht unterstützt**), um ihre Arbeit von der Transaktion auszuschließen. Wie im Beispielcode in Schritt 3 gezeigt, `ValidateAuthorName` führt schreibgeschützte Abfragen für die Datenbank aus, und der Fehler dieser nebensächlichen Aufgabe sollte nicht das Potenzial haben, die Transaktion abzubricht. Der Transaktionsattributwert der Komponente ist jedoch `AddNewAuthor` auf **Erforderlich** festgelegt.

Die `AddNewAuthor` `UpdateAuthorAddress` Komponenten , und stimmen alle in der `ValidateAuthorAddress` Transaktion ab. In dieser Transaktion `AddNewAuthor` ist das Stammobjekt. COM+ macht das erste in der Transaktion erstellte Objekt immer zum Stammobjekt.

In diesem Beispiel ist die Wiederverwendung der `UpdateAuthorAddress` Komponente einfach– COM+ stellt automatisch die erwarteten Dienste bereit. Die Ergebnisse würden sich jedoch unterscheiden, wenn der Transaktionsattributwert der `UpdateAuthorAddress` Komponente anfänglich auf Erfordert **Neu** anstelle von **Erforderlich** festgelegt wäre. Auf der Oberfläche werden beide Einstellungen ähnlich angezeigt. beide garantieren eine Transaktion. **Erfordert Neu,** startet jedoch immer eine neue Transaktion, während **Required** nur dann eine neue Transaktion startet, wenn der Aufrufer des Objekts nicht transaktional ist. Sie sehen, wie wichtig es war, sorgfältig und sorgfältig zu `UpdateAuthorAddress` konfigurieren. Andernfalls hat COM+ die Dienstanforderung möglicherweise anders interpretiert und dabei zwei nicht verbundene Transaktionen generiert, wie in der folgenden Abbildung dargestellt, anstelle einer Transaktion.

![Diagramm, das den Ablauf beim Wiederverwenden von Komponenten mit "Erfordert Neu" zeigt.](images/24b9edf6-af00-4994-8fa1-cee4ace16379.png)

> [!Note]  
> Wenn Sie Komponenten wiederverwenden, stellen Sie sicher, dass die Dienste so konfiguriert sind, dass sie das gewünschte Ergebnis unterstützen.

 

## <a name="sample-code"></a>Beispielcode

Die AddNewAuthor-Komponente führt Batchhinzufügungen neuer Autoren durch, indem das Objekt aktiv bleibt, bis der Client seinen Verweis auf das Objekt freigibt.


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



Die `ValidateAuthorName` Komponente überprüft Autorennamen, bevor `AddNewAuthor` sie der Datenbank den Namen hinzufügt. Diese Komponente löst einen Fehler an ihren Aufrufer zurück, wenn etwas Unerwartetes geschieht.


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



## <a name="summary"></a>Zusammenfassung

-   Es gibt Zeiten, in denen Sie nicht möchten, dass eine Komponente in der Transaktion abstimmt.
-   COM+ erzwingt keine JIT-Aktivierung oder keinen Parallelitätsschutz für nicht transaktionale Komponenten. Sie können diese Dienste separat konfigurieren.
-   Die Konfiguration einer aufrufenden Komponente wirkt sich darauf aus, wie COM+ die Dienstanforderungen der aufgerufenen Komponente interpretiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schritt 1: Erstellen einer Transaktionskomponente](step-1--creating-a-transactional-component.md)
</dt> <dt>

[Schritt 2: Erweitern einer Transaktion über mehrere Komponenten hinweg](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[Konfigurieren von Transaktionen](configuring-transactions.md)
</dt> <dt>

[Entwerfen für Skalierbarkeit](designing-for-scalability.md)
</dt> </dl>

 

 



