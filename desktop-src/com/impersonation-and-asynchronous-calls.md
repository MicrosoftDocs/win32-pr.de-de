---
title: Identitätswechsel und asynchrone Aufrufe
description: Identitätswechsel und asynchrone Aufrufe
ms.assetid: 7eaa0a66-7a80-4831-b0b6-b8eff4abd036
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0854946b619f7580173ffcbc97c9af3f2540361b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730680"
---
# <a name="impersonation-and-asynchronous-calls"></a><span data-ttu-id="96a77-103">Identitätswechsel und asynchrone Aufrufe</span><span class="sxs-lookup"><span data-stu-id="96a77-103">Impersonation and Asynchronous Calls</span></span>

<span data-ttu-id="96a77-104">Der Server kann die Identität des Clients nicht annehmen, nachdem der [**isynchronize:: Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal) -Aufrufe des Servers abgeschlossen wurde, auch wenn die BEGIN- \_ Methode noch nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="96a77-104">The server cannot impersonate the client after the server's call to [**ISynchronize::Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal) completes, even if the Begin\_ method has not yet completed.</span></span> <span data-ttu-id="96a77-105">Angenommen, ein Client ruft die BEGIN- \_ Methode auf, der Server verarbeitet den Aufruf sofort und der Server Ruft ein **Signal** auf, um anzugeben, dass die Verarbeitung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="96a77-105">For example, suppose a client calls the Begin\_ method, the server processes the call immediately, and the server calls **Signal** to indicate it is finished processing.</span></span> <span data-ttu-id="96a77-106">Auch wenn die Arbeit in der Begin-Methode ausgeführt wird \_ , kann der Server den Client nicht annehmen, nachdem der **Signal** Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="96a77-106">Even if work remains to be done in the Begin\_ method, the server cannot impersonate the client after the call to **Signal** completes.</span></span>

<span data-ttu-id="96a77-107">Wenn der Server die Identität des Clients annimmt, bevor er [**Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal)aufruft, wird das Identitätswechsel Token erst dann aus dem Thread entfernt, wenn der Server [**IServerSecurity:: RevertToSelf**](/windows/win32/api/objidlbase/nf-objidlbase-iserversecurity-reverttoself) aufruft oder bis der Aufruf des Servers \_ zurückgibt, je nachdem, was zuerst eintritt.</span><span class="sxs-lookup"><span data-stu-id="96a77-107">If the server impersonates the client before it calls [**Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal), the impersonation token will not be removed from the thread until the server calls [**IServerSecurity::RevertToSelf**](/windows/win32/api/objidlbase/nf-objidlbase-iserversecurity-reverttoself) or until the server's call to Begin\_ returns, whichever comes first.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96a77-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="96a77-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96a77-109">Delegierung und Identitätswechsel</span><span class="sxs-lookup"><span data-stu-id="96a77-109">Delegation and Impersonation</span></span>](delegation-and-impersonation.md)
</dt> <dt>

[<span data-ttu-id="96a77-110">Ausführen eines asynchronen Aufrufes</span><span class="sxs-lookup"><span data-stu-id="96a77-110">Making an Asynchronous Call</span></span>](making-an-asynchronous-call.md)
</dt> </dl>

 

 