---
description: Eine Kombination aus 0 (null) oder mehr Sperroptionen, die den Typ der durchzuführenden Sperre beschreiben.
ms.assetid: 46a611bd-a1ec-4967-b68d-72661d1b5cad
title: D3DLOCK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adaeddbc1aff0812d3e0f67df90c2cf9b1118347
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999427"
---
# <a name="d3dlock"></a><span data-ttu-id="050f0-103">D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="050f0-103">D3DLOCK</span></span>

<span data-ttu-id="050f0-104">Eine Kombination aus 0 (null) oder mehr Sperroptionen, die den Typ der durchzuführenden Sperre beschreiben.</span><span class="sxs-lookup"><span data-stu-id="050f0-104">A combination of zero or more locking options that describe the type of lock to perform.</span></span>



| <span data-ttu-id="050f0-105">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="050f0-105">\#define</span></span>                   | <span data-ttu-id="050f0-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="050f0-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="050f0-107">D3DLOCK \_ DISCARD</span><span class="sxs-lookup"><span data-stu-id="050f0-107">D3DLOCK\_DISCARD</span></span>           | <span data-ttu-id="050f0-108">Die Anwendung verwirft den ganzen Arbeitsspeicher im gesperrten Bereich.</span><span class="sxs-lookup"><span data-stu-id="050f0-108">The application discards all memory within the locked region.</span></span> <span data-ttu-id="050f0-109">Für Scheitelpunkt- und Indexpuffer wird der gesamte Puffer verworfen.</span><span class="sxs-lookup"><span data-stu-id="050f0-109">For vertex and index buffers, the entire buffer will be discarded.</span></span> <span data-ttu-id="050f0-110">Diese Option ist nur gültig, wenn die Ressource mit dynamischer Nutzung erstellt wird (siehe [D3DUSAGE](d3dusage.md)).</span><span class="sxs-lookup"><span data-stu-id="050f0-110">This option is only valid when the resource is created with dynamic usage (see [D3DUSAGE](d3dusage.md)).</span></span>                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="050f0-111">D3DLOCK \_ DONOTWAIT</span><span class="sxs-lookup"><span data-stu-id="050f0-111">D3DLOCK\_DONOTWAIT</span></span>         | <span data-ttu-id="050f0-112">Ermöglicht es einer Anwendung, CPU-Zyklen zurück zu erhalten, wenn der Treiber die Oberfläche nicht sofort sperren kann.</span><span class="sxs-lookup"><span data-stu-id="050f0-112">Allows an application to gain back CPU cycles if the driver cannot lock the surface immediately.</span></span> <span data-ttu-id="050f0-113">Wenn dieses Flag festgelegt ist und der Treiber die Oberfläche nicht sofort sperren kann, gibt der Sperraufruf D3DERR \_ WASAUFRUFDRAWING zurück.</span><span class="sxs-lookup"><span data-stu-id="050f0-113">If this flag is set and the driver cannot lock the surface immediately, the lock call will return D3DERR\_WASSTILLDRAWING.</span></span> <span data-ttu-id="050f0-114">Dieses Flag kann nur verwendet werden, wenn eine Oberfläche gesperrt wird, die mit [**CreateOffscreenPlainSurface,**](/windows/desktop/api) [**CreateRenderTarget**](/windows/desktop/api)oder [**CreateDepthStencilSurface erstellt wurde.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)</span><span class="sxs-lookup"><span data-stu-id="050f0-114">This flag can only be used when locking a surface created using [**CreateOffscreenPlainSurface**](/windows/desktop/api), [**CreateRenderTarget**](/windows/desktop/api), or [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface).</span></span> <span data-ttu-id="050f0-115">Dieses Flag kann auch mit einem Hintergrundpuffer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="050f0-115">This flag can also be used with a back buffer.</span></span>            |
| <span data-ttu-id="050f0-116">D3DLOCK \_ KEIN \_ GEÄNDERTES \_ UPDATE</span><span class="sxs-lookup"><span data-stu-id="050f0-116">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span> | <span data-ttu-id="050f0-117">Standardmäßig fügt eine Sperre für eine Ressource dieser Ressource eine verfeinerte Region hinzu.</span><span class="sxs-lookup"><span data-stu-id="050f0-117">By default, a lock on a resource adds a dirty region to that resource.</span></span> <span data-ttu-id="050f0-118">Diese Option verhindert Änderungen am geänderten Zustand der Ressource.</span><span class="sxs-lookup"><span data-stu-id="050f0-118">This option prevents any changes to the dirty state of the resource.</span></span> <span data-ttu-id="050f0-119">Anwendungen sollten diese Option verwenden, wenn sie über zusätzliche Informationen über den Satz von Regionen verfügen, die während des Sperrvorganges geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="050f0-119">Applications should use this option when they have additional information about the set of regions changed during the lock operation.</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="050f0-120">D3DLOCK \_ NOOVERWRITE</span><span class="sxs-lookup"><span data-stu-id="050f0-120">D3DLOCK\_NOOVERWRITE</span></span>       | <span data-ttu-id="050f0-121">Gibt an, dass der Arbeitsspeicher, auf den seit der letzten Sperre ohne dieses Flag in einem Zeichnungsaufruf verwiesen wurde, während der Sperre nicht geändert wird.</span><span class="sxs-lookup"><span data-stu-id="050f0-121">Indicates that memory that was referred to in a drawing call since the last lock without this flag will not be modified during the lock.</span></span> <span data-ttu-id="050f0-122">Dies kann Optimierungen ermöglichen, wenn die Anwendung Daten an eine Ressource anfügt.</span><span class="sxs-lookup"><span data-stu-id="050f0-122">This can enable optimizations when the application is appending data to a resource.</span></span> <span data-ttu-id="050f0-123">Durch Die Angabe dieses Flags kann der Treiber sofort zurückkehren, wenn die Ressource verwendet wird. Andernfalls muss der Treiber die Verwendung der Ressource beenden, bevor die Sperrung aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="050f0-123">Specifying this flag enables the driver to return immediately if the resource is in use, otherwise, the driver must finish using the resource before returning from locking.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="050f0-124">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="050f0-124">D3DLOCK\_NOSYSLOCK</span></span>         | <span data-ttu-id="050f0-125">Das Standardverhalten einer Videospeichersperre besteht darin, einen systemweiten kritischen Abschnitt zu reservieren, wodurch sichergestellt wird, dass für die Dauer der Sperre keine Änderungen am Anzeigemodus vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="050f0-125">The default behavior of a video memory lock is to reserve a system-wide critical section, guaranteeing that no display mode changes will occur for the duration of the lock.</span></span> <span data-ttu-id="050f0-126">Diese Option bewirkt, dass der systemweite kritische Abschnitt für die Dauer der Sperre nicht gehalten wird.</span><span class="sxs-lookup"><span data-stu-id="050f0-126">This option causes the system-wide critical section not to be held for the duration of the lock.</span></span><br/> <span data-ttu-id="050f0-127">Der Sperrvorgang ist zeitaufwändig, kann es dem System jedoch ermöglichen, andere Aufgaben auszuführen, z. B. das Bewegen des Mauszeigers.</span><span class="sxs-lookup"><span data-stu-id="050f0-127">The lock operation is time consuming, but can enable the system to perform other duties, such as moving the mouse cursor.</span></span> <span data-ttu-id="050f0-128">Diese Option ist nützlich für Sperren mit langer Dauer, z. B. die Sperre des Hintergrundpuffers für das Softwarerendering, die andernfalls die Reaktionsfähigkeit des Systems beeinträchtigen würde.</span><span class="sxs-lookup"><span data-stu-id="050f0-128">This option is useful for long-duration locks, such as the lock of the back buffer for software rendering that would otherwise adversely affect system responsiveness.</span></span><br/> |
| <span data-ttu-id="050f0-129">D3DLOCK \_ READONLY</span><span class="sxs-lookup"><span data-stu-id="050f0-129">D3DLOCK\_READONLY</span></span>          | <span data-ttu-id="050f0-130">Die Anwendung schreibt nicht in den Puffer.</span><span class="sxs-lookup"><span data-stu-id="050f0-130">The application will not write to the buffer.</span></span> <span data-ttu-id="050f0-131">Dadurch können Ressourcen, die in nicht nativen Formaten gespeichert sind, beim Entsperren den Schritt zur Erneutkomprimierung speichern.</span><span class="sxs-lookup"><span data-stu-id="050f0-131">This enables resources stored in non-native formats to save the recompression step when unlocking.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="constant-information"></a><span data-ttu-id="050f0-132">Konstanteninformationen</span><span class="sxs-lookup"><span data-stu-id="050f0-132">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="050f0-133">Header</span><span class="sxs-lookup"><span data-stu-id="050f0-133">Header</span></span>                   | <span data-ttu-id="050f0-134">d3d9types.h</span><span class="sxs-lookup"><span data-stu-id="050f0-134">d3d9types.h</span></span> |
| <span data-ttu-id="050f0-135">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="050f0-135">Minimum operating system</span></span> | <span data-ttu-id="050f0-136">Windows 98</span><span class="sxs-lookup"><span data-stu-id="050f0-136">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="050f0-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="050f0-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="050f0-138">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="050f0-138">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="050f0-139">**LockRect**</span><span class="sxs-lookup"><span data-stu-id="050f0-139">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="050f0-140">**Sperre**</span><span class="sxs-lookup"><span data-stu-id="050f0-140">**Lock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[<span data-ttu-id="050f0-141">**LockRect**</span><span class="sxs-lookup"><span data-stu-id="050f0-141">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="050f0-142">**LockRect**</span><span class="sxs-lookup"><span data-stu-id="050f0-142">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="050f0-143">**Sperre**</span><span class="sxs-lookup"><span data-stu-id="050f0-143">**Lock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[<span data-ttu-id="050f0-144">**Lockbox**</span><span class="sxs-lookup"><span data-stu-id="050f0-144">**LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="050f0-145">**Lockbox**</span><span class="sxs-lookup"><span data-stu-id="050f0-145">**LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="050f0-146">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="050f0-146">**LockIndexBuffer**</span></span>](id3dxbasemesh--lockindexbuffer.md)
</dt> <dt>

[<span data-ttu-id="050f0-147">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="050f0-147">**LockVertexBuffer**</span></span>](id3dxbasemesh--lockvertexbuffer.md)
</dt> <dt>

<span data-ttu-id="050f0-148">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="050f0-148">**LockVertexBuffer**</span></span>
</dt> <dt>

[<span data-ttu-id="050f0-149">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="050f0-149">**LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="050f0-150">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="050f0-150">**LockAttributeBuffer**</span></span>](id3dxpatchmesh--lockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="050f0-151">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="050f0-151">**LockIndexBuffer**</span></span>](id3dxpatchmesh--lockindexbuffer.md)
</dt> <dt>

[<span data-ttu-id="050f0-152">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="050f0-152">**LockVertexBuffer**</span></span>](id3dxpatchmesh--lockvertexbuffer.md)
</dt> </dl>

 

 
