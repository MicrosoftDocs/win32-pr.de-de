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
# <a name="step-3-reusing-components"></a>Schritt 3: wieder verwenden von Komponenten

## <a name="objectives"></a>Ziele

In diesem Schritt erfahren Sie mehr über Folgendes:

-   Wiederverwendbare Komponenten.
-   Planen der Wiederverwendbarkeit.

## <a name="description"></a>BESCHREIBUNG

Zwei vorherige Teile dieses com+-Diensts: [Schritt 1: Erstellen einer Transaktions Komponente](step-1--creating-a-transactional-component.md) und [Schritt 2: Erweitern einer Transaktion über mehrere Komponenten](step-2--extending-a-transaction-across-multiple-components.md) erfahren, wie eine Komponente geschrieben wird, die eine zweite Komponente aufruft, um den Abschluss einiger Aufgaben zu unterstützen und die Autoreninformationen in der Microsoft SQL Server pubs-Datenbank zu aktualisieren. Alle Arbeiten werden durch eine einzelne Transaktion geschützt. Die Beispiel Komponenten konzentrieren sich auf das Aktualisieren der Daten eines Autors und das Überprüfen der Adresse des Autors, und com+ hat die Transaktionsverarbeitung, [JIT-Aktivierung](com--just-in-time-activation.md)und Parallelitäts [Schutz](com--synchronization.md)bereitgestellt.

In diesem Schritt wird veranschaulicht, wie die in den Schritten 1 und 2 erstellten Komponenten wieder verwendet werden, und es wird erläutert, was dies für den Entwurf dieser Komponenten bedeutet. Wie in der folgenden Abbildung gezeigt, bedeutet dies, dass eine neue Komponente erstellt wird, `AddNewAuthor` die der Datenbank neue Autoren hinzufügt, indem aufgerufen wird `UpdateAuthorAddress` .

![Diagramm, das den Flow anzeigt, wenn Komponenten wieder verwendet werden.](images/e746f50e-2e86-4e59-82f9-f407d2b0325c.png)

Zusätzlich zur Wiederverwendung vorhandener Komponenten Funktionen `AddNewAuthor` Ruft eine weitere neue Komponente mit dem Namen auf `ValidateAuthorName` . Wie die vorherige Abbildung zeigt, `ValidateAuthorName` ist nicht transaktional. Der Wert des Transaktions Attributs für diese Komponente bleibt bei der Standardeinstellung (**nicht unterstützt**), um die Arbeit von der Transaktion auszuschließen. Wie im Beispielcode Schritt 3 gezeigt, werden schreibgeschützte `ValidateAuthorName` Abfragen für die Datenbank durchführt, und der Fehler dieser kleinen Aufgabe sollte nicht die Möglichkeit haben, die Transaktion abzubrechen. Allerdings ist der Wert des Transaktions Attributs der `AddNewAuthor` Komponente auf **Required** festgelegt.

Die `AddNewAuthor` `UpdateAuthorAddress` Komponenten, und `ValidateAuthorAddress` Stimmen in der Transaktion ab. In dieser Transaktion `AddNewAuthor` ist das Stamm Objekt. Com+ macht das erste Objekt, das in der Transaktion erstellt wird, immer zum Stamm Objekt.

In diesem Beispiel ist die Wiederverwendung der `UpdateAuthorAddress` Komponente einfach – durch com + werden die erwarteten Dienste automatisch bereitgestellt. Die Ergebnisse unterscheiden sich jedoch, wenn der Wert des Transaktions Attributs der `UpdateAuthorAddress` Komponente anfänglich auf " **neu** " anstatt " **erforderlich**" festgelegt wurde. Auf der-Oberfläche erscheinen beide Einstellungen ähnlich. Beide garantieren eine Transaktion. **Erfordert New, erfordert** jedoch immer eine neue Transaktion, während **erforderlich** eine neue Transaktion nur dann startet, wenn der Aufrufer des Objekts nicht transaktional ist. Sie sehen, wie wichtig es ist, `UpdateAuthorAddress` sorgfältig und sorgfältig zu konfigurieren. Andernfalls könnte com+ die Service Request anders interpretieren und dabei zwei nicht verknüpfte Transaktionen erzeugen, wie in der folgenden Abbildung dargestellt, anstelle von einer.

![Diagramm, das den Flow anzeigt, wenn Komponenten mit "erfordert New" wieder verwendet werden.](images/24b9edf6-af00-4994-8fa1-cee4ace16379.png)

> [!Note]  
> Wenn Sie Komponenten wieder verwenden, stellen Sie sicher, dass die Dienste für die Unterstützung des gewünschten Ergebnisses konfiguriert sind.

 

## <a name="sample-code"></a>Beispielcode

Die Komponente addnewauthor führt Batch Ergänzungen neuer Autoren durch, indem das Objekt so lange aktiv bleibt, bis der Client seinen Verweis auf das Objekt freigibt.


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



Die `ValidateAuthorName` Komponente überprüft Autorennamen, bevor `AddNewAuthor` der Name der Datenbank hinzugefügt wird. Diese Komponente löst einen Fehler an den Aufrufer aus, wenn etwas unerwartetes Ereignis auftritt.


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

-   Es gibt Zeiten, in denen eine Komponente nicht in der Transaktion abstimmen soll.
-   Com+ erzwingt nicht die JIT-Aktivierung oder den Parallelitäts Schutz für nicht transaktionale Komponenten. Diese Dienste können separat konfiguriert werden.
-   Die Konfiguration einer aufrufenden Komponente wirkt sich darauf aus, wie com+ die Service Requests der aufgerufenen Komponente interpretiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schritt 1: Erstellen einer transaktionalen Komponente](step-1--creating-a-transactional-component.md)
</dt> <dt>

[Schritt 2: Erweitern einer Transaktion über mehrere Komponenten hinweg](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[Konfigurieren von Transaktionen](configuring-transactions.md)
</dt> <dt>

[Entwerfen von Skalierbarkeit](designing-for-scalability.md)
</dt> </dl>

 

 



