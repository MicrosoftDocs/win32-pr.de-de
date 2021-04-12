---
description: Definiert die Ebenen der multisamplinggrad-voll Szene, die auf dem Gerät angewendet werden können.
ms.assetid: 1a3c1efe-f5b1-47a1-a5f5-ac49d318f3b8
title: D3DMULTISAMPLE_TYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMULTISAMPLE_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: da8f9c1c8bb3aa74c0ab22a5cc701e7d835898de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355066"
---
# <a name="d3dmultisample_type-enumeration"></a><span data-ttu-id="8e835-103">D3DMULTISAMPLE- \_ Typenumeration</span><span class="sxs-lookup"><span data-stu-id="8e835-103">D3DMULTISAMPLE\_TYPE enumeration</span></span>

<span data-ttu-id="8e835-104">Definiert die Ebenen der multisamplinggrad-voll Szene, die auf dem Gerät angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="8e835-104">Defines the levels of full-scene multisampling that the device can apply.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e835-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e835-105">Syntax</span></span>


```C++
typedef enum D3DMULTISAMPLE_TYPE { 
  D3DMULTISAMPLE_NONE          = 0,
  D3DMULTISAMPLE_NONMASKABLE   = 1,
  D3DMULTISAMPLE_2_SAMPLES     = 2,
  D3DMULTISAMPLE_3_SAMPLES     = 3,
  D3DMULTISAMPLE_4_SAMPLES     = 4,
  D3DMULTISAMPLE_5_SAMPLES     = 5,
  D3DMULTISAMPLE_6_SAMPLES     = 6,
  D3DMULTISAMPLE_7_SAMPLES     = 7,
  D3DMULTISAMPLE_8_SAMPLES     = 8,
  D3DMULTISAMPLE_9_SAMPLES     = 9,
  D3DMULTISAMPLE_10_SAMPLES    = 10,
  D3DMULTISAMPLE_11_SAMPLES    = 11,
  D3DMULTISAMPLE_12_SAMPLES    = 12,
  D3DMULTISAMPLE_13_SAMPLES    = 13,
  D3DMULTISAMPLE_14_SAMPLES    = 14,
  D3DMULTISAMPLE_15_SAMPLES    = 15,
  D3DMULTISAMPLE_16_SAMPLES    = 16,
  D3DMULTISAMPLE_FORCE_DWORD   = 0xffffffff
} D3DMULTISAMPLE_TYPE, *LPD3DMULTISAMPLE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="8e835-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="8e835-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8e835-107"><span id="D3DMULTISAMPLE_NONE"></span><span id="d3dmultisample_none"></span>**D3DMULTISAMPLE \_ None**</span><span class="sxs-lookup"><span data-stu-id="8e835-107"><span id="D3DMULTISAMPLE_NONE"></span><span id="d3dmultisample_none"></span>**D3DMULTISAMPLE\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="8e835-108">Es ist keine Ebene der multisamplinggrad-vollständige Szene verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8e835-108">No level of full-scene multisampling is available.</span></span>

</dd> <dt>

<span data-ttu-id="8e835-109"><span id="D3DMULTISAMPLE_NONMASKABLE_"></span><span id="d3dmultisample_nonmaskable_"></span>**D3DMULTISAMPLE \_ Nonmaskable**</span><span class="sxs-lookup"><span data-stu-id="8e835-109"><span id="D3DMULTISAMPLE_NONMASKABLE_"></span><span id="d3dmultisample_nonmaskable_"></span>**D3DMULTISAMPLE\_NONMASKABLE**</span></span> 
</dt> <dd>

<span data-ttu-id="8e835-110">Aktiviert den Qualitäts Wert "Multisampling".</span><span class="sxs-lookup"><span data-stu-id="8e835-110">Enables the multisample quality value.</span></span> <span data-ttu-id="8e835-111">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="8e835-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8e835-112"><span id="D3DMULTISAMPLE_2_SAMPLES"></span><span id="d3dmultisample_2_samples"></span>**D3DMULTISAMPLE \_ 2- \_ Beispiele**</span><span class="sxs-lookup"><span data-stu-id="8e835-112"><span id="D3DMULTISAMPLE_2_SAMPLES"></span><span id="d3dmultisample_2_samples"></span>**D3DMULTISAMPLE\_2\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8e835-113">Verfügbare Ebene der multisamplinggrad-vollständige Szene.</span><span class="sxs-lookup"><span data-stu-id="8e835-113">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8e835-114"><span id="D3DMULTISAMPLE_3_SAMPLES"></span><span id="d3dmultisample_3_samples"></span>**D3DMULTISAMPLE \_ 3- \_ Beispiele**</span><span class="sxs-lookup"><span data-stu-id="8e835-114"><span id="D3DMULTISAMPLE_3_SAMPLES"></span><span id="d3dmultisample_3_samples"></span>**D3DMULTISAMPLE\_3\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8e835-115">Verfügbare Ebene der multisamplinggrad-vollständige Szene.</span><span class="sxs-lookup"><span data-stu-id="8e835-115">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8e835-116"><span id="D3DMULTISAMPLE_4_SAMPLES"></span><span id="d3dmultisample_4_samples"></span>**D3DMULTISAMPLE \_ 4- \_ Beispiele**</span><span class="sxs-lookup"><span data-stu-id="8e835-116"><span id="D3DMULTISAMPLE_4_SAMPLES"></span><span id="d3dmultisample_4_samples"></span>**D3DMULTISAMPLE\_4\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8e835-117">Verfügbare Ebene der multisamplinggrad-vollständige Szene.</span><span class="sxs-lookup"><span data-stu-id="8e835-117">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8e835-118"><span id="D3DMULTISAMPLE_5_SAMPLES"></span><span id="d3dmultisample_5_samples"></span>**D3DMULTISAMPLE \_ 5 \_ Beispiele**</span><span class="sxs-lookup"><span data-stu-id="8e835-118"><span id="D3DMULTISAMPLE_5_SAMPLES"></span><span id="d3dmultisample_5_samples"></span>**D3DMULTISAMPLE\_5\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8e835-119">Verfügbare Ebene der multisamplinggrad-vollständige Szene.</span><span class="sxs-lookup"><span data-stu-id="8e835-119">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8e835-120"><span id="D3DMULTISAMPLE_6_SAMPLES"></span><span id="d3dmultisample_6_samples"></span>**D3DMULTISAMPLE \_ 6- \_ Beispiele**</span><span class="sxs-lookup"><span data-stu-id="8e835-120"><span id="D3DMULTISAMPLE_6_SAMPLES"></span><span id="d3dmultisample_6_samples"></span>**D3DMULTISAMPLE\_6\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8e835-121">Verfügbare Ebene der multisamplinggrad-vollständige Szene.</span><span class="sxs-lookup"><span data-stu-id="8e835-121">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8e835-122"><span id="D3DMULTISAMPLE_7_SAMPLES"></span><span id="d3dmultisample_7_samples"></span>**D3DMULTISAMPLE \_ 7- \_ Beispiele**</span><span class="sxs-lookup"><span data-stu-id="8e835-122"><span id="D3DMULTISAMPLE_7_SAMPLES"></span><span id="d3dmultisample_7_samples"></span>**D3DMULTISAMPLE\_7\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8e835-123">Verfügbare Ebene der multisamplinggrad-vollständige Szene.</span><span class="sxs-lookup"><span data-stu-id="8e835-123">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8e835-124"><span id="D3DMULTISAMPLE_8_SAMPLES"></span><span id="d3dmultisample_8_samples"></span>**D3DMULTISAMPLE \_ 8- \_ Beispiele**</span><span class="sxs-lookup"><span data-stu-id="8e835-124"><span id="D3DMULTISAMPLE_8_SAMPLES"></span><span id="d3dmultisample_8_samples"></span>**D3DMULTISAMPLE\_8\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8e835-125">Verfügbare Ebene der multisamplinggrad-vollständige Szene.</span><span class="sxs-lookup"><span data-stu-id="8e835-125">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8e835-126"><span id="D3DMULTISAMPLE_9_SAMPLES"></span><span id="d3dmultisample_9_samples"></span>**D3DMULTISAMPLE \_ 9- \_ Beispiele**</span><span class="sxs-lookup"><span data-stu-id="8e835-126"><span id="D3DMULTISAMPLE_9_SAMPLES"></span><span id="d3dmultisample_9_samples"></span>**D3DMULTISAMPLE\_9\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8e835-127">Verfügbare Ebene der multisamplinggrad-vollständige Szene.</span><span class="sxs-lookup"><span data-stu-id="8e835-127">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8e835-128"><span id="D3DMULTISAMPLE_10_SAMPLES"></span><span id="d3dmultisample_10_samples"></span>**D3DMULTISAMPLE \_ 10- \_ Beispiele**</span><span class="sxs-lookup"><span data-stu-id="8e835-128"><span id="D3DMULTISAMPLE_10_SAMPLES"></span><span id="d3dmultisample_10_samples"></span>**D3DMULTISAMPLE\_10\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8e835-129">Verfügbare Ebene der multisamplinggrad-vollständige Szene.</span><span class="sxs-lookup"><span data-stu-id="8e835-129">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8e835-130"><span id="D3DMULTISAMPLE_11_SAMPLES"></span><span id="d3dmultisample_11_samples"></span>**D3DMULTISAMPLE \_ 11- \_ Beispiele**</span><span class="sxs-lookup"><span data-stu-id="8e835-130"><span id="D3DMULTISAMPLE_11_SAMPLES"></span><span id="d3dmultisample_11_samples"></span>**D3DMULTISAMPLE\_11\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8e835-131">Verfügbare Ebene der multisamplinggrad-vollständige Szene.</span><span class="sxs-lookup"><span data-stu-id="8e835-131">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8e835-132"><span id="D3DMULTISAMPLE_12_SAMPLES"></span><span id="d3dmultisample_12_samples"></span>**D3DMULTISAMPLE \_ 12- \_ Beispiele**</span><span class="sxs-lookup"><span data-stu-id="8e835-132"><span id="D3DMULTISAMPLE_12_SAMPLES"></span><span id="d3dmultisample_12_samples"></span>**D3DMULTISAMPLE\_12\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8e835-133">Verfügbare Ebene der multisamplinggrad-vollständige Szene.</span><span class="sxs-lookup"><span data-stu-id="8e835-133">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8e835-134"><span id="D3DMULTISAMPLE_13_SAMPLES"></span><span id="d3dmultisample_13_samples"></span>**D3DMULTISAMPLE \_ 13- \_ Beispiele**</span><span class="sxs-lookup"><span data-stu-id="8e835-134"><span id="D3DMULTISAMPLE_13_SAMPLES"></span><span id="d3dmultisample_13_samples"></span>**D3DMULTISAMPLE\_13\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8e835-135">Verfügbare Ebene der multisamplinggrad-vollständige Szene.</span><span class="sxs-lookup"><span data-stu-id="8e835-135">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8e835-136"><span id="D3DMULTISAMPLE_14_SAMPLES"></span><span id="d3dmultisample_14_samples"></span>**D3DMULTISAMPLE \_ 14- \_ Beispiele**</span><span class="sxs-lookup"><span data-stu-id="8e835-136"><span id="D3DMULTISAMPLE_14_SAMPLES"></span><span id="d3dmultisample_14_samples"></span>**D3DMULTISAMPLE\_14\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8e835-137">Verfügbare Ebene der multisamplinggrad-vollständige Szene.</span><span class="sxs-lookup"><span data-stu-id="8e835-137">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8e835-138"><span id="D3DMULTISAMPLE_15_SAMPLES"></span><span id="d3dmultisample_15_samples"></span>**D3DMULTISAMPLE \_ 15 \_ Beispiele**</span><span class="sxs-lookup"><span data-stu-id="8e835-138"><span id="D3DMULTISAMPLE_15_SAMPLES"></span><span id="d3dmultisample_15_samples"></span>**D3DMULTISAMPLE\_15\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8e835-139">Verfügbare Ebene der multisamplinggrad-vollständige Szene.</span><span class="sxs-lookup"><span data-stu-id="8e835-139">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8e835-140"><span id="D3DMULTISAMPLE_16_SAMPLES"></span><span id="d3dmultisample_16_samples"></span>**D3DMULTISAMPLE \_ 16- \_ Beispiele**</span><span class="sxs-lookup"><span data-stu-id="8e835-140"><span id="D3DMULTISAMPLE_16_SAMPLES"></span><span id="d3dmultisample_16_samples"></span>**D3DMULTISAMPLE\_16\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="8e835-141">Verfügbare Ebene der multisamplinggrad-vollständige Szene.</span><span class="sxs-lookup"><span data-stu-id="8e835-141">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="8e835-142"><span id="D3DMULTISAMPLE_FORCE_DWORD"></span><span id="d3dmultisample_force_dword"></span>**D3DMULTISAMPLE \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="8e835-142"><span id="D3DMULTISAMPLE_FORCE_DWORD"></span><span id="d3dmultisample_force_dword"></span>**D3DMULTISAMPLE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="8e835-143">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="8e835-143">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="8e835-144">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="8e835-144">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="8e835-145">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8e835-145">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e835-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e835-146">Remarks</span></span>

<span data-ttu-id="8e835-147">Zusätzlich zur Aktivierung der multisamplinggrad-Funktion für die vollständige Szene bei der [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) -Zeit gibt es Rendering-Zustände, mit denen verschiedene Aspekte auf differenzierten Ebenen ein-und ausgeschaltet werden können.</span><span class="sxs-lookup"><span data-stu-id="8e835-147">In addition to enabling full-scene multisampling at [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) time, there will be render states that turn various aspects on and off at fine-grained levels.</span></span>

<span data-ttu-id="8e835-148">Multisampling ist nur für eine Austausch Kette gültig, die mit dem D3DSWAPEFFECT DISCARD-Swap-Effekt erstellt oder zurückgesetzt wird \_ .</span><span class="sxs-lookup"><span data-stu-id="8e835-148">Multisampling is valid only on a swap chain that is being created or reset with the D3DSWAPEFFECT\_DISCARD swap effect.</span></span>

<span data-ttu-id="8e835-149">Der Multisampling-Antialiasing-Wert kann mit den Parametern (oder unter Parametern) in den folgenden Methoden festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8e835-149">The multisample antialiasing value can be set with the parameters (or sub-parameters) in the following methods.</span></span>



| <span data-ttu-id="8e835-150">Methode</span><span class="sxs-lookup"><span data-stu-id="8e835-150">Method</span></span>                                                                                             | <span data-ttu-id="8e835-151">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e835-151">Parameters</span></span>                         | <span data-ttu-id="8e835-152">Unter Parameter</span><span class="sxs-lookup"><span data-stu-id="8e835-152">Sub-parameters</span></span>                     |
|----------------------------------------------------------------------------------------------------|------------------------------------|------------------------------------|
| [<span data-ttu-id="8e835-153">**IDirect3D9:: checkdevicemultisampletype**</span><span class="sxs-lookup"><span data-stu-id="8e835-153">**IDirect3D9::CheckDeviceMultiSampleType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)           | <span data-ttu-id="8e835-154">MultiSampleType und pqualitylevels</span><span class="sxs-lookup"><span data-stu-id="8e835-154">MultiSampleType and pQualityLevels</span></span> |                                    |
| [<span data-ttu-id="8e835-155">**IDirect3D9:: kreatedevice**</span><span class="sxs-lookup"><span data-stu-id="8e835-155">**IDirect3D9::CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)                                       | <span data-ttu-id="8e835-156">ppresentationparameters</span><span class="sxs-lookup"><span data-stu-id="8e835-156">pPresentationParameters</span></span>            | <span data-ttu-id="8e835-157">MultiSampleType und pqualitylevels</span><span class="sxs-lookup"><span data-stu-id="8e835-157">MultiSampleType and pQualityLevels</span></span> |
| [<span data-ttu-id="8e835-158">**IDirect3DDevice9:: kreateadditionalswapchain**</span><span class="sxs-lookup"><span data-stu-id="8e835-158">**IDirect3DDevice9::CreateAdditionalSwapChain**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) | <span data-ttu-id="8e835-159">ppresentationparameters</span><span class="sxs-lookup"><span data-stu-id="8e835-159">pPresentationParameters</span></span>            | <span data-ttu-id="8e835-160">MultiSampleType und pqualitylevels</span><span class="sxs-lookup"><span data-stu-id="8e835-160">MultiSampleType and pQualityLevels</span></span> |
| [<span data-ttu-id="8e835-161">**IDirect3DDevice9:: kreatedepthstencilsurface**</span><span class="sxs-lookup"><span data-stu-id="8e835-161">**IDirect3DDevice9::CreateDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) | <span data-ttu-id="8e835-162">MultiSampleType und pqualitylevels</span><span class="sxs-lookup"><span data-stu-id="8e835-162">MultiSampleType and pQualityLevels</span></span> |                                    |
| [<span data-ttu-id="8e835-163">**IDirect3DDevice9:: anaterendertarget**</span><span class="sxs-lookup"><span data-stu-id="8e835-163">**IDirect3DDevice9::CreateRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)               | <span data-ttu-id="8e835-164">MultiSampleType und pqualitylevels</span><span class="sxs-lookup"><span data-stu-id="8e835-164">MultiSampleType and pQualityLevels</span></span> |                                    |
| [<span data-ttu-id="8e835-165">**IDirect3DDevice9:: Reset**</span><span class="sxs-lookup"><span data-stu-id="8e835-165">**IDirect3DDevice9::Reset**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)                                         | <span data-ttu-id="8e835-166">ppresentationparameters</span><span class="sxs-lookup"><span data-stu-id="8e835-166">pPresentationParameters</span></span>            | <span data-ttu-id="8e835-167">MultiSampleType und pqualitylevels</span><span class="sxs-lookup"><span data-stu-id="8e835-167">MultiSampleType and pQualityLevels</span></span> |



 

<span data-ttu-id="8e835-168">Es ist nicht empfehlenswert, von einem Multisampling-Typ zu einem anderen zu wechseln, um die Qualität des Antialiasing zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="8e835-168">It is not good practice to switch from one multisample type to another to raise the quality of the antialiasing.</span></span>

<span data-ttu-id="8e835-169">D3DMULTISAMPLE \_ None ermöglicht andere Auslagerungs Effekte als verwerfen, Sperren usw.</span><span class="sxs-lookup"><span data-stu-id="8e835-169">D3DMULTISAMPLE\_NONE enables swap effects other than discarding, locking, and so on.</span></span>

<span data-ttu-id="8e835-170">Unabhängig davon, ob das Anzeigegerät das hochskalierbaren multisamplinggrad unterstützt (mehr als ein Beispiel für ein Renderziel-Format mit mehreren Stichproben Plus Unterstützung für AntiAlias) oder lediglich eine nicht-maskierbarer-multisamplinggrad (nur Unterstützung für AntiAlias), stellt der Treiber für das Gerät die Anzahl der Qualitätsstufen für den D3DMULTISAMPLE \_ nicht maskierbarer Multiple-Sample-Typ</span><span class="sxs-lookup"><span data-stu-id="8e835-170">Whether the display device supports maskable multisampling (more than one sample for a multiple-sample render-target format plus antialias support) or just non-maskable multisampling (only antialias support), the driver for the device provides the number of quality levels for the D3DMULTISAMPLE\_NONMASKABLE multiple-sample type.</span></span> <span data-ttu-id="8e835-171">Anwendungen, die nur multisamplinggrad für Antialiasing-Zwecke verwenden, müssen nur die Anzahl der nicht von der Treiber unterstützten Qualitäts Ebenen mit mehreren Stichproben Abfragen.</span><span class="sxs-lookup"><span data-stu-id="8e835-171">Applications that just use multisampling for antialiasing purposes only need to query for the number of non-maskable multiple-sample quality levels that the driver supports.</span></span>

<span data-ttu-id="8e835-172">Die vom Gerät unterstützten Qualitätsstufen können mit dem pqualitylevels-Parameter von [**IDirect3D9:: checkdevicemultisampletype**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8e835-172">The quality levels supported by the device can be obtained with the pQualityLevels parameter of [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype).</span></span> <span data-ttu-id="8e835-173">Die Qualitätsstufen, die von der Anwendung verwendet werden, werden mit dem multisamplequality-Parameter von [**IDirect3DDevice9:: | atedepthstencilsurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) und [**IDirect3DDevice9:: anaterendertarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8e835-173">Quality levels used by the application are set with the MultiSampleQuality parameter of [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) and [**IDirect3DDevice9::CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget).</span></span>

<span data-ttu-id="8e835-174">Unter D3DRS \_ multisamplemask finden Sie eine Erläuterung der nicht ordnungs fähigen Multisampling.</span><span class="sxs-lookup"><span data-stu-id="8e835-174">See D3DRS\_MULTISAMPLEMASK for discussion of maskable multisampling.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e835-175">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e835-175">Requirements</span></span>



| <span data-ttu-id="8e835-176">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e835-176">Requirement</span></span> | <span data-ttu-id="8e835-177">Wert</span><span class="sxs-lookup"><span data-stu-id="8e835-177">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e835-178">Header</span><span class="sxs-lookup"><span data-stu-id="8e835-178">Header</span></span><br/> | <dl> <span data-ttu-id="8e835-179"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e835-179"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e835-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e835-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e835-181">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="8e835-181">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="8e835-182">**D3DPRESENT- \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="8e835-182">**D3DPRESENT\_PARAMETERS**</span></span>](d3dpresent-parameters.md)
</dt> <dt>

[<span data-ttu-id="8e835-183">**D3DSURFACE- \_ Abteilung**</span><span class="sxs-lookup"><span data-stu-id="8e835-183">**D3DSURFACE\_DESC**</span></span>](d3dsurface-desc.md)
</dt> </dl>

 

 
