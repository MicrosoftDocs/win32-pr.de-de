---
description: Eine Kombination von 0 (null) oder mehreren Sperr Optionen, die den Typ der auszuführenden Sperre beschreiben.
ms.assetid: 46a611bd-a1ec-4967-b68d-72661d1b5cad
title: D3DLOCK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea3a60318aad8ae0fadcf02d5dea76f6aa62548
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748729"
---
# <a name="d3dlock"></a><span data-ttu-id="04658-103">D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="04658-103">D3DLOCK</span></span>

<span data-ttu-id="04658-104">Eine Kombination von 0 (null) oder mehreren Sperr Optionen, die den Typ der auszuführenden Sperre beschreiben.</span><span class="sxs-lookup"><span data-stu-id="04658-104">A combination of zero or more locking options that describe the type of lock to perform.</span></span>



|                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04658-105">\#definieren</span><span class="sxs-lookup"><span data-stu-id="04658-105">\#define</span></span>                   | <span data-ttu-id="04658-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04658-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="04658-107">D3DLOCK \_ verwerfen</span><span class="sxs-lookup"><span data-stu-id="04658-107">D3DLOCK\_DISCARD</span></span>           | <span data-ttu-id="04658-108">Die Anwendung verwirft den gesamten Arbeitsspeicher innerhalb der gesperrten Region.</span><span class="sxs-lookup"><span data-stu-id="04658-108">The application discards all memory within the locked region.</span></span> <span data-ttu-id="04658-109">Für Scheitelpunkt-und Index Puffer wird der gesamte Puffer verworfen.</span><span class="sxs-lookup"><span data-stu-id="04658-109">For vertex and index buffers, the entire buffer will be discarded.</span></span> <span data-ttu-id="04658-110">Diese Option ist nur gültig, wenn die Ressource mit dynamischer Verwendung erstellt wird (siehe [D3DUSAGE](d3dusage.md)).</span><span class="sxs-lookup"><span data-stu-id="04658-110">This option is only valid when the resource is created with dynamic usage (see [D3DUSAGE](d3dusage.md)).</span></span>                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="04658-111">D3DLOCK \_ donotwait</span><span class="sxs-lookup"><span data-stu-id="04658-111">D3DLOCK\_DONOTWAIT</span></span>         | <span data-ttu-id="04658-112">Ermöglicht es einer Anwendung, CPU-Zyklen zurückzugewinnen, wenn der Treiber die-Oberfläche nicht sofort sperren kann.</span><span class="sxs-lookup"><span data-stu-id="04658-112">Allows an application to gain back CPU cycles if the driver cannot lock the surface immediately.</span></span> <span data-ttu-id="04658-113">Wenn dieses Flag festgelegt ist und der Treiber die-Oberfläche nicht sofort sperren kann, gibt der Lock-Befehl D3DERR \_ wasstilldrawing zurück.</span><span class="sxs-lookup"><span data-stu-id="04658-113">If this flag is set and the driver cannot lock the surface immediately, the lock call will return D3DERR\_WASSTILLDRAWING.</span></span> <span data-ttu-id="04658-114">Dieses Flag kann nur verwendet werden, wenn eine Oberfläche gesperrt wird, die mithilfe von "| [**ateoffscreenplainsurface**](/windows/desktop/api)", " [**kreaterendertarget**](/windows/desktop/api)" oder " [**kreatedepthschablone**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)" erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="04658-114">This flag can only be used when locking a surface created using [**CreateOffscreenPlainSurface**](/windows/desktop/api), [**CreateRenderTarget**](/windows/desktop/api), or [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface).</span></span> <span data-ttu-id="04658-115">Dieses Flag kann auch mit einem Hintergrund Puffer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="04658-115">This flag can also be used with a back buffer.</span></span>            |
| <span data-ttu-id="04658-116">D3DLOCK \_ kein \_ Dirty \_ Update</span><span class="sxs-lookup"><span data-stu-id="04658-116">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span> | <span data-ttu-id="04658-117">Standardmäßig fügt eine Sperre für eine Ressource der Ressource einen geänderten Bereich hinzu.</span><span class="sxs-lookup"><span data-stu-id="04658-117">By default, a lock on a resource adds a dirty region to that resource.</span></span> <span data-ttu-id="04658-118">Diese Option verhindert Änderungen am geänderten Zustand der Ressource.</span><span class="sxs-lookup"><span data-stu-id="04658-118">This option prevents any changes to the dirty state of the resource.</span></span> <span data-ttu-id="04658-119">Anwendungen sollten diese Option verwenden, wenn Sie über zusätzliche Informationen über den Satz von Regionen verfügen, der während des Sperr Vorgangs geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="04658-119">Applications should use this option when they have additional information about the set of regions changed during the lock operation.</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="04658-120">D3DLOCK \_ noüberschreibung</span><span class="sxs-lookup"><span data-stu-id="04658-120">D3DLOCK\_NOOVERWRITE</span></span>       | <span data-ttu-id="04658-121">Gibt an, dass der Arbeitsspeicher, auf den in einem Zeichnungs aufrufzeichen seit der letzten Sperre ohne dieses Flag verwiesen wurde, während der Sperre nicht geändert wird.</span><span class="sxs-lookup"><span data-stu-id="04658-121">Indicates that memory that was referred to in a drawing call since the last lock without this flag will not be modified during the lock.</span></span> <span data-ttu-id="04658-122">Dadurch können Optimierungen aktiviert werden, wenn die Anwendung Daten an eine Ressource anfügt.</span><span class="sxs-lookup"><span data-stu-id="04658-122">This can enable optimizations when the application is appending data to a resource.</span></span> <span data-ttu-id="04658-123">Wenn Sie dieses Flag angeben, kann der Treiber sofort zurückkehren, wenn die Ressource verwendet wird. andernfalls muss der Treiber die Verwendung der Ressource beenden, bevor die Sperre zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="04658-123">Specifying this flag enables the driver to return immediately if the resource is in use, otherwise, the driver must finish using the resource before returning from locking.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="04658-124">D3DLOCK \_ nosyslock</span><span class="sxs-lookup"><span data-stu-id="04658-124">D3DLOCK\_NOSYSLOCK</span></span>         | <span data-ttu-id="04658-125">Das Standardverhalten einer Videospeicher Sperre besteht darin, einen systemweiten kritischen Abschnitt zu reservieren. Dadurch wird sichergestellt, dass für die Dauer der Sperre keine Änderungen des Anzeigemodus auftreten.</span><span class="sxs-lookup"><span data-stu-id="04658-125">The default behavior of a video memory lock is to reserve a system-wide critical section, guaranteeing that no display mode changes will occur for the duration of the lock.</span></span> <span data-ttu-id="04658-126">Diese Option bewirkt, dass der systemweite kritische Abschnitt für die Dauer der Sperre nicht aufrechterhalten wird.</span><span class="sxs-lookup"><span data-stu-id="04658-126">This option causes the system-wide critical section not to be held for the duration of the lock.</span></span><br/> <span data-ttu-id="04658-127">Der Sperr Vorgang ist zeitaufwändig, kann jedoch dem System ermöglichen, andere Aufgaben auszuführen, z. b. das Bewegen des Mauszeigers.</span><span class="sxs-lookup"><span data-stu-id="04658-127">The lock operation is time consuming, but can enable the system to perform other duties, such as moving the mouse cursor.</span></span> <span data-ttu-id="04658-128">Diese Option ist für Sperren mit langer Dauer nützlich, wie z. b. die Sperre des Hintergrund Puffers für das Software Rendering, das sich andernfalls nachteilig auf die Reaktionsfähigkeit des Systems auswirkt.</span><span class="sxs-lookup"><span data-stu-id="04658-128">This option is useful for long-duration locks, such as the lock of the back buffer for software rendering that would otherwise adversely affect system responsiveness.</span></span><br/> |
| <span data-ttu-id="04658-129">D3DLOCK \_ schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="04658-129">D3DLOCK\_READONLY</span></span>          | <span data-ttu-id="04658-130">Die Anwendung schreibt nicht in den Puffer.</span><span class="sxs-lookup"><span data-stu-id="04658-130">The application will not write to the buffer.</span></span> <span data-ttu-id="04658-131">Dadurch können Ressourcen, die in nicht nativen Formaten gespeichert sind, beim Entsperren den Schritt zum erneuten komprimieren speichern.</span><span class="sxs-lookup"><span data-stu-id="04658-131">This enables resources stored in non-native formats to save the recompression step when unlocking.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="constant-information"></a><span data-ttu-id="04658-132">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="04658-132">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="04658-133">Header</span><span class="sxs-lookup"><span data-stu-id="04658-133">Header</span></span>                   | <span data-ttu-id="04658-134">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="04658-134">d3d9types.h</span></span> |
| <span data-ttu-id="04658-135">Mindestens Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="04658-135">Minimum operating system</span></span> | <span data-ttu-id="04658-136">Windows 98</span><span class="sxs-lookup"><span data-stu-id="04658-136">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="04658-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="04658-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04658-138">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="04658-138">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="04658-139">**Lockrect**</span><span class="sxs-lookup"><span data-stu-id="04658-139">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="04658-140">**Sperre**</span><span class="sxs-lookup"><span data-stu-id="04658-140">**Lock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[<span data-ttu-id="04658-141">**Lockrect**</span><span class="sxs-lookup"><span data-stu-id="04658-141">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="04658-142">**Lockrect**</span><span class="sxs-lookup"><span data-stu-id="04658-142">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="04658-143">**Sperre**</span><span class="sxs-lookup"><span data-stu-id="04658-143">**Lock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[<span data-ttu-id="04658-144">**Lockbox**</span><span class="sxs-lookup"><span data-stu-id="04658-144">**LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="04658-145">**Lockbox**</span><span class="sxs-lookup"><span data-stu-id="04658-145">**LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="04658-146">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="04658-146">**LockIndexBuffer**</span></span>](id3dxbasemesh--lockindexbuffer.md)
</dt> <dt>

[<span data-ttu-id="04658-147">**Lockvertexbuffer**</span><span class="sxs-lookup"><span data-stu-id="04658-147">**LockVertexBuffer**</span></span>](id3dxbasemesh--lockvertexbuffer.md)
</dt> <dt>

<span data-ttu-id="04658-148">**Lockvertexbuffer**</span><span class="sxs-lookup"><span data-stu-id="04658-148">**LockVertexBuffer**</span></span>
</dt> <dt>

[<span data-ttu-id="04658-149">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="04658-149">**LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="04658-150">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="04658-150">**LockAttributeBuffer**</span></span>](id3dxpatchmesh--lockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="04658-151">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="04658-151">**LockIndexBuffer**</span></span>](id3dxpatchmesh--lockindexbuffer.md)
</dt> <dt>

[<span data-ttu-id="04658-152">**Lockvertexbuffer**</span><span class="sxs-lookup"><span data-stu-id="04658-152">**LockVertexBuffer**</span></span>](id3dxpatchmesh--lockvertexbuffer.md)
</dt> </dl>

 

 
