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
# <a name="using-non-transactional-components-in-a-transaction"></a><span data-ttu-id="5c325-103">Verwenden von nicht transaktionalen Komponenten in einer Transaktion</span><span class="sxs-lookup"><span data-stu-id="5c325-103">Using Non-Transactional Components in a Transaction</span></span>

<span data-ttu-id="5c325-104">Es ist häufig nützlich, nicht transaktionale Komponenten in eine Transaktion zu platzieren, um die Acid- [Eigenschaften](acid-properties.md) von Transaktionen zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="5c325-104">It is often useful to place non-transactional components into a transaction to take advantage of the [ACID properties](acid-properties.md) of transactions.</span></span> <span data-ttu-id="5c325-105">Wenn Sie z. b. über nicht transaktionale Legacy Komponenten verfügen, die Sie zum Aktualisieren von Kenn Wörtern in einem Netzwerk verwenden, können Sie diese Komponenten in einer Transaktion platzieren, um sicherzustellen, dass Kenn Wort Aktualisierungen im gesamten Netzwerk einheitlich sind.</span><span class="sxs-lookup"><span data-stu-id="5c325-105">For example, if you have non-transactional legacy components that you use to update passwords on a network, you can place those components in a transaction to ensure that password updates are consistent across the network.</span></span>

<span data-ttu-id="5c325-106">Das *Transaktionskontext Objekt* ist ein generisches Objekt, das es nicht transaktionalen Clients ermöglicht, die Arbeit mehrerer COM-Objekte in einer einzelnen Transaktion zu kombinieren, ohne dass Sie eine neue Komponente speziell für diesen Zweck entwickeln müssen.</span><span class="sxs-lookup"><span data-stu-id="5c325-106">The *transaction context object* is a generic object that allows non-transactional clients to combine the work of multiple COM objects into a single transaction, without requiring you to develop a new component specifically for that purpose.</span></span> <span data-ttu-id="5c325-107">Im Gegensatz zu einer automatischen Transaktion erfordert das Transaktionskontext Objekt, dass der Client die Transaktion explizit Committe oder abbricht.</span><span class="sxs-lookup"><span data-stu-id="5c325-107">In contrast to an automatic transaction, the transaction context object requires its client to explicitly commit or abort the transaction.</span></span>

<span data-ttu-id="5c325-108">Standardmäßig ist der Wert des Transaktions Attributs des Transaktionskontext Objekts auf Required festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5c325-108">By default, the transaction attribute value of the transaction context object is set to Required.</span></span> <span data-ttu-id="5c325-109">Com+ bricht die Transaktion ab, wenn der Client das Transaktionskontext Objekt freigibt, ohne einen Commit-oder Abbruch-aufruber explizit auszugeben.</span><span class="sxs-lookup"><span data-stu-id="5c325-109">COM+ aborts the transaction if the client releases the transaction context object without explicitly issuing a commit or abort call.</span></span>

<span data-ttu-id="5c325-110">Im folgenden Visual Basic Beispiel wird veranschaulicht, wie ein nicht transaktionaler Client die Arbeit von mehreren Objekten in einer einzelnen Transaktion zusammenstellen kann:</span><span class="sxs-lookup"><span data-stu-id="5c325-110">The following Visual Basic example shows how a non-transactional client can compose the work done by more than one object into a single transaction:</span></span>


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



## <a name="limitations-of-the-transaction-context-object"></a><span data-ttu-id="5c325-111">Einschränkungen des Transaktionskontext Objekts</span><span class="sxs-lookup"><span data-stu-id="5c325-111">Limitations of the Transaction Context Object</span></span>

<span data-ttu-id="5c325-112">Im folgenden sind einige wichtige Einschränkungen des Transaktionskontext Objekts aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="5c325-112">Following are some important limitations of the transaction context object:</span></span>

-   <span data-ttu-id="5c325-113">Wenn ein Transaktionskontext Objekt verwendet wird, ist die Anwendungslogik, die die Arbeit mehrerer Objekte in einer einzigen Transaktion kombiniert, an eine bestimmte nicht transaktionale Client Implementierung gebunden, und einige Vorteile der Verwendung von COM-Komponenten gehen verloren.</span><span class="sxs-lookup"><span data-stu-id="5c325-113">When using a transaction context object, the application logic that combines the work of multiple objects into a single transaction is tied to a specific non-transactional client implementation and some advantages of using COM components are lost.</span></span> <span data-ttu-id="5c325-114">Zu diesen verlorenen Vorteilen zählen die folgenden:</span><span class="sxs-lookup"><span data-stu-id="5c325-114">These lost advantages include the following:</span></span>
    -   <span data-ttu-id="5c325-115">Möglichkeit zur Wiederverwendung der Anwendungslogik als Teil einer noch größeren Transaktion</span><span class="sxs-lookup"><span data-stu-id="5c325-115">Ability to reuse the application logic as part of an even larger transaction</span></span>
    -   <span data-ttu-id="5c325-116">Auferlegung deklarativer Sicherheit</span><span class="sxs-lookup"><span data-stu-id="5c325-116">Imposition of declarative security</span></span>
    -   <span data-ttu-id="5c325-117">Flexibilität beim Remote Ausführen der Logik vom Client</span><span class="sxs-lookup"><span data-stu-id="5c325-117">Flexibility to run the logic remotely from the client</span></span>
-   <span data-ttu-id="5c325-118">Das Transaktionskontext Objekt wird innerhalb des Prozesses mit dem nicht transaktionalen Client ausgeführt, was bedeutet, dass com+ auf dem nicht transaktionalen Client Computer verfügbar sein muss.</span><span class="sxs-lookup"><span data-stu-id="5c325-118">The transaction context object runs in-process with the non-transactional client, which means that COM+ must be available on the non-transactional client computer.</span></span> <span data-ttu-id="5c325-119">Dies ist möglicherweise kein Problem, z. b. wenn das Transaktionskontext Objekt von einer Seite mit Active Server Pages (ASP) verwendet wird, die auf demselben Server wie com+ ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5c325-119">This might not be a problem, for example, when the transaction context object is used from an Active Server Pages (ASP) page that is running on the same server as COM+.</span></span>
-   <span data-ttu-id="5c325-120">Sie erhalten keinen Kontext für den nicht transaktionalen Client, wenn Sie ein Transaktionskontext Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="5c325-120">You do not get a context for the non-transactional client when you create a transaction context object.</span></span> <span data-ttu-id="5c325-121">Transaktionale arbeiten können nur indirekt über COM-Objekte durchgeführt werden, die mithilfe des Transaktionskontext Objekts erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="5c325-121">Transactional work can only be done indirectly, through COM objects created by using the transaction context object.</span></span> <span data-ttu-id="5c325-122">Insbesondere der nicht transaktionale Client kann keine com+-Ressourcen Spender (z. b. ODBC) verwenden und die Arbeit in der Transaktion enthalten.</span><span class="sxs-lookup"><span data-stu-id="5c325-122">In particular, the non-transactional client cannot use COM+ resource dispensers (such as ODBC) and have the work included in the transaction.</span></span> <span data-ttu-id="5c325-123">Beispielsweise können Entwickler mit der folgenden Syntax für transaktionale arbeiten an relationalen Datenbanksystemen vertraut sein:</span><span class="sxs-lookup"><span data-stu-id="5c325-123">For example, developers may be familiar with the following syntax for doing transactional work on relational database systems:</span></span>

    ``` syntax
    BEGIN TRANSACTION
      DoWork
    COMMIT TRANSACTION
    ```

    <span data-ttu-id="5c325-124">Die Verwendung des Transaktionskontext Objekts auf ähnliche Weise ergibt nicht das gewünschte Ergebnis:</span><span class="sxs-lookup"><span data-stu-id="5c325-124">Using the transaction context object in a similar way does not yield the desired result:</span></span>

    ``` syntax
    Set objTxCtx = CreateObject ("TxCtx.TransactionContext")
      DoWork
      objTxCtx.Commit
    Set objTxCtx = Nothing
    ```

    <span data-ttu-id="5c325-125">Der in diesem Beispiel aufzurufende DoWork-Befehl ist nicht in einer Transaktion eingetragen.</span><span class="sxs-lookup"><span data-stu-id="5c325-125">The call to DoWork in this example is not enlisted in a transaction.</span></span> <span data-ttu-id="5c325-126">Stattdessen müssen Sie eine COM-Komponente erstellen, die DoWork aufruft, eine Objektinstanz dieser Komponente mithilfe des Transaktionskontext Objekts erstellen und dieses Objekt dann vom nicht transaktionalen Client aus aufrufen, damit die Arbeit Teil der Client gesteuerten Transaktion ist.</span><span class="sxs-lookup"><span data-stu-id="5c325-126">Instead, you must build a COM component that calls DoWork, create an object instance of that component using the transaction context object, and then call that object from the non-transactional client for the work to be part of the client-controlled transaction.</span></span>

 

 



