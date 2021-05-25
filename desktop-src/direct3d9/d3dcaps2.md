---
description: Eine Liste der Treiberfunktionsflags finden Sie hier. Enthält die Definitionen, Werte und Beschreibungen mit Links zu APIs.
ms.assetid: 0c0c65fc-f953-4379-a6d0-6ce447a0c183
title: D3DCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f209e840450b834c3a69593d1297f2cba9ee43c0
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343375"
---
# <a name="d3dcaps2"></a><span data-ttu-id="6632d-104">D3DCAPS2</span><span class="sxs-lookup"><span data-stu-id="6632d-104">D3DCAPS2</span></span>

<span data-ttu-id="6632d-105">Treiberfunktionsflags.</span><span class="sxs-lookup"><span data-stu-id="6632d-105">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6632d-106">#Definieren</span><span class="sxs-lookup"><span data-stu-id="6632d-106">#define</span></span></td>
<td><span data-ttu-id="6632d-107">Wert</span><span class="sxs-lookup"><span data-stu-id="6632d-107">Value</span></span></td>
<td><span data-ttu-id="6632d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6632d-108">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6632d-109">D3DCAPS2_CANAUTOGENMIPMAP</span><span class="sxs-lookup"><span data-stu-id="6632d-109">D3DCAPS2_CANAUTOGENMIPMAP</span></span></td>
<td><span data-ttu-id="6632d-110">0x40000000L</span><span class="sxs-lookup"><span data-stu-id="6632d-110">0x40000000L</span></span></td>
<td><span data-ttu-id="6632d-111">Der Treiber kann automatisch Mipmaps generieren.</span><span class="sxs-lookup"><span data-stu-id="6632d-111">The driver is capable of automatically generating mipmaps.</span></span> <span data-ttu-id="6632d-112">Weitere Informationen finden Sie unter <a href="automatic-generation-of-mipmaps.md">Automatische Generierung von Mipmaps (Direct3D 9).</a></span><span class="sxs-lookup"><span data-stu-id="6632d-112">For more information, see <a href="automatic-generation-of-mipmaps.md">Automatic Generation of Mipmaps (Direct3D 9)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6632d-113">D3DCAPS2_CANCALIBRATEGAMMA</span><span class="sxs-lookup"><span data-stu-id="6632d-113">D3DCAPS2_CANCALIBRATEGAMMA</span></span></td>
<td><span data-ttu-id="6632d-114">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="6632d-114">0x00100000L</span></span></td>
<td><span data-ttu-id="6632d-115">Auf dem System ist ein Kalibrierer installiert, mit dem die Gammaverlaufsverlauf automatisch angepasst werden kann, sodass das Ergebnis auf allen Systemen, die über einen Kalibrierer verfügen, identisch ist.</span><span class="sxs-lookup"><span data-stu-id="6632d-115">The system has a calibrator installed that can automatically adjust the gamma ramp so that the result is identical on all systems that have a calibrator.</span></span> <span data-ttu-id="6632d-116">Um den Kalibrierungsprozessor beim Festlegen neuer Gammawerte aufzurufen, verwenden Sie beim Aufrufen von <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>das flag D3DSGR_CALIBRATE .</span><span class="sxs-lookup"><span data-stu-id="6632d-116">To invoke the calibrator when setting new gamma levels, use the D3DSGR_CALIBRATE flag when calling <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>.</span></span> <span data-ttu-id="6632d-117">Das Kalibrieren von Gamma rampen verursacht einen gewissen Verarbeitungsaufwand und sollte nicht häufig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6632d-117">Calibrating gamma ramps incurs some processing overhead and should not be used frequently.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6632d-118">D3DCAPS2_CANSHARERESOURCE</span><span class="sxs-lookup"><span data-stu-id="6632d-118">D3DCAPS2_CANSHARERESOURCE</span></span></td>
<td><span data-ttu-id="6632d-119">0x80000000L</span><span class="sxs-lookup"><span data-stu-id="6632d-119">0x80000000L</span></span></td>
<td><span data-ttu-id="6632d-120">Das Gerät kann sharable Ressourcen erstellen.</span><span class="sxs-lookup"><span data-stu-id="6632d-120">The device can create sharable resources.</span></span> <span data-ttu-id="6632d-121">Methoden, die Ressourcen erstellen, können Nicht-NULL-Werte für ihre <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>pSharedHandle-Parameter</strong></a> festlegen.</span><span class="sxs-lookup"><span data-stu-id="6632d-121">Methods that create resources can set non-NULL values for their <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>pSharedHandle</strong></a> parameters.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6632d-122">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="6632d-122">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="6632d-123">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6632d-123">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6632d-124">D3DCAPS2_CANMANAGERESOURCE</span><span class="sxs-lookup"><span data-stu-id="6632d-124">D3DCAPS2_CANMANAGERESOURCE</span></span></td>
<td><span data-ttu-id="6632d-125">0x10000000L</span><span class="sxs-lookup"><span data-stu-id="6632d-125">0x10000000L</span></span></td>
<td><span data-ttu-id="6632d-126">Der Treiber kann Ressourcen verwalten.</span><span class="sxs-lookup"><span data-stu-id="6632d-126">The driver is capable of managing resources.</span></span> <span data-ttu-id="6632d-127">Bei solchen Treibern D3DPOOL_MANAGED Ressourcen vom Treiber verwaltet.</span><span class="sxs-lookup"><span data-stu-id="6632d-127">On such drivers, D3DPOOL_MANAGED resources will be managed by the driver.</span></span> <span data-ttu-id="6632d-128">Damit Direct3D den Treiber überschreibt, sodass Direct3D Ressourcen verwaltet, verwenden Sie das D3DCREATE_DISABLE_DRIVER_MANAGEMENT-Flag, wenn <a href="/windows/desktop/api"><strong>Sie CreateDevice aufrufen.</strong></a></span><span class="sxs-lookup"><span data-stu-id="6632d-128">To have Direct3D override the driver so that Direct3D manages resources, use the D3DCREATE_DISABLE_DRIVER_MANAGEMENT flag when calling <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6632d-129">D3DCAPS2_DYNAMICTEXTURES</span><span class="sxs-lookup"><span data-stu-id="6632d-129">D3DCAPS2_DYNAMICTEXTURES</span></span></td>
<td><span data-ttu-id="6632d-130">0x20000000L</span><span class="sxs-lookup"><span data-stu-id="6632d-130">0x20000000L</span></span></td>
<td><span data-ttu-id="6632d-131">Der Treiber unterstützt dynamische Texturen.</span><span class="sxs-lookup"><span data-stu-id="6632d-131">The driver supports dynamic textures.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6632d-132">D3DCAPS2_FULLSCREENGAMMA</span><span class="sxs-lookup"><span data-stu-id="6632d-132">D3DCAPS2_FULLSCREENGAMMA</span></span></td>
<td><span data-ttu-id="6632d-133">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="6632d-133">0x00020000L</span></span></td>
<td><span data-ttu-id="6632d-134">Der Treiber unterstützt die dynamische Gamma-Rampenanpassung im Vollbildmodus.</span><span class="sxs-lookup"><span data-stu-id="6632d-134">The driver supports dynamic gamma ramp adjustment in full-screen mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6632d-135">D3DCAPS2_RESERVED</span><span class="sxs-lookup"><span data-stu-id="6632d-135">D3DCAPS2_RESERVED</span></span></td>
<td><span data-ttu-id="6632d-136">0x02000000L</span><span class="sxs-lookup"><span data-stu-id="6632d-136">0x02000000L</span></span></td>
<td><span data-ttu-id="6632d-137">Reserviert; nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6632d-137">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6632d-138">Diese Konstanten werden vom D3CAPS2-Member von [**D3DCAPS9 verwendet.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="6632d-138">These constants are used by the D3CAPS2 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="6632d-139">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="6632d-139">Constant Information</span></span>



|  <span data-ttu-id="6632d-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6632d-140">Requirement</span></span>                        | <span data-ttu-id="6632d-141">Wert</span><span class="sxs-lookup"><span data-stu-id="6632d-141">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="6632d-142">Header</span><span class="sxs-lookup"><span data-stu-id="6632d-142">Header</span></span>                   | <span data-ttu-id="6632d-143">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="6632d-143">d3d9caps.h</span></span> |
| <span data-ttu-id="6632d-144">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="6632d-144">Minimum operating system</span></span> | <span data-ttu-id="6632d-145">Windows 98</span><span class="sxs-lookup"><span data-stu-id="6632d-145">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6632d-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6632d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6632d-147">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="6632d-147">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
