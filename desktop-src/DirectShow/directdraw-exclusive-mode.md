---
description: Exklusiver DirectDraw-Modus
ms.assetid: 3ef4f267-4dc2-421b-ade4-6b1efa364733
title: Exklusiver DirectDraw-Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5b04bae9c3221a4acee9900c5f19ba4e9b0d54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344935"
---
# <a name="directdraw-exclusive-mode"></a><span data-ttu-id="7a990-103">Exklusiver DirectDraw-Modus</span><span class="sxs-lookup"><span data-stu-id="7a990-103">DirectDraw Exclusive Mode</span></span>

> [!Note]  
> <span data-ttu-id="7a990-104">Dieses Thema gilt nur für VMR-7.</span><span class="sxs-lookup"><span data-stu-id="7a990-104">This topic applies to the VMR-7 only.</span></span> <span data-ttu-id="7a990-105">In VMR-9 aktivieren Sie den exklusiven Modus, indem Sie Ihren eigenen exklusiven moduszuordnerpräsentator bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7a990-105">In the VMR-9, you enable exclusive mode by supplying your own exclusive mode allocator-presenter.</span></span> <span data-ttu-id="7a990-106">Dies ist relativ unkompliziert, wenn Sie die [**IVMRSurfaceAllocatorNotify9:: depingesurfacehelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a990-106">This is relatively straightforward if you use the [**IVMRSurfaceAllocatorNotify9::AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) method.</span></span> <span data-ttu-id="7a990-107">Das VMR9Allocator-Beispiel zeigt, wie ein benutzerdefinierter Zuweiser zukator implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="7a990-107">The VMR9Allocator sample shows how to implement a custom allocator-presenter.</span></span>

 

<span data-ttu-id="7a990-108">Im exklusiven DirectDraw-Modus übernimmt eine Anwendung die exklusive Kontrolle über die Grafikhardware.</span><span class="sxs-lookup"><span data-stu-id="7a990-108">In DirectDraw Exclusive Mode, an application takes exclusive control of the graphics hardware.</span></span> <span data-ttu-id="7a990-109">Dies ist nützlich für Anwendungen, wie z. b. Spiele oder für Vollbild-Videoanwendungen.</span><span class="sxs-lookup"><span data-stu-id="7a990-109">This is useful for applications such as games, or perhaps full-screen video applications.</span></span> <span data-ttu-id="7a990-110">Normalerweise erstellt VMR die DirectDraw-Objekte und legt die kooperative Ebene auf Normal fest.</span><span class="sxs-lookup"><span data-stu-id="7a990-110">Normally, the VMR creates the DirectDraw objects and sets the cooperative level to normal.</span></span> <span data-ttu-id="7a990-111">Um jedoch VMR im exklusiven DirectDraw-Modus auszuführen, muss die Anwendung selbst das DirectDraw-Objekt und die primäre Oberfläche erstellen und **setkooperativelevel** aufrufen, um den exklusiven Modus anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7a990-111">However, to run the VMR in DirectDraw Exclusive Mode, the application itself must create the DirectDraw object and the primary surface, and call **SetCooperativeLevel** to specify exclusive mode.</span></span>

<span data-ttu-id="7a990-112">VMR verfügt über einen speziellen zuordnerpräsentator, der es ermöglicht, im exklusiven DirectDraw-Modus auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7a990-112">The VMR has a special allocator-presenter that enables it to run in DirectDraw Exclusive Mode.</span></span> <span data-ttu-id="7a990-113">So konfigurieren Sie VMR für die Verwendung dieses zuordnerstellers:</span><span class="sxs-lookup"><span data-stu-id="7a990-113">To configure the VMR to use this allocator-presenter:</span></span>

1.  <span data-ttu-id="7a990-114">Erstellen Sie das Filter Diagramm, und fügen Sie das VMR mithilfe der [**ifiltergraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) -Methode hinzu.</span><span class="sxs-lookup"><span data-stu-id="7a990-114">Create the Filter Graph and add the VMR to it using the [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) method.</span></span> <span data-ttu-id="7a990-115">Ein Codebeispiel finden Sie unter [VMR (fensterlose Modus](vmr-windowless-mode.md)).</span><span class="sxs-lookup"><span data-stu-id="7a990-115">For a code example, see [VMR Windowless Mode](vmr-windowless-mode.md).</span></span>
2.  <span data-ttu-id="7a990-116">Erstellen Sie den exklusiven Modus "zuordcator-Presenter":</span><span class="sxs-lookup"><span data-stu-id="7a990-116">Create the Exclusive Mode allocator-presenter:</span></span>
    ```C++
    IVMRImagePresenterExclModeConfig* pExclModeConfig;
    CoCreateInstance(
            CLSID_AllocPresenterDDXclMode,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_IVMRImagePresenterExclModeConfig,
            (void**)&pExclModeConfig
            );
    ```

    

3.  <span data-ttu-id="7a990-117">Konfigurieren Sie den neuen zuordcator-Presenter:</span><span class="sxs-lookup"><span data-stu-id="7a990-117">Configure the new allocator-presenter:</span></span>
    ```C++
    pExclModeConfig->SetXlcModeDDObjAndPrimarySurface(...);
    ```

    

4.  <span data-ttu-id="7a990-118">Verbinden Sie die neue Zuweisung-Presenter mit der VMR.</span><span class="sxs-lookup"><span data-stu-id="7a990-118">Plug the new allocator-presenter into the VMR.</span></span>
5.  <span data-ttu-id="7a990-119">Erstellen Sie den Rest des Filter Diagramms auf die übliche Weise.</span><span class="sxs-lookup"><span data-stu-id="7a990-119">Build the rest of the filter graph in the usual ways.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a990-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7a990-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a990-121">VMR-Betriebsmodi</span><span class="sxs-lookup"><span data-stu-id="7a990-121">VMR Modes of Operation</span></span>](vmr-modes-of-operation.md)
</dt> </dl>

 

 



