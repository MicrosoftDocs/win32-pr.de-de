---
description: Treiberfunktionsflags.
ms.assetid: 0c0c65fc-f953-4379-a6d0-6ce447a0c183
title: D3DCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb953e73c0ea6b079a6b8f0658790c749b4f30a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343610"
---
# <a name="d3dcaps2"></a><span data-ttu-id="4d3d5-103">D3DCAPS2</span><span class="sxs-lookup"><span data-stu-id="4d3d5-103">D3DCAPS2</span></span>

<span data-ttu-id="4d3d5-104">Treiberfunktionsflags.</span><span class="sxs-lookup"><span data-stu-id="4d3d5-104">Driver capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d3d5-105">#definieren</span><span class="sxs-lookup"><span data-stu-id="4d3d5-105">#define</span></span></td>
<td><span data-ttu-id="4d3d5-106">Wert</span><span class="sxs-lookup"><span data-stu-id="4d3d5-106">Value</span></span></td>
<td><span data-ttu-id="4d3d5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4d3d5-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d3d5-108">D3DCAPS2_CANAUTOGENMIPMAP</span><span class="sxs-lookup"><span data-stu-id="4d3d5-108">D3DCAPS2_CANAUTOGENMIPMAP</span></span></td>
<td><span data-ttu-id="4d3d5-109">0x40000000l</span><span class="sxs-lookup"><span data-stu-id="4d3d5-109">0x40000000L</span></span></td>
<td><span data-ttu-id="4d3d5-110">Der Treiber kann automatisch Mipmaps erstellen.</span><span class="sxs-lookup"><span data-stu-id="4d3d5-110">The driver is capable of automatically generating mipmaps.</span></span> <span data-ttu-id="4d3d5-111">Weitere Informationen finden Sie unter <a href="automatic-generation-of-mipmaps.md">Automatische Generierung von Mipmaps (Direct3D 9)</a>.</span><span class="sxs-lookup"><span data-stu-id="4d3d5-111">For more information, see <a href="automatic-generation-of-mipmaps.md">Automatic Generation of Mipmaps (Direct3D 9)</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d3d5-112">D3DCAPS2_CANCALIBRATEGAMMA</span><span class="sxs-lookup"><span data-stu-id="4d3d5-112">D3DCAPS2_CANCALIBRATEGAMMA</span></span></td>
<td><span data-ttu-id="4d3d5-113">0x00100000l</span><span class="sxs-lookup"><span data-stu-id="4d3d5-113">0x00100000L</span></span></td>
<td><span data-ttu-id="4d3d5-114">Das System verfügt über einen installierten kalierer, der die Gamma-Rampe automatisch anpassen kann, sodass das Ergebnis auf allen Systemen mit einem kalikalierer identisch ist.</span><span class="sxs-lookup"><span data-stu-id="4d3d5-114">The system has a calibrator installed that can automatically adjust the gamma ramp so that the result is identical on all systems that have a calibrator.</span></span> <span data-ttu-id="4d3d5-115">Wenn Sie den kalierer beim Festlegen neuer Gamma Ebenen aufrufen möchten, verwenden Sie das D3DSGR_CALIBRATE-Flag beim Aufrufen von <a href="/windows/desktop/api"><strong>setgammaramp</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4d3d5-115">To invoke the calibrator when setting new gamma levels, use the D3DSGR_CALIBRATE flag when calling <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>.</span></span> <span data-ttu-id="4d3d5-116">Die Kalibrierung von Gamma Rampen verursacht einen gewissen Verarbeitungsaufwand und sollte nicht häufig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4d3d5-116">Calibrating gamma ramps incurs some processing overhead and should not be used frequently.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d3d5-117">D3DCAPS2_CANSHARERESOURCE</span><span class="sxs-lookup"><span data-stu-id="4d3d5-117">D3DCAPS2_CANSHARERESOURCE</span></span></td>
<td><span data-ttu-id="4d3d5-118">0x80000000l</span><span class="sxs-lookup"><span data-stu-id="4d3d5-118">0x80000000L</span></span></td>
<td><span data-ttu-id="4d3d5-119">Das Gerät kann freileg Bare Ressourcen erstellen.</span><span class="sxs-lookup"><span data-stu-id="4d3d5-119">The device can create sharable resources.</span></span> <span data-ttu-id="4d3d5-120">Methoden, die Ressourcen erstellen, können Werte ungleich NULL für Ihre <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>psharedhandle</strong></a> -Parameter festlegen.</span><span class="sxs-lookup"><span data-stu-id="4d3d5-120">Methods that create resources can set non-NULL values for their <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>pSharedHandle</strong></a> parameters.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d3d5-121">Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="4d3d5-121">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="4d3d5-122">Dieses Flag ist nur in Direct3D 9Ex verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4d3d5-122">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d3d5-123">D3DCAPS2_CANMANAGERESOURCE</span><span class="sxs-lookup"><span data-stu-id="4d3d5-123">D3DCAPS2_CANMANAGERESOURCE</span></span></td>
<td><span data-ttu-id="4d3d5-124">0x10000000l</span><span class="sxs-lookup"><span data-stu-id="4d3d5-124">0x10000000L</span></span></td>
<td><span data-ttu-id="4d3d5-125">Der Treiber kann Ressourcen verwalten.</span><span class="sxs-lookup"><span data-stu-id="4d3d5-125">The driver is capable of managing resources.</span></span> <span data-ttu-id="4d3d5-126">Bei solchen Treibern werden D3DPOOL_MANAGED Ressourcen vom Treiber verwaltet.</span><span class="sxs-lookup"><span data-stu-id="4d3d5-126">On such drivers, D3DPOOL_MANAGED resources will be managed by the driver.</span></span> <span data-ttu-id="4d3d5-127">Um Direct3D den Treiber außer Kraft zu setzen, damit Direct3D Ressourcen verwaltet, verwenden Sie das D3DCREATE_DISABLE_DRIVER_MANAGEMENT-Flag beim Aufrufen von <a href="/windows/desktop/api"><strong>createdevice</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4d3d5-127">To have Direct3D override the driver so that Direct3D manages resources, use the D3DCREATE_DISABLE_DRIVER_MANAGEMENT flag when calling <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d3d5-128">D3DCAPS2_DYNAMICTEXTURES</span><span class="sxs-lookup"><span data-stu-id="4d3d5-128">D3DCAPS2_DYNAMICTEXTURES</span></span></td>
<td><span data-ttu-id="4d3d5-129">0x20000000l</span><span class="sxs-lookup"><span data-stu-id="4d3d5-129">0x20000000L</span></span></td>
<td><span data-ttu-id="4d3d5-130">Der Treiber unterstützt dynamische Texturen.</span><span class="sxs-lookup"><span data-stu-id="4d3d5-130">The driver supports dynamic textures.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d3d5-131">D3DCAPS2_FULLSCREENGAMMA</span><span class="sxs-lookup"><span data-stu-id="4d3d5-131">D3DCAPS2_FULLSCREENGAMMA</span></span></td>
<td><span data-ttu-id="4d3d5-132">0x00020000l</span><span class="sxs-lookup"><span data-stu-id="4d3d5-132">0x00020000L</span></span></td>
<td><span data-ttu-id="4d3d5-133">Der Treiber unterstützt die dynamische Gamma Rampen Anpassung im Vollbildmodus.</span><span class="sxs-lookup"><span data-stu-id="4d3d5-133">The driver supports dynamic gamma ramp adjustment in full-screen mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d3d5-134">D3DCAPS2_RESERVED</span><span class="sxs-lookup"><span data-stu-id="4d3d5-134">D3DCAPS2_RESERVED</span></span></td>
<td><span data-ttu-id="4d3d5-135">0x02000000l</span><span class="sxs-lookup"><span data-stu-id="4d3d5-135">0x02000000L</span></span></td>
<td><span data-ttu-id="4d3d5-136">Bleiben nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4d3d5-136">Reserved; not used.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4d3d5-137">Diese Konstanten werden vom D3CAPS2-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.</span><span class="sxs-lookup"><span data-stu-id="4d3d5-137">These constants are used by the D3CAPS2 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="4d3d5-138">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="4d3d5-138">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="4d3d5-139">Header</span><span class="sxs-lookup"><span data-stu-id="4d3d5-139">Header</span></span>                   | <span data-ttu-id="4d3d5-140">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="4d3d5-140">d3d9caps.h</span></span> |
| <span data-ttu-id="4d3d5-141">Mindestens Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="4d3d5-141">Minimum operating system</span></span> | <span data-ttu-id="4d3d5-142">Windows 98</span><span class="sxs-lookup"><span data-stu-id="4d3d5-142">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4d3d5-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4d3d5-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d3d5-144">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="4d3d5-144">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
