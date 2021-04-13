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
# <a name="step-2-extending-a-transaction-across-components"></a>Schritt 2: Erweitern einer Transaktion über Komponenten hinweg

## <a name="objectives"></a>Ziele

In diesem Schritt erfahren Sie mehr über Folgendes:

-   Transaktions Fluss
-   Abstimmen von mehreren Objekten in einer Transaktion

## <a name="description"></a>BESCHREIBUNG

[Schritt 1: Erstellen einer transaktionalen Komponente](step-1--creating-a-transactional-component.md) zeigt, wie Sie eine einfache Transaktions Komponente schreiben, die Autoreninformationen in der Microsoft SQL Server pubs-Datenbank aktualisiert. Schritt 2 zeigt, was geschieht, wenn eine Transaktion über mehrere Komponenten hinweg erweitert wird.

Unter Beibehaltung des com+-Programmiermodells `UpdateAuthorAddress` Ruft eine andere Komponente im Verlauf der Arbeit auf. Die zweite Komponente, `ValidateAuthorAddress` , überprüft die Adresse des Autors und gibt die Ergebnisse an den Aufrufer zurück `UpdateAuthorAddress` .

Im Gegensatz zum Aufrufer ist `ValidateAuthorAddress` keine Transaktion erforderlich, kann aber dennoch an der Transaktion des Aufrufers teilnehmen. In diesem Schritt wird der Wert des Transaktions Attributs auf **unterstützt** festgelegt, wie in der folgenden Abbildung gezeigt, die die vorhandene Transaktion auf das neue Objekt erweitert.

![Diagramm, das die Erweiterung der vorhandenen Transaktion auf das neue Objekt anzeigt.](images/f58acb34-55db-40a4-8c48-f51ad024ff7e.png)

Der **unterstützte** Attribut Wert erweitert (oder fließt) eine vorhandene Transaktion nur, wenn der Aufrufer transaktional ist. Bei `UpdateAuthorAddress` Aufrufen von `ValidateAuthorAddress` prüft com+ zuerst den Kontext des Aufrufers, um zu sehen, ob er transaktional ist. Com+ prüft dann die Dienst Attribute, die für festgelegt sind, `ValidateAuthorAddress` und weist das neue-Objekt dem gleichen Transaktions Bezeichner zu, der dem Aufruferobjekt zugewiesen ist. Informationen zum besseren Verständnis dieses Prozesses finden Sie unter [Kontext Aktivierung](context-activation.md).

Da Sie denselben Transaktions Bezeichner gemeinsam nutzen, müssen beide Objekte ihre Arbeit erfolgreich abgeschlossen haben, oder com+ bricht die Transaktion ab (macht Änderungen an der pubs-Datenbank nicht mehr erforderlich).

Alle Objekte, die an einer Transaktion teilnehmen, Stimmen ab, um die Transaktion zu committen oder abzubrechen. Die Abstimmung erfolgt explizit, wenn Sie Abstimmungsanweisungen in Ihren Code einschließen, wie in der folgenden Extraktion aus dem Schritt 1-Beispielcode gezeigt, der die- `UpdateAuthorAddress` Komponente erstellt:


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



Die Abstimmung erfolgt auch implizit, wie es in der Komponente der Fall ist `ValidateAuthorAddress` . Wenn das-Objekt nicht anderweitig deklariert, geht com+ davon aus, dass ein Objekt seine Arbeit erfolgreich abgeschlossen hat, aber nicht für die Deaktivierung bereit ist. Com+ nimmt die folgende Annahme an:


```VB
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn False
```



Wenn `ValidateAuthorAddress` an seinen Aufrufer zurückkehrt, liest com+ seine Stimme als Commit. Com+ zählt die Stimmen erst, wenn das Stamm Objekt deaktiviert wird, das das erste Objekt in der Transaktion ist, in diesem Fall das- `UpdateAuthorAddress` Objekt.

## <a name="sample-code"></a>Beispielcode

Die `ValidateAuthorAddress` Komponente führt eine einfache Überprüfung der Adresse des Autors durch. Da `UpdateAuthorAddress` nicht explizit abgestimmt, verwendet com+ die standardmäßigen Abstimmungs Einstellungen.


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



## <a name="summary"></a>Zusammenfassung

-   Das Festlegen des Transaktions Attributs für eine Komponente auf " **unterstützt** " kann dazu führen, dass das neue Objekt in der Transaktion des aufrufenden Objekts erstellt wird. Com+ prüft den Kontext des Aufrufers, um den Transaktionsstatus des neuen Objekts zu bestimmen. Wenn der Aufrufer transaktional ist, fließt com+ die Transaktion an das neue-Objekt.
-   Alle Objekte, die an derselben Transaktion teilnehmen, haben eine gemeinsame Transaktions-ID, die von com+ aus dem Kontext des Objekts gelesen wird.
-   Jedes Objekt in einer Transaktion Stimmen unabhängig von anderen Objekten ab. Com+ zählt die Stimmen, wenn das Stamm Objekt deaktiviert wird.
-   Sie können die Transaktions Stimme eines Objekts zwischen Commit und Abbrechen umschalten, bis com+ das Objekt deaktiviert oder das Stamm Objekt von com+ deaktiviert und die Transaktion beendet wird. Nur die Einstellung für die letzte Stimme wird gezählt. Die Schnittstellen [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) und [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) stellen Methoden bereit, die ähnliche Abstimmungsergebnisse wie in der folgenden Tabelle dargestellt erstellen. Sie können beide Schnittstellen verwenden, um in einer Transaktion explizit abzustimmen. 

    | [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) -Kombinations Methoden                                                                                                                                                      | [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) -äquivalente Methode       |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
    | [**Setmytransaktionvote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txvote*-  =  **txcommit**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeaktivieren*  =  **true**<br/>  | [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     |
    | [**Setmytransaktionvote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txvote*-  =  **txcommit**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeaktivieren*  =  **false**<br/> | [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   |
    | [**Setmytransaktionvote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txvote*  =  **txabort**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeaktivieren*  =  **true**<br/>   | [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           |
    | [**Setmytransaktionvote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txvote*  =  **txabort**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeaktivieren*  =  **false**<br/>  | [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> |

    

     

-   Com+ legt die Stimme eines Objekts auf das Äquivalent von [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) fest, es sei denn, die Komponente stimmt explizit überein.
-   Wenn Sie explizit abstimmen, kann die Gesamtdauer der Transaktion reduziert und teure Ressourcen Sperren freigegeben werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schritt 1: Erstellen einer transaktionalen Komponente](step-1--creating-a-transactional-component.md)
</dt> <dt>

[Schritt 3: wieder verwenden von Komponenten](step-3--reusing-components.md)
</dt> <dt>

[Kontext Aktivierung](context-activation.md)
</dt> <dt>

[Verwalten von automatischen Transaktionen in com+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 




