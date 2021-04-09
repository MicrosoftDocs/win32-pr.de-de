---
title: Abbrechen eines asynchronen Aufrufes
description: Ein Client kann einen asynchronen Aufruf abbrechen, der gerade ausgeführt wird, wenn das Aufruf Objekt die icancelmethodcalls-Schnittstelle implementiert.
ms.assetid: 30a162f2-ce16-4ee6-8002-59216ac0e59a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775b187f1abd3fca43ba907d92f6eabd926e4608
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102423"
---
# <a name="canceling-an-asynchronous-call"></a><span data-ttu-id="111ed-103">Abbrechen eines asynchronen Aufrufes</span><span class="sxs-lookup"><span data-stu-id="111ed-103">Canceling an Asynchronous Call</span></span>

<span data-ttu-id="111ed-104">Ein Client kann einen asynchronen Aufruf abbrechen, der gerade ausgeführt wird, wenn das Aufruf Objekt die [**icancelmethodcalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="111ed-104">A client can cancel an asynchronous call that is in progress if the call object implements the [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) interface.</span></span> <span data-ttu-id="111ed-105">Bei Objekten, die Standardmäßiges Marshalling verwenden, ist **icancelmethodcalls** immer für gemarshallte Aufrufe verfügbar.</span><span class="sxs-lookup"><span data-stu-id="111ed-105">For objects that use standard marshaling, **ICancelMethodCalls** is always available for marshaled calls.</span></span> <span data-ttu-id="111ed-106">Bei Objekten, die benutzerdefiniertes Marshalling oder Aufrufe von Server Objekten innerhalb desselben Apartment verwenden, ist diese Funktion nur verfügbar, wenn das Aufruf Objekt **icancelmethodcalls** implementiert.</span><span class="sxs-lookup"><span data-stu-id="111ed-106">For objects that use custom marshaling or for calls to server objects within the same apartment, this functionality is available only if the call object implements **ICancelMethodCalls**.</span></span>

<span data-ttu-id="111ed-107">Der Client kann den Aufruf jederzeit abbrechen, von dem Zeitpunkt, an dem die BEGIN- \_ Methode aufgerufen wird, bis die Finish- \_ Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="111ed-107">The client can cancel the call at any time, from when the Begin\_ method is called until the Finish\_ method returns.</span></span> <span data-ttu-id="111ed-108">Wenn der Client den Aufruf vor dem Aufrufen der Methode "Finish" \_ abbricht, muss er die "Finish"-Methode aufrufen, \_ um den Status des Aufruf Objekts zu bereinigen.</span><span class="sxs-lookup"><span data-stu-id="111ed-108">If the client cancels the call before calling the Finish\_ method, it must call the Finish\_ method to clean up the state of the call object.</span></span> <span data-ttu-id="111ed-109">Solange der Client dies nicht erreicht hat, geben alle Aufrufe einer beliebigen BEGIN- \_ Methode für das Aufruf Objekt einen RPC- \_ E- \_ Aufruf \_ aus.</span><span class="sxs-lookup"><span data-stu-id="111ed-109">Until the client has done so, any calls to any Begin\_ method on the call object will return RPC\_E\_CALL\_PENDING.</span></span>

<span data-ttu-id="111ed-110">**So brechen Sie einen asynchronen-Befehl ab**</span><span class="sxs-lookup"><span data-stu-id="111ed-110">**To cancel an asynchronous call**</span></span>

1.  <span data-ttu-id="111ed-111">Fragen Sie das Aufruf Objekt für [**icancelmethodcalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls)ab.</span><span class="sxs-lookup"><span data-stu-id="111ed-111">Query the call object for [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls).</span></span>

2.  <span data-ttu-id="111ed-112">Rufen Sie [**icancelmethodcalls:: Cancel**](/windows/win32/api/objidlbase/nf-objidlbase-icancelmethodcalls-cancel)auf, und rufen Sie dann [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) auf, um den Zeiger freizugeben, den der [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) -Aufruf in Schritt 1 erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="111ed-112">Call [**ICancelMethodCalls::Cancel**](/windows/win32/api/objidlbase/nf-objidlbase-icancelmethodcalls-cancel), and then call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release the pointer obtained by the [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) call in step 1.</span></span>

3.  <span data-ttu-id="111ed-113">Wenn der Client die "Finish"- \_ Methode nicht bereits aufgerufen hat, nennen Sie ihn jetzt.</span><span class="sxs-lookup"><span data-stu-id="111ed-113">If the client has not called the Finish\_ method already, call it now.</span></span>

<span data-ttu-id="111ed-114">Es gibt keine Garantie dafür, dass der Server die Ausführung des Aufrufes tatsächlich beendet hat.</span><span class="sxs-lookup"><span data-stu-id="111ed-114">There is no guarantee that the server actually stopped execution of the call.</span></span> <span data-ttu-id="111ed-115">Wenn die weitere Arbeit des Clients von einem Serverstatus abhängig ist, den der-Rückruf möglicherweise geändert hat, sollte der Client diesen Zustand vor dem Fortfahren ermitteln.</span><span class="sxs-lookup"><span data-stu-id="111ed-115">If the client's further work depends on some server state that the call may or may not have changed, the client should determine that state before proceeding.</span></span>

## <a name="related-topics"></a><span data-ttu-id="111ed-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="111ed-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="111ed-117">Ausführen eines asynchronen Aufrufes</span><span class="sxs-lookup"><span data-stu-id="111ed-117">Making an Asynchronous Call</span></span>](making-an-asynchronous-call.md)
</dt> </dl>

 

 