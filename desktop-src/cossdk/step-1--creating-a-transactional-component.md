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
# <a name="step-1-creating-a-transactional-component"></a>Schritt 1: Erstellen einer transaktionalen Komponente

## <a name="objectives"></a>Ziele

In diesem Schritt erfahren Sie Folgendes:

-   So schreiben Sie eine transaktionale Komponente in Microsoft Visual Basic
-   Die Standardeinstellungen für COM+-Dienste sind
-   Konfigurieren von COM+-Diensten

## <a name="description"></a>BESCHREIBUNG

Mit der Komponente updateauthoraddress, der in diesem Abschnitt zu erstellenden Komponente, wird die Adresse eines vorhandenen Autors in der pubs-Datenbank aktualisiert. Die pubs-Datenbank ist eine Beispieldatenbank, die im Lieferumfang von Microsoft SQL Server enthalten ist. Sie enthält Veröffentlichungsinformationen, wie z. b. Autorennamen, Adressen und Buchtitel.

> [!Note]  
> Pubs ist der Datenspeicher, der in dieser Einführung verwendet wird.

 

Da updateauthoraddress einen Datenspeicher aktualisiert, empfiehlt es sich, die Arbeit in eine Transaktion einzubeziehen, wie in der folgenden Abbildung dargestellt, sodass com+ automatisch eine Transaktion startet und die Datenbank (Resource Manager) in diese Transaktion eingetragen, wenn ein Client die Komponente aufruft. (Ausführliche Informationen zu Transaktionen in com+ finden Sie unter [com+-Transaktionen](com--transactions.md).)

![Diagramm, das eine COM+-Transaktion mit updateauthoraddress anzeigt.](images/d5a47e03-c07e-4db3-b328-111ca9e50bef.png)

Damit updateauthoraddress eine transaktionale Komponente ist, sind die folgenden Schritte erforderlich:

1.  Die Komponente muss geschrieben werden. Für zusätzlichen Schutz wird eine Unterroutine hinzugefügt, die überprüft, ob com+ das Objekt in einer Transaktion erstellt hat. Außerdem ist die grundlegende Fehlerbehandlung in der Komponente enthalten, um die Fehlerwiederherstellung zu vereinfachen. Die Transaktions Überprüfung und die Fehlerbehandlung verbessern die Zuverlässigkeit der Komponente. (Siehe Schritt 1 Beispiel Code für eine komplette Liste der Komponente updateauthoraddress.)
2.  Nachdem Sie die Komponente zu einer COM+-Anwendung hinzugefügt und die Anwendung installiert haben, muss das Transaktions Attribut auf " **erforderlich**" festgelegt werden, wodurch sichergestellt wird, dass com+ jedes updateauthoraddress-Objekt in einer Transaktion erstellt. Anweisungen zum Festlegen des Transaktions Attributs für eine Komponente finden Sie unter [Festlegen des Transaktions Attributs](setting-the-transaction-attribute.md).
    > [!Note]  
    > Das Festlegen des Transaction-Attributs für eine Komponente definiert, wie com+ jedes Objekt in Bezug auf Transaktionen erstellt. Transaktions Attributwerte werden **ignoriert**, **nicht unter** stützt, **unterstützt**, **erforderlich** und müssen **neu** sein. Der **erforderliche** Wert ist keiner der Standard Attributwerte einer Komponente.

     

Com+ bindet den Transaktions Dienst mit Just-in-time (JIT)-Aktivierung und Parallelität. Wenn Sie eine Komponente als transaktional deklarieren, erzwingt com+ auch die JIT-Aktivierung und den Parallelitäts Schutz (Synchronisierung).

## <a name="sample-code"></a>Beispielcode

Die Komponente updateauthoraddress öffnet eine Verbindung mit der pubs-Datenbank und ermöglicht dem Benutzer, den Namen, die Adresse oder den Vertragsstatus eines Autors zu ändern. Außerdem wird eine zweite Komponente aufgerufen, die in [Schritt 2: Erweitern einer Transaktion über mehrere Komponenten](step-2--extending-a-transaction-across-multiple-components.md)erläutert wird.

Um den folgenden Code in einem Microsoft Visual Basic-Projekt zu verwenden, öffnen Sie ein neues ActiveX.dll-Projekt, und fügen Sie Verweise auf die Microsoft ActiveX Data Objects-Bibliothek und die Typbibliothek für COM+-Dienste hinzu.

> [!Note]  
> Der Beispielcode in dieser Einführung dient zur Veranschaulichung und ist möglicherweise nicht die effizienteste Lösung für die tatsächliche Staging-und Produktionsumgebung.

 


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

-   Com+ weist Standard Attributwerte zu. Die meisten Dienst Attribute können neu konfiguriert werden.
-   Durch Festlegen des Transaktions Attributs für eine Komponente auf " **erforderlich** " wird sichergestellt, dass com+ jede Instanz dieser Komponente in einer Transaktion erstellen muss, aber nicht notwendigerweise eine neue Transaktion startet.
-   Das Überprüfen des Vorhandenseins einer Transaktion bestätigt, dass der Wert des Transaktions Attributs der Komponente nicht versehentlich auf einen nicht transaktionalen Wert zurückgesetzt wurde, wie z. b. **Ignore** oder **nicht unterstützt**.
-   Durch die Behandlung von Fehlern wird Ihre Komponente zuverlässiger und leichter zu beheben.
-   Com+ erzwingt [JIT-Aktivierungs](com--just-in-time-activation.md) -und Parallelitäts [Schutz](com--synchronization.md) -Dienste für Transaktions Komponenten.
-   Wenn Sie die Datenbankverbindung schließen, wenn Sie damit abgeschlossen sind, kann eine andere Komponente in derselben Transaktion die Verbindung aus dem Verbindungspool wieder verwenden. (Das Verbindungspooling sollte nicht mit dem [Objekt Pooling](com--object-pooling.md)verwechselt werden.)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schritt 2: Erweitern einer Transaktion über mehrere Komponenten hinweg](step-2--extending-a-transaction-across-multiple-components.md)
</dt> <dt>

[Schritt 3: wieder verwenden von Komponenten](step-3--reusing-components.md)
</dt> <dt>

[Just-in-Time-Aktivierung von com+](com--just-in-time-activation.md)
</dt> <dt>

[Com+-Synchronisierung](com--synchronization.md)
</dt> <dt>

[Konfigurieren von Transaktionen](configuring-transactions.md)
</dt> <dt>

[Com+-Anwendungen werden erstellt.](creating-com--applications.md)
</dt> <dt>

[Festlegen des Transaktions Attributs](setting-the-transaction-attribute.md)
</dt> </dl>

 

 



