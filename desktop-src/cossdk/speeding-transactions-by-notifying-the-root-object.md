---
description: Beschleunigen von Transaktionen durch Benachrichtigen des root-Objekts
ms.assetid: 5737324a-65e5-4a39-b325-762768e171a1
title: Beschleunigen von Transaktionen durch Benachrichtigen des root-Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f3865382434ee070db753a0f9113577531558d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214117"
---
# <a name="speeding-transactions-by-notifying-the-root-object"></a><span data-ttu-id="b5efe-103">Beschleunigen von Transaktionen durch Benachrichtigen des root-Objekts</span><span class="sxs-lookup"><span data-stu-id="b5efe-103">Speeding Transactions by Notifying the Root Object</span></span>

<span data-ttu-id="b5efe-104">Um automatische Transaktionen effektiv zu verwenden, sollte jede Transaktions Komponente angeben, dass Sie Ihre Arbeit abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="b5efe-104">To use automatic transactions effectively, each transactional component should indicate that it has completed its work.</span></span> <span data-ttu-id="b5efe-105">Wenn eine Objektinstanz die Aufgabe erfolgreich abgeschlossen hat, sollte Sie Ihre konsistenten und done-Flags auf true festlegen, indem Sie die [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="b5efe-105">When an object instance completes its task successfully, it should set its consistent and done flags to True by calling the [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) method.</span></span> <span data-ttu-id="b5efe-106">Wenn alle inneren Objekte der Transaktion **SetComplete** aufgerufen haben, kann die Transaktion beendet werden, indem das Stamm Objekt durch Aufrufen der **SetComplete** -Methode explizit deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="b5efe-106">When all of the interior objects of the transaction have called **SetComplete**, the transaction can be terminated by explicitly deactivating the root object by calling its **SetComplete** method.</span></span> <span data-ttu-id="b5efe-107">Wenn Sie explizit angeben, dass ein Stamm Objekt seine Arbeit abgeschlossen hat, können Sie die Länge der Transaktion reduzieren.</span><span class="sxs-lookup"><span data-stu-id="b5efe-107">By explicitly indicating that a root object has completed its work, you can reduce the length of the transaction.</span></span>

<span data-ttu-id="b5efe-108">Wenn eine transaktionale Objektmethode fehlschlägt, sollte das Objekt das konsistente Flag auf false und das done-Flag auf true festlegen, indem die [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b5efe-108">When a transactional object method fails, the object should set its consistent flag to False and its done flag to True by calling the [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) method.</span></span> <span data-ttu-id="b5efe-109">Durch Aufrufen der **SetAbort** -Methode gibt ein Objekt die Steuerung an seinen Aufrufer zurück und stellt sicher, dass die Transaktion letztendlich abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="b5efe-109">By calling the **SetAbort** method, an object returns control to its caller and ensures that the transaction is ultimately aborted.</span></span>

<span data-ttu-id="b5efe-110">Es sei denn, das Objekt, von dem [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) aufgerufen wird, ist der Stamm der Transaktion. die Transaktion wird jedoch weiterhin ausgeführt, auch wenn Sie Sie nicht speichern kann.</span><span class="sxs-lookup"><span data-stu-id="b5efe-110">However, unless the object calling [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) is the root of the transaction, the transaction continues to run even though nothing can save it from eventually aborting.</span></span> <span data-ttu-id="b5efe-111">Um die Beendigung einer fehlgeschlagenen Transaktion zu beschleunigen, können Sie einen Fehler generieren, um das Stamm Objekt darauf hinzuweisen, dass auch **SetAbort** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b5efe-111">To speed up the termination of a failed transaction, you can raise an error to alert the root object to also call **SetAbort**.</span></span> <span data-ttu-id="b5efe-112">Zum Abschluss sollte das Stamm Objekt dann eine Fehlermeldung an den Client senden.</span><span class="sxs-lookup"><span data-stu-id="b5efe-112">For completion, the root object should then send an error message to its client.</span></span>

<span data-ttu-id="b5efe-113">Obwohl es viele verschiedene Ansätze gibt, die Sie zur Behandlung von Fehlern verwenden können, sollte Ihr Ansatz die Kommunikation zwischen inneren Objekten und dem Stamm Objekt eindeutig koordinieren.</span><span class="sxs-lookup"><span data-stu-id="b5efe-113">While there are many different approaches you can take to handle errors, your approach should clearly coordinate the communications between interior objects and the root object.</span></span>

<span data-ttu-id="b5efe-114">Die folgenden Visual Basic Code Fragmente zeigen einen Ansatz für die Fehlerbehandlung.</span><span class="sxs-lookup"><span data-stu-id="b5efe-114">The following Visual Basic code fragments show one approach to error handling.</span></span> <span data-ttu-id="b5efe-115">Im ersten Fragment Ruft ein inneres Objekt [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)auf, löst einen Fehler aus und generiert eine Fehlermeldung wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b5efe-115">In the first fragment, an interior object calls [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), raises an error, and generates an error message, as follows:</span></span>

``` syntax
Dim ObjCtx As ObjectContext
Dim ErrorCode As Long, Description As String

Set ObjCtx = GetObjectContext()
ObjCtx.SetAbort
ErrorCode = vbObjectError + 5
Description = "Some meaningful message"
Err.Raise ErrorCode, , Description
```

<span data-ttu-id="b5efe-116">Im zweiten Fragment verarbeitet das Stamm Objekt den Fehler und übergibt die Nachricht wie folgt an den Client:</span><span class="sxs-lookup"><span data-stu-id="b5efe-116">In the second fragment, the root object handles the error and passes the message to its client, as follows:</span></span>

``` syntax
Sub MyObjMethod1()
  On Error GoTo MyObjMethod1_err
  Dim ObjCtx As ObjectContext
  Dim InteriorObj1 As Cinterior  ' Cinterior is a user-defined object.

  Set ObjCtx = GetObjectContext()
  Set InteriorObj1 = CreateObject ("MyDll.Cinterior")
  InteriorObj1.Method1
  ' If the call completed successfully, then...
  ObjCtx.SetComplete
Exit Sub
  MyObjMethod1_err:
  ' Doom the transaction and exit.
  ObjCtx.SetAbort
  ' Pass the message back to client.
  Err.Raise Err.Number, , Err.Description
End Sub
```

## <a name="related-topics"></a><span data-ttu-id="b5efe-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b5efe-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5efe-118">Verwalten von automatischen Transaktionen in com+</span><span class="sxs-lookup"><span data-stu-id="b5efe-118">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



