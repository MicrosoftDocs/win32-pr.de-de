---
description: 'Schritt 1: Erstellen einer Transaktionskomponente'
ms.assetid: 9ab9ac2d-bf1d-419c-8f6b-e2ee80a4bf20
title: 'Schritt 1: Erstellen einer Transaktionskomponente'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f5c87fb5c5f615ee04a3233f1a563d5ae5230e4dd18908c78e94092ff0f5c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305409"
---
# <a name="step-1-creating-a-transactional-component"></a>Schritt 1: Erstellen einer Transaktionskomponente

## <a name="objectives"></a>Ziele

In diesem Schritt lernen Sie Folgendes:

-   Schreiben einer Transaktionskomponente in Microsoft Visual Basic
-   Standardeinstellungen für COM+-Dienste
-   Konfigurieren von COM+-Diensten

## <a name="description"></a>Beschreibung

Die UpdateAuthorAddress-Komponente, die in diesem Abschnitt zu erstellende Komponente, aktualisiert die Adresse eines vorhandenen Autors in der Pubs-Datenbank. Die Pubs-Datenbank ist eine Beispieldatenbank, die mit Microsoft SQL Server. Es enthält Veröffentlichungsinformationen wie Autorennamen, Adressen und Buchtitel.

> [!Note]  
> Pubs ist der Datenspeicher, der in dieser Grundung verwendet wird.

 

Da UpdateAuthorAddress einen Datenspeicher aktualisiert, empfiehlt es sich, die Arbeit wie in der folgenden Abbildung gezeigt in eine Transaktion einarbeiten, sodass COM+ automatisch eine Transaktion startet und die Datenbank (Ressourcen-Manager) in diese Transaktion einträgt, wenn ein Client die Komponente aufruft. (Ausführliche Informationen zu Transaktionen in COM+ finden Sie unter [COM+-Transaktionen](com--transactions.md).)

![Diagramm, das eine COM+-Transaktion mit UpdateAuthorAddress zeigt.](images/d5a47e03-c07e-4db3-b328-111ca9e50bef.png)

Um UpdateAuthorAddress zu einer Transaktionskomponente zu machen, sind die folgenden Schritte erforderlich:

1.  Die Komponente muss geschrieben werden. Für zusätzlichen Schutz wird eine Unterroutine hinzugefügt, die überprüft, ob COM+ das Objekt in einer Transaktion erstellt hat. Außerdem ist die grundlegende Fehlerbehandlung in der -Komponente enthalten, um die Fehlerwiederherstellung zu vereinfachen. Transaktionsüberprüfung und Fehlerbehandlung verbessern die Zuverlässigkeit der Komponente. (Eine vollständige Auflistung der UpdateAuthorAddress-Komponente finden Sie unter Schritt 1-Beispielcode.)
2.  Nach dem Hinzufügen der Komponente zu einer COM+-Anwendung und der Installation der Anwendung muss das Transaktionsattribut auf **Erforderlich** festgelegt werden. Dadurch wird sichergestellt, dass COM+ jedes UpdateAuthorAddress-Objekt in einer Transaktion erstellt. Anweisungen zum Festlegen des Transaktionsattributs für eine Komponente finden Sie unter [Festlegen des Transaktionsattributs](setting-the-transaction-attribute.md).
    > [!Note]  
    > Das Festlegen des Transaktionsattributs für eine Komponente definiert, wie COM+ jedes Objekt im Hinblick auf Transaktionen erstellt. Transaktionsattributwerte **sind Ignored**, **Not Supported**, **Supported**, **Required** und **Requires New**. Der **Required-Wert** ist nicht einer der Standardattributwerte einer Komponente.

     

COM+ bindet den Transaktionsdienst mit Just-In-Time-Aktivierung (JIT) und Parallelität. Wenn Sie eine Komponente als transaktional deklarieren, erzwingt COM+ auch jit-Aktivierung und Parallelitätsschutz (Synchronisierung).

## <a name="sample-code"></a>Beispielcode

Die UpdateAuthorAddress-Komponente öffnet eine Verbindung mit der Pubs-Datenbank, sodass der Benutzer den Namen, die Adresse oder den Vertragsstatus eines Autors ändern kann. Sie ruft auch eine zweite Komponente auf, die in [Schritt 2: Erweitern einer](step-2--extending-a-transaction-across-multiple-components.md)Transaktion über mehrere Komponenten erläutert wird.

Um den folgenden Code in einem Microsoft Visual Basic-Projekt zu verwenden, öffnen Sie ein neues ActiveX.dll-Projekt, und fügen Sie Verweise auf die Microsoft ActiveX Data Objects Library und die COM+-Diensttypbibliothek hinzu.

> [!Note]  
> Der Beispielcode in diesem Primer dient zur Veranschaulichung und ist möglicherweise nicht der effizienteste für die tatsächliche Staging- und Produktionsumgebung.

 


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



## <a name="summary"></a>Zusammenfassung

-   COM+ weist Standardattributwerte zu. Sie können die meisten Dienstattribute neu konfigurieren.
-   Wenn Sie das Transaktionsattribut einer Komponente auf Erforderlich festlegen, wird sichergestellt, dass COM+ jede Instanz dieser Komponente in einer Transaktion erstellen muss, aber nicht notwendigerweise eine neue Transaktion startet. 
-   Das Überprüfen des Vorhandenseins einer Transaktion bestätigt, dass der Transaktionsattributwert der Komponente nicht versehentlich auf einen nicht transaktionalen Wert zurückgesetzt wurde, z. B. **Ignore** oder **Not Supported**.
-   Durch die Behandlung von Fehlern wird ihre Komponente zuverlässiger und einfacher zu beheben.
-   COM+ erzwingt [JIT-Aktivierungs-](com--just-in-time-activation.md) und [Parallelitätsschutzdienste](com--synchronization.md) für Transaktionskomponenten.
-   Wenn Sie die Datenbankverbindung schließen, kann eine andere Komponente in derselben Transaktion die Verbindung aus dem Verbindungspool wiederverwenden. (Verbindungspooling sollte nicht mit [Objektpooling verwechselt werden.)](com--object-pooling.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schritt 2: Erweitern einer Transaktion auf mehrere Komponenten](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[Schritt 3: Wiederverwendung von Komponenten](step-3--reusing-components.md)
</dt> <dt>

[COM+-Just-In-Time-Aktivierung](com--just-in-time-activation.md)
</dt> <dt>

[COM+-Synchronisierung](com--synchronization.md)
</dt> <dt>

[Konfigurieren von Transaktionen](configuring-transactions.md)
</dt> <dt>

[Erstellen von COM+-Anwendungen](creating-com--applications.md)
</dt> <dt>

[Festlegen des Transaktionsattributs](setting-the-transaction-attribute.md)
</dt> </dl>

 

 



