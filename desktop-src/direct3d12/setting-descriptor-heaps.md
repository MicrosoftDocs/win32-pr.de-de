---
title: Festlegen und Auffüllen von deskriptorheaps
description: Die deskriptorheap-Typen, die in einer Befehlsliste festgelegt werden können, sind diejenigen, die Deskriptoren enthalten, für die deskriptortabellen verwendet werden können (höchstens jeweils jeweils jeweils).
ms.assetid: F0FF3D7C-1DAC-48C3-B47D-0378BE369F37
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e3a1b6c4863827e1d8e1bdfb33a0a64420211d
ms.sourcegitcommit: 584b35959515bc5e4a104e8cf5270513f146f590
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2019
ms.locfileid: "104548669"
---
# <a name="setting-and-populating-descriptor-heaps"></a><span data-ttu-id="7ca92-103">Festlegen und Auffüllen von deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="7ca92-103">Setting and Populating Descriptor Heaps</span></span>

<span data-ttu-id="7ca92-104">Die deskriptorheap-Typen, die in einer Befehlsliste festgelegt werden können, sind diejenigen, die Deskriptoren enthalten, für die deskriptortabellen verwendet werden können (höchstens jeweils jeweils jeweils).</span><span class="sxs-lookup"><span data-stu-id="7ca92-104">The descriptor heap types that can be set on a command list are those that contain descriptors for which descriptor tables can be used (at most one of each at a time).</span></span>

-   [<span data-ttu-id="7ca92-105">Festlegen von deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="7ca92-105">Setting descriptor heaps</span></span>](#setting-and-populating-descriptor-heaps)
-   [<span data-ttu-id="7ca92-106">Auffüllen von deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="7ca92-106">Populating descriptor heaps</span></span>](#populating-descriptor-heaps)
-   [<span data-ttu-id="7ca92-107">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7ca92-107">Related topics</span></span>](#related-topics)

## <a name="setting-descriptor-heaps"></a><span data-ttu-id="7ca92-108">Festlegen von deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="7ca92-108">Setting descriptor heaps</span></span>

<span data-ttu-id="7ca92-109">Die Typen des deskriptorheaps, die in einer Befehlsliste festgelegt werden können, sind:</span><span class="sxs-lookup"><span data-stu-id="7ca92-109">The types of descriptor heap that can be set on a command list are:</span></span>

``` syntax
D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV
D3D12_DESCRIPTOR_HEAP_TYPE_SAMPLER
```

<span data-ttu-id="7ca92-110">Die Heaps, die in der Befehlsliste festgelegt werden, müssen auch als Shader-sichtbar erstellt worden sein.</span><span class="sxs-lookup"><span data-stu-id="7ca92-110">The heaps being set on the command list must also have been created as shader visible.</span></span> <span data-ttu-id="7ca92-111">Es gibt drei Typen von Befehlslisten: Direct, Bundle und Compute.</span><span class="sxs-lookup"><span data-stu-id="7ca92-111">There are three types of command list: DIRECT, BUNDLE, and COMPUTE.</span></span>

<span data-ttu-id="7ca92-112">Nachdem ein deskriptorheap in einer Befehlsliste festgelegt wurde, verweisen nachfolgende Aufrufe, die deskriptortabellen definieren, auf den aktuellen deskriptorheap.</span><span class="sxs-lookup"><span data-stu-id="7ca92-112">After a descriptor heap is set on a command list, subsequent calls that define descriptor tables refer to the current descriptor heap.</span></span> <span data-ttu-id="7ca92-113">Der deskriptortabellenstatus ist am Anfang einer Befehlsliste nicht definiert, und nach dem Ändern der deskriptorheaps in einer Befehlsliste.</span><span class="sxs-lookup"><span data-stu-id="7ca92-113">Descriptor table state is undefined at the beginning of a command list and after descriptor heaps are changed on a command list.</span></span> <span data-ttu-id="7ca92-114">Das redundanter festlegen desselben deskriptorheaps führt nicht dazu, dass deskriptortabelleneinstellungen nicht definiert sind.</span><span class="sxs-lookup"><span data-stu-id="7ca92-114">Redundantly setting the same descriptor heap does not cause descriptor table settings to be undefined.</span></span>

<span data-ttu-id="7ca92-115">In einem Bündel können die deskriptorheaps dagegen nur einmal festgelegt werden (redundante Aufrufe, die zweimal denselben Heap festlegen, verursachen keinen Fehler); Andernfalls ist das Verhalten nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="7ca92-115">In a bundle, by contrast, the descriptor heaps can only be set once (redundant calls setting the same heap twice do not produce an error); otherwise, the behavior is undefined.</span></span> <span data-ttu-id="7ca92-116">Die festgelegten deskriptorheaps müssen dem Status entsprechen, wenn eine Befehlsliste das Paket aufruft. Andernfalls ist das Verhalten nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="7ca92-116">The descriptor heaps that are set must match the state when any command list calls the bundle; otherwise, the behavior is undefined.</span></span> <span data-ttu-id="7ca92-117">Dadurch können Pakete die deskriptortabelleneinstellungen der Befehlsliste erben und bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="7ca92-117">This allows bundles to inherit and edit the command list’s descriptor table settings.</span></span> <span data-ttu-id="7ca92-118">Bündel, die keine deskriptortabellen ändern (nur erben), müssen überhaupt keinen deskriptorheap festlegen, und Sie erben nur von der aufrufenden Befehlsliste.</span><span class="sxs-lookup"><span data-stu-id="7ca92-118">Bundles that don’t change descriptor tables (only inherit them) don’t need to set a descriptor heap at all and will just inherit from the calling command list.</span></span>

<span data-ttu-id="7ca92-119">Wenn deskriptorheaps festgelegt werden (mithilfe von [**ID3D12GraphicsCommandList:: setdescriptorheaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)), werden alle verwendeten Heaps in einem einzelnen-Befehl festgelegt (und alle zuvor festgelegten Heaps werden durch den-Befehl nicht festgelegt).</span><span class="sxs-lookup"><span data-stu-id="7ca92-119">When descriptor heaps are set (using [**ID3D12GraphicsCommandList::SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)), all the heaps being used are set in a single call (and all previously set heaps are unset by the call).</span></span> <span data-ttu-id="7ca92-120">Höchstens ein Heap jedes oben aufgeführten Typs kann im-Befehl festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7ca92-120">At most one heap of each type listed above can be set in the call.</span></span>

## <a name="populating-descriptor-heaps"></a><span data-ttu-id="7ca92-121">Auffüllen von deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="7ca92-121">Populating descriptor heaps</span></span>

<span data-ttu-id="7ca92-122">Nachdem eine Anwendung einen deskriptorheap erstellt hat, kann Sie Methoden auf dem Gerät verwenden, um entweder Deskriptoren direkt in den Heap zu generieren oder Deskriptoren von einem Ort in einen anderen zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="7ca92-122">After an application has created a descriptor heap, it can then use methods on the device to either generate descriptors directly into the heap or copy descriptors from one place to another.</span></span>

<span data-ttu-id="7ca92-123">Der anfängliche Inhalt des deskriptorheap-Speichers ist nicht definiert. Daher kann die GPU oder der Treiber zum Verweisen auf nicht initialisierten Speicher für das Rendering zu nicht definierten Ergebnissen führen, z. b. zum Zurücksetzen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="7ca92-123">The initial contents of descriptor heap memory is undefined, so asking the GPU or driver to reference uninitialized memory for rendering can cause undefined results such as a device reset.</span></span>

<span data-ttu-id="7ca92-124">Wenn die Anwendung einen deskriptorheap für die CPU-Sicht konfiguriert, kann die CPU Methoden zum Erstellen von Deskriptoren im Heap und zum Kopieren von Ort zu Ort (einschließlich Heaps) in einem unmittelbaren, kostenlosen Thread aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="7ca92-124">If the application configures a descriptor heap to be CPU visible, then the CPU can call methods to create descriptors into the heap and copy from place to place (including across heaps) in an immediate, free threaded manner.</span></span> <span data-ttu-id="7ca92-125">Wenn der Heap als SHADER_VISIBLE konfiguriert wurde, ist das Lesen der CPU nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="7ca92-125">If the heap has been configured as SHADER_VISIBLE, reading by the CPU is not permitted.</span></span>



## <a name="related-topics"></a><span data-ttu-id="7ca92-126">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7ca92-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ca92-127">Deskriptorheaps</span><span class="sxs-lookup"><span data-stu-id="7ca92-127">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




