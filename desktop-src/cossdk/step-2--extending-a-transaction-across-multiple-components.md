---
description: 'Schritt 2: Erweitern einer Transaktion auf mehrere Komponenten'
ms.assetid: 20a30e87-e209-45ae-bf1b-722568758c47
title: 'Schritt 2: Erweitern einer Transaktion auf mehrere Komponenten'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96aa168eca7bfba29a4b00a6cd24b45d06c7610c76d47a4d6454e77295e57bc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915807"
---
# <a name="step-2-extending-a-transaction-across-components"></a>Schritt 2: Komponentenübergreifendes Erweitern einer Transaktion

## <a name="objectives"></a>Ziele

In diesem Schritt lernen Sie Folgendes:

-   Transaktionsfluss
-   Abstimmen mehrerer Objekte in einer Transaktion

## <a name="description"></a>BESCHREIBUNG

[Schritt 1: Erstellen](step-1--creating-a-transactional-component.md) einer Transaktionskomponente zeigt, wie Sie eine einfache Transaktionskomponente schreiben, die Autoreninformationen in der Microsoft SQL Server Pubs-Datenbank aktualisiert. Schritt 2 zeigt, was geschieht, wenn eine Transaktion über mehrere Komponenten hinweg erweitert wird.

Im Einklang mit dem COM+-Programmiermodell ruft eine andere Komponente während der Arbeit `UpdateAuthorAddress` auf. Die zweite Komponente, , überprüft die Adresse des Autors und gibt `ValidateAuthorAddress` die Ergebnisse an den Aufrufer zurück. `UpdateAuthorAddress`

Im Gegensatz zu seinem Aufrufer erfordert keine Transaktion, kann aber weiterhin an der Transaktion `ValidateAuthorAddress` des Aufrufers teilnehmen. In diesem Schritt wird der Transaktionsattributwert auf **Unterstützt** festgelegt, wie in der folgenden Abbildung gezeigt, wodurch die vorhandene Transaktion auf das neue -Objekt erweitert wird.

![Diagramm, das das Erweitern der vorhandenen Transaktion auf das neue Objekt zeigt.](images/f58acb34-55db-40a4-8c48-f51ad024ff7e.png)

Der  Supported-Attributwert erweitert (oder fließt) eine vorhandene Transaktion nur, wenn der Aufrufer transaktional ist. Wenn aufruft, untersucht COM+ zuerst den Kontext des Aufrufers, um festzustellen, ob `UpdateAuthorAddress` `ValidateAuthorAddress` er transaktional ist. COM+ untersucht dann die Dienstattribute, die für festgelegt sind, und weist dem neuen Objekt denselben Transaktionsbezeichner zu, der dem `ValidateAuthorAddress` Aufruferobjekt zugewiesen ist. Weitere Informationen zu diesem Prozess finden Sie unter [Kontextaktivierung.](context-activation.md)

Da sie denselben Transaktionsbezeichner verwenden, müssen beide Objekte ihre Arbeit erfolgreich abschließen, oder COM+ bricht die Transaktion ab (macht alle Änderungen rückgängig, die an der Pubs-Datenbank vorgenommen wurden).

Alle An einer Transaktion beteiligten Objekte stimmen für einen Commit oder Abbruch der Transaktion ab. Die Abstimmung erfolgt explizit, wenn Sie Abstimmungsanweisungen in Ihren Code eingeben, wie in der folgenden Extraktion aus dem Schritt 1-Beispielcode gezeigt, der die Komponente `UpdateAuthorAddress` erstellt:


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



Die Abstimmung erfolgt auch implizit, wie dies in der -Komponente `ValidateAuthorAddress` erfolgt. Sofern das -Objekt nicht anders deklariert, geht COM+ davon aus, dass ein Objekt seine Arbeit erfolgreich abgeschlossen hat, aber nicht bereit ist, deaktiviert zu werden. COM+ geht von der folgenden Annahme aus:


```VB
  contextstate.SetMyTransactionVote TxCommit
  contextstate.SetDeactivateOnReturn False
```



Wenn `ValidateAuthorAddress` an den Aufrufer zurückgegeben wird, liest COM+ seine Stimme als Commit. COM+ zählt die Stimmen erst, wenn es das Stammobjekt deaktiviert, das in diesem Fall das erste Objekt in der Transaktion ist, das `UpdateAuthorAddress` -Objekt.

## <a name="sample-code"></a>Beispielcode

Die `ValidateAuthorAddress` Komponente überprüft die Adresse des Autors einfach. Da `UpdateAuthorAddress` nicht explizit abstimme, verwendet COM+ die Standardabstimmungseinstellungen.


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

-   Das Festlegen des Transaktionsattributs einer Komponente auf **Supported** kann dazu führen, dass das neue Objekt in der Transaktion des aufrufenden Objekts erstellt wird. COM+ untersucht den Kontext des Aufrufers, um den Transaktionsstatus des neuen Objekts zu bestimmen. Wenn der Aufrufer transaktional ist, übertrat COM+ die Transaktion an das neue Objekt.
-   Alle Objekte, die an derselben Transaktion teilnehmen, verwenden einen gemeinsamen Transaktionsbezeichner, den COM+ aus dem Kontext des Objekts liest.
-   Jedes Objekt in einer Transaktion stimmt unabhängig von anderen Objekten ab. COM+ zählt die Stimmen, wenn das Stammobjekt deaktiviert wird.
-   Sie können die Transaktionsabstimmung eines Objekts zwischen Commit und Abbruch umschalten, bis COM+ das Objekt deaktiviert, oder bis COM+ das Stammobjekt deaktiviert und die Transaktion beendet. Nur die letzte Abstimmungseinstellung zählt. Die [**Schnittstellen IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) und [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) stellen Methoden bereit und erzeugen ähnliche Abstimmungsergebnisse wie in der folgenden Tabelle gezeigt. Sie können beide Schnittstellen verwenden, um in einer Transaktion explizit zu abstimmen. 

    | [**IContextState-Kombinationsmethoden**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)                                                                                                                                                      | [**Äquivalente IObjectContext-Methode**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)       |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **True**<br/>  | [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     |
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxCommit**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **False**<br/> | [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   |
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxAbort**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **True**<br/>   | [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           |
    | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote*  =  **TxAbort**<br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate*  =  **False**<br/>  | [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> |

    

     

-   COM+ legt die Stimme eines Objekts auf die Entsprechung von [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) fest, es sei denn, die Komponente stimmt explizit ab.
-   Eine explizite Abstimmung kann die Gesamtdauer der Transaktion reduzieren und teure Ressourcensperren frei geben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schritt 1: Erstellen einer Transaktionskomponente](step-1--creating-a-transactional-component.md)
</dt> <dt>

[Schritt 3: Wiederverwendung von Komponenten](step-3--reusing-components.md)
</dt> <dt>

[Kontextaktivierung](context-activation.md)
</dt> <dt>

[Verwalten automatischer Transaktionen in COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 




