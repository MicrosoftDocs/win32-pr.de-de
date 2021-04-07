---
description: Verwenden von nicht transaktionalen Komponenten in einer Transaktion
ms.assetid: b83b4bab-1851-48dc-b35a-6467a6dff741
title: Verwenden von nicht transaktionalen Komponenten in einer Transaktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75cd8ebc756971a56413e371cf23de2144e5816
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748992"
---
# <a name="using-non-transactional-components-in-a-transaction"></a>Verwenden von nicht transaktionalen Komponenten in einer Transaktion

Es ist häufig nützlich, nicht transaktionale Komponenten in eine Transaktion zu platzieren, um die Acid- [Eigenschaften](acid-properties.md) von Transaktionen zu nutzen. Wenn Sie z. b. über nicht transaktionale Legacy Komponenten verfügen, die Sie zum Aktualisieren von Kenn Wörtern in einem Netzwerk verwenden, können Sie diese Komponenten in einer Transaktion platzieren, um sicherzustellen, dass Kenn Wort Aktualisierungen im gesamten Netzwerk einheitlich sind.

Das *Transaktionskontext Objekt* ist ein generisches Objekt, das es nicht transaktionalen Clients ermöglicht, die Arbeit mehrerer COM-Objekte in einer einzelnen Transaktion zu kombinieren, ohne dass Sie eine neue Komponente speziell für diesen Zweck entwickeln müssen. Im Gegensatz zu einer automatischen Transaktion erfordert das Transaktionskontext Objekt, dass der Client die Transaktion explizit Committe oder abbricht.

Standardmäßig ist der Wert des Transaktions Attributs des Transaktionskontext Objekts auf Required festgelegt. Com+ bricht die Transaktion ab, wenn der Client das Transaktionskontext Objekt freigibt, ohne einen Commit-oder Abbruch-aufruber explizit auszugeben.

Im folgenden Visual Basic Beispiel wird veranschaulicht, wie ein nicht transaktionaler Client die Arbeit von mehreren Objekten in einer einzelnen Transaktion zusammenstellen kann:


```VB
Dim objTxCtx As TransactionContext
Dim objCat As MyDLL.Ccat  ' Ccat is a user-defined component.
Dim objDog As MyDLL.Cdog  ' Cdog is a user-defined component.

' Get TransactionContext object.
Set objTxCtx = _
  CreateObject ("TxCtx.TransactionContext")

' Create instances of Cat and Dog.
Set objCat = _ 
  objTxCtx.CreateInstance ("MyDLL.Ccat")
Set objDog = _ 
  objTxCtx.CreateInstance ("MyDLL.Cdog")

' Both objects do work.
objDog.Bark
objCat.Hiss

' Commit the transaction.
objTxCtx.Commit

```



## <a name="limitations-of-the-transaction-context-object"></a>Einschränkungen des Transaktionskontext Objekts

Im folgenden sind einige wichtige Einschränkungen des Transaktionskontext Objekts aufgeführt:

-   Wenn ein Transaktionskontext Objekt verwendet wird, ist die Anwendungslogik, die die Arbeit mehrerer Objekte in einer einzigen Transaktion kombiniert, an eine bestimmte nicht transaktionale Client Implementierung gebunden, und einige Vorteile der Verwendung von COM-Komponenten gehen verloren. Zu diesen verlorenen Vorteilen zählen die folgenden:
    -   Möglichkeit zur Wiederverwendung der Anwendungslogik als Teil einer noch größeren Transaktion
    -   Auferlegung deklarativer Sicherheit
    -   Flexibilität beim Remote Ausführen der Logik vom Client
-   Das Transaktionskontext Objekt wird innerhalb des Prozesses mit dem nicht transaktionalen Client ausgeführt, was bedeutet, dass com+ auf dem nicht transaktionalen Client Computer verfügbar sein muss. Dies ist möglicherweise kein Problem, z. b. wenn das Transaktionskontext Objekt von einer Seite mit Active Server Pages (ASP) verwendet wird, die auf demselben Server wie com+ ausgeführt wird.
-   Sie erhalten keinen Kontext für den nicht transaktionalen Client, wenn Sie ein Transaktionskontext Objekt erstellen. Transaktionale arbeiten können nur indirekt über COM-Objekte durchgeführt werden, die mithilfe des Transaktionskontext Objekts erstellt wurden. Insbesondere der nicht transaktionale Client kann keine com+-Ressourcen Spender (z. b. ODBC) verwenden und die Arbeit in der Transaktion enthalten. Beispielsweise können Entwickler mit der folgenden Syntax für transaktionale arbeiten an relationalen Datenbanksystemen vertraut sein:

    ``` syntax
    BEGIN TRANSACTION
      DoWork
    COMMIT TRANSACTION
    ```

    Die Verwendung des Transaktionskontext Objekts auf ähnliche Weise ergibt nicht das gewünschte Ergebnis:

    ``` syntax
    Set objTxCtx = CreateObject ("TxCtx.TransactionContext")
      DoWork
      objTxCtx.Commit
    Set objTxCtx = Nothing
    ```

    Der in diesem Beispiel aufzurufende DoWork-Befehl ist nicht in einer Transaktion eingetragen. Stattdessen müssen Sie eine COM-Komponente erstellen, die DoWork aufruft, eine Objektinstanz dieser Komponente mithilfe des Transaktionskontext Objekts erstellen und dieses Objekt dann vom nicht transaktionalen Client aus aufrufen, damit die Arbeit Teil der Client gesteuerten Transaktion ist.

 

 



