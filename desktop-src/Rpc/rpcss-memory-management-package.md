---
title: RPCSS-Speicher Verwaltungspaket
description: Das standardmäßige Zuweisungs-/zuordnerpaar, das von den Stub-und Laufzeit-Speicherplatz für die Speicher Belegung im Auftrag der Anwendung verwendet wird, ist die mittlere \_ Benutzer \_ Zuordnung/mittlere \_ Benutzer Freigabe \_ .
ms.assetid: 9477e677-59cb-45d5-b485-ab0171ac17ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26dca10ebea44fbb202240e981612e16e7960216
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473900"
---
# <a name="rpcss-memory-management-package"></a><span data-ttu-id="ab21d-103">RPCSS-Speicher Verwaltungspaket</span><span class="sxs-lookup"><span data-stu-id="ab21d-103">RpcSs Memory Management Package</span></span>

<span data-ttu-id="ab21d-104">Das standardmäßige Allocator-/zuordnerpaar, das von den Stub-und Lauf Zeit Elementen verwendet wird, wenn Speicher im Auftrag der Anwendung **belegt wird \_ \_** / **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="ab21d-104">The default allocator/deallocator pair used by the stubs and run time when allocating memory on behalf of the application is **midl\_user\_allocate**/**midl\_user\_free**.</span></span> <span data-ttu-id="ab21d-105">Allerdings können Sie das RPCSS-Paket anstelle der Standardeinstellung mithilfe des ACF-Attributs " **\[ \_ zuordnen \]**" auswählen.</span><span class="sxs-lookup"><span data-stu-id="ab21d-105">However, you can choose the RpcSs package instead of the default by using the ACF attribute **\[enable\_allocate\]**.</span></span> <span data-ttu-id="ab21d-106">Das RPCSS-Paket besteht aus RPC-Funktionen, die mit dem Präfix **RPCSS** oder **rpcsm** beginnen.</span><span class="sxs-lookup"><span data-stu-id="ab21d-106">The RpcSs package consists of RPC functions that begin with the prefix **RpcSs** or **RpcSm**.</span></span> <span data-ttu-id="ab21d-107">Das RPCSS-Paket wird für Windows-Anwendungen nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="ab21d-107">The RpcSs package is not recommended for Windows applications.</span></span>

> [!Note]  
> <span data-ttu-id="ab21d-108">Das RPCSS-Speicher Verwaltungspaket ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="ab21d-108">The Rpcss Memory Management Package is obsolete.</span></span> <span data-ttu-id="ab21d-109">Es wird empfohlen, dass die [**\_ Benutzer \_**](/windows/desktop/Midl/midl-user-allocate-1) Namen-und [**Mittel \_ \_ lose Benutzerzuordnungen**](/windows/desktop/Midl/midl-user-free-1) an dieser Stelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab21d-109">It is recommended that [**midl\_user\_allocate**](/windows/desktop/Midl/midl-user-allocate-1) and [**midl\_user\_free**](/windows/desktop/Midl/midl-user-free-1) are used in its place.</span></span>

 

<span data-ttu-id="ab21d-110">Im **/OSF** -Modus wird das RPCSS-Paket automatisch für die von der Mitte generierten Stub aktiviert, wenn vollständige Zeiger verwendet werden, wenn die Argumente eine Speicher Belegung erfordern oder wenn das Attribut " **\[ \_ \] zuordnen** " verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ab21d-110">In **/osf** mode, the RpcSs package is enabled for MIDL-generated stubs automatically when full pointers are used, when the arguments require memory allocation, or as a result of using the **\[enable\_allocate\]** attribute.</span></span> <span data-ttu-id="ab21d-111">Im Standardmodus (Microsoft Extended) ist das RPCSS-Paket nur aktiviert, wenn das Attribut " **\[ \_ zuordnen \]** " verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ab21d-111">In the default (Microsoft extended) mode, the RpcSs package is enabled only when the **\[enable\_allocate\]** attribute is used.</span></span> <span data-ttu-id="ab21d-112">Das Attribut " **\[ \_ zuordnen \]** " ermöglicht die RPCSS-Umgebung durch die serverseitigen Stub.</span><span class="sxs-lookup"><span data-stu-id="ab21d-112">The **\[enable\_allocate\]** attribute enables the RpcSs environment by the server-side stubs.</span></span> <span data-ttu-id="ab21d-113">Die Clientseite wird mit der Möglichkeit benachrichtigt, dass das RPCSS-Paket aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ab21d-113">The client side becomes alerted to the possibility that the RpcSs package may be enabled.</span></span> <span data-ttu-id="ab21d-114">Im **/OSF** -Modus ist die Clientseite nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="ab21d-114">In **/osf** mode, the client side is not affected.</span></span>

<span data-ttu-id="ab21d-115">Wenn das RPCSS-Paket aktiviert ist, wird die Speicher Belegung auf der Serverseite mit den privaten RPCSS-Speicher Verwaltungs Zuordnungen und dem deallokator-paar erreicht.</span><span class="sxs-lookup"><span data-stu-id="ab21d-115">When the RpcSs package is enabled, allocation of memory on the server side is accomplished with the private RpcSs memory management allocator and deallocator pair.</span></span> <span data-ttu-id="ab21d-116">Sie können Speicher mithilfe desselben Mechanismus zuweisen, indem Sie [**rpcsmallo(**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) oder [**rpcsszuordnen**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssallocate)) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ab21d-116">You can allocate memory using the same mechanism by calling [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) (or [**RpcSsAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssallocate)).</span></span> <span data-ttu-id="ab21d-117">Bei der Rückgabe vom Serverstub wird der gesamte vom RPCSS-Paket zugewiesene Arbeitsspeicher automatisch freigegeben.</span><span class="sxs-lookup"><span data-stu-id="ab21d-117">Upon return from the server stub, all the memory allocated by the RpcSs package is automatically freed.</span></span> <span data-ttu-id="ab21d-118">Das folgende Beispiel zeigt, wie Sie das RPCSS-Paket aktivieren:</span><span class="sxs-lookup"><span data-stu-id="ab21d-118">The following example shows how to enable the RpcSs package:</span></span>

``` syntax
/* ACF file fragment */

[ 
    implicit_handle(handle_t GlobalHandle),
    enable_allocate
]
interface iface
{
}

/*Server management routine fragment. Replaces p=midl_user_allocate(size); */

    p=RpcSsAllocate(size);                /*raises exception */
    p=RpcSmAllocate(size, &status);       /*returns error code */
```

<span data-ttu-id="ab21d-119">Die Anwendung kann durch Aufrufen der Funktion [**rpcssfree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssfree) oder [**rpcsmfree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) explizit Arbeitsspeicher freigeben.</span><span class="sxs-lookup"><span data-stu-id="ab21d-119">Your application can explicitly free memory by invoking the [**RpcSsFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssfree) or [**RpcSmFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmfree) function.</span></span> <span data-ttu-id="ab21d-120">Beachten Sie, dass diese Funktionen keinen Speicherplatz freigeben.</span><span class="sxs-lookup"><span data-stu-id="ab21d-120">Note that these functions do not actually free memory.</span></span> <span data-ttu-id="ab21d-121">Sie markieren Sie zum Löschen.</span><span class="sxs-lookup"><span data-stu-id="ab21d-121">They mark it for deletion.</span></span> <span data-ttu-id="ab21d-122">Die RPC-Bibliothek gibt den Arbeitsspeicher frei, wenn das Programm " [**rpcssdisableallolealloleallolealloleallolealloleallole**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate) [](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate)</span><span class="sxs-lookup"><span data-stu-id="ab21d-122">The RPC library releases the memory when your program calls [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate) or [**RpcSsDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdisableallocate).</span></span>

<span data-ttu-id="ab21d-123">Sie können auch die Speicher Verwaltungs Umgebung für Ihre Anwendung aktivieren, indem Sie die [**rpcsmenableallo-**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmenableallocate) Routine aufrufen (und Sie können Sie deaktivieren, indem Sie die Routine [**rpcsmdisablebelegungs**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmdisableallocate) Vorgang aufrufen).</span><span class="sxs-lookup"><span data-stu-id="ab21d-123">You can also enable the memory management environment for your application by calling the [**RpcSmEnableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmenableallocate) routine (and you can disable it by calling the [**RpcSmDisableAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmdisableallocate) routine).</span></span> <span data-ttu-id="ab21d-124">Nachdem die Funktion aktiviert wurde, kann der Anwendungscode Arbeitsspeicher zuordnen und seine Freigabe durch Aufrufen von Funktionen aus dem RPCSS-Paket verringern.</span><span class="sxs-lookup"><span data-stu-id="ab21d-124">Once enabled, application code can allocate and deallocate memory by calling functions from the RpcSs package.</span></span>

 

 