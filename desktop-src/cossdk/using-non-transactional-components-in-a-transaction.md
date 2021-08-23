---
description: Verwenden nicht transaktionaler Komponenten in einer Transaktion
ms.assetid: b83b4bab-1851-48dc-b35a-6467a6dff741
title: Verwenden nicht transaktionaler Komponenten in einer Transaktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365cf6f8e5c20f328f4308366e9a98916d9277363bba815fdbc00b5e2d8203d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991350"
---
# <a name="using-non-transactional-components-in-a-transaction"></a>Verwenden nicht transaktionaler Komponenten in einer Transaktion

Häufig ist es hilfreich, nicht transaktionale Komponenten in eine Transaktion zu platzieren, um die [ACID-Eigenschaften von](acid-properties.md) Transaktionen zu nutzen. Wenn Sie beispielsweise über nicht transaktionale Legacykomponenten verfügen, die Sie zum Aktualisieren von Kennwörtern in einem Netzwerk verwenden, können Sie diese Komponenten in einer Transaktion platzieren, um sicherzustellen, dass Kennwortupdates im gesamten Netzwerk konsistent sind.

Das *Transaktionskontextobjekt* ist ein generisches Objekt, das es nicht transaktionalen Clients ermöglicht, die Arbeit mehrerer COM-Objekte in einer einzelnen Transaktion zu kombinieren, ohne dass Sie speziell für diesen Zweck eine neue Komponente entwickeln müssen. Im Gegensatz zu einer automatischen Transaktion erfordert das Transaktionskontextobjekt, dass sein Client einen expliziten Commit oder Abbruch der Transaktion ausgeführt hat.

Standardmäßig ist der Transaktionsattributwert des Transaktionskontextobjekts auf Erforderlich festgelegt. COM+ bricht die Transaktion ab, wenn der Client das Transaktionskontextobjekt ohne expliziten Commit- oder Abbruchaufruf frei gibt.

Das folgende Visual Basic zeigt, wie ein nicht transaktionaler Client die Arbeit, die von mehr als einem -Objekt ausgeführt wird, in einer einzelnen Transaktion zusammenstellen kann:


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



## <a name="limitations-of-the-transaction-context-object"></a>Einschränkungen des Transaktionskontextobjekts

Im Folgenden finden Sie einige wichtige Einschränkungen des Transaktionskontextobjekts:

-   Bei Verwendung eines Transaktionskontextobjekts ist die Anwendungslogik, die die Arbeit mehrerer Objekte in einer einzelnen Transaktion kombiniert, an eine bestimmte nicht transaktionale Clientimplementierung gebunden, und einige Vorteile der Verwendung von COM-Komponenten gehen verloren. Zu diesen vorteilen, die verloren gegangen sind, gehören die folgenden:
    -   Möglichkeit zur Wiederverwendung der Anwendungslogik als Teil einer noch größeren Transaktion
    -   Einführung der deklarativen Sicherheit
    -   Flexibilität beim Remote ausführen der Logik über den Client
-   Das Transaktionskontextobjekt wird im Prozess mit dem nicht transaktionalen Client ausgeführt, was bedeutet, dass COM+ auf dem nicht transaktionalen Clientcomputer verfügbar sein muss. Dies kann beispielsweise kein Problem darstellen, wenn das Transaktionskontextobjekt von einer ASP-Seite (Active Server Pages) verwendet wird, die auf demselben Server wie COM+ ausgeführt wird.
-   Sie erhalten keinen Kontext für den nicht transaktionalen Client, wenn Sie ein Transaktionskontextobjekt erstellen. Transaktionale Arbeit kann nur indirekt über COM-Objekte erfolgen, die mithilfe des Transaktionskontextobjekts erstellt wurden. Insbesondere kann der nicht transaktionale Client keine COM+-Ressourcenverzehrer (z. B. ODBC) verwenden und die Arbeit in der Transaktion enthalten. Entwickler können z. B. mit der folgenden Syntax für transaktionale Arbeit auf relationalen Datenbanksystemen vertraut sein:

    ``` syntax
    BEGIN TRANSACTION
      DoWork
    COMMIT TRANSACTION
    ```

    Die Verwendung des Transaktionskontextobjekts auf ähnliche Weise führt nicht zum gewünschten Ergebnis:

    ``` syntax
    Set objTxCtx = CreateObject ("TxCtx.TransactionContext")
      DoWork
      objTxCtx.Commit
    Set objTxCtx = Nothing
    ```

    Der Aufruf von DoWork in diesem Beispiel ist nicht in einer Transaktion eingetragen. Stattdessen müssen Sie eine COM-Komponente erstellen, die DoWork aufruft, eine Objektinstanz dieser Komponente mithilfe des Transaktionskontextobjekts erstellen und dieses Objekt dann vom nicht transaktionalen Client aufrufen, damit die Arbeit Teil der clientgesteuerten Transaktion ist.

 

 



