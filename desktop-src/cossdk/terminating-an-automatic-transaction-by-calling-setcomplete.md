---
description: Beenden einer automatischen Transaktion durch Aufrufen von SetComplete
ms.assetid: 5bd06cfd-1ee0-48ac-84ab-3737d76bccc0
title: Beenden einer automatischen Transaktion durch Aufrufen von SetComplete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba4bf09e631acf69a9b663d68d7eb82cfaa4490f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344953"
---
# <a name="terminating-an-automatic-transaction-by-calling-setcomplete"></a><span data-ttu-id="79445-103">Beenden einer automatischen Transaktion durch Aufrufen von SetComplete</span><span class="sxs-lookup"><span data-stu-id="79445-103">Terminating an Automatic Transaction by Calling SetComplete</span></span>

<span data-ttu-id="79445-104">Um automatische Transaktionen effektiv zu verwenden, sollte jede Transaktions Komponente angeben, dass Sie Ihre Arbeit abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="79445-104">To use automatic transactions effectively, each transactional component should indicate that it has completed its work.</span></span> <span data-ttu-id="79445-105">Wenn eine Objektinstanz die Aufgabe erfolgreich abgeschlossen hat, sollte Sie Ihre konsistenten und done-Flags auf true festlegen, indem Sie die [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) -Methode aufruft, die über die [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) -Schnittstelle und das [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) -Objekt verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="79445-105">When an object instance completes its task successfully, it should set its consistent and done flags to True by calling the [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) method, which is exposed through both the [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) interface and the [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) object.</span></span>

<span data-ttu-id="79445-106">Die effizienteste Methode zum Ausführen einer automatischen Transaktion besteht darin, das Stamm Objekt mithilfe der [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) -Methode explizit zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="79445-106">The most efficient way to complete an automatic transaction is to explicitly deactivate the root object by using the [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) method.</span></span> <span data-ttu-id="79445-107">Wenn Sie explizit angeben, dass ein Stamm Objekt seine Arbeit abgeschlossen hat, können Sie die Länge der Transaktion reduzieren.</span><span class="sxs-lookup"><span data-stu-id="79445-107">By explicitly indicating that a root object has completed its work, you can reduce the length of the transaction.</span></span>

<span data-ttu-id="79445-108">Im folgenden Visual Basic Beispiel wird gezeigt, wie angegeben wird, dass die Arbeit eines transaktionalen Objekts erfolgreich abgeschlossen wurde:</span><span class="sxs-lookup"><span data-stu-id="79445-108">The following Visual Basic example shows how to indicate that a transactional object has completed its work successfully:</span></span>


```VB
Sub MyObjMethod1()
  Dim ObjCtx As ObjectContext
  Dim InteriorObj1 As Cinterior  ' Cinterior is a user-defined object.

  Set ObjCtx = GetObjectContext()
  Set InteriorObj1 = CreateObject ("MyDll.Cinterior")
  InteriorObj1.Method1
  ' If the call completed successfully, then...
  objCtx.SetComplete
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="79445-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="79445-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79445-110">Konsistente und done-Flags</span><span class="sxs-lookup"><span data-stu-id="79445-110">Consistent and Done Flags</span></span>](consistent-and-done-flags.md)
</dt> <dt>

[<span data-ttu-id="79445-111">Verwalten von automatischen Transaktionen in com+</span><span class="sxs-lookup"><span data-stu-id="79445-111">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



