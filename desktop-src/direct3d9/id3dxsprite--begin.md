---
description: Bereitet ein Gerät zum Zeichnen von Sprites vor.
ms.assetid: ec9eb069-0a41-4dd5-bbd5-5a31133550b6
title: 'ID3DXSprite:: Begin-Methode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7670c3c516627283a466b3adbb369dc76bbe0d45
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366658"
---
# <a name="id3dxspritebegin-method"></a><span data-ttu-id="3109c-103">ID3DXSprite:: Begin-Methode</span><span class="sxs-lookup"><span data-stu-id="3109c-103">ID3DXSprite::Begin method</span></span>

<span data-ttu-id="3109c-104">Bereitet ein Gerät zum Zeichnen von Sprites vor.</span><span class="sxs-lookup"><span data-stu-id="3109c-104">Prepares a device for drawing sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="3109c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3109c-105">Syntax</span></span>


```C++
HRESULT Begin(
  [in] DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="3109c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3109c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3109c-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="3109c-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3109c-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3109c-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3109c-109">Kombination aus null oder mehr Flags, die Sprite-Renderingoptionen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="3109c-109">Combination of zero or more flags that describe sprite rendering options.</span></span> <span data-ttu-id="3109c-110">Für diese Methode sind die gültigen Flags:</span><span class="sxs-lookup"><span data-stu-id="3109c-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="3109c-111">D3DXSPRITE \_ AlphaBlend</span><span class="sxs-lookup"><span data-stu-id="3109c-111">D3DXSPRITE\_ALPHABLEND</span></span>
-   <span data-ttu-id="3109c-112">D3DXSPRITE- \_ \_ Billboard</span><span class="sxs-lookup"><span data-stu-id="3109c-112">D3DXSPRITE\_\_BILLBOARD</span></span>
-   <span data-ttu-id="3109c-113">D3DXSPRITE \_ donotmodify \_ renderstate</span><span class="sxs-lookup"><span data-stu-id="3109c-113">D3DXSPRITE\_DONOTMODIFY\_RENDERSTATE</span></span>
-   <span data-ttu-id="3109c-114">D3DXSPRITE \_ DoNotSaveState</span><span class="sxs-lookup"><span data-stu-id="3109c-114">D3DXSPRITE\_DONOTSAVESTATE</span></span>
-   <span data-ttu-id="3109c-115">D3DXSPRITE \_ ObjectSpace</span><span class="sxs-lookup"><span data-stu-id="3109c-115">D3DXSPRITE\_OBJECTSPACE</span></span>
-   <span data-ttu-id="3109c-116">D3DXSPRITE \_ \_ Sortier \_ Tiefe zurück \_ wechseln</span><span class="sxs-lookup"><span data-stu-id="3109c-116">D3DXSPRITE\_\_SORT\_DEPTH\_BACKTOFRONT</span></span>
-   <span data-ttu-id="3109c-117">D3DXSPRITE- \_ \_ \_ Detail- \_ frontbackback</span><span class="sxs-lookup"><span data-stu-id="3109c-117">D3DXSPRITE\_\_SORT\_DEPTH\_FRONTTOBACK</span></span>
-   <span data-ttu-id="3109c-118">D3DXSPRITE \_ \_ Sortier \_ Textur</span><span class="sxs-lookup"><span data-stu-id="3109c-118">D3DXSPRITE\_\_SORT\_TEXTURE</span></span>

<span data-ttu-id="3109c-119">Eine Beschreibung der Flags und Informationen zum Steuern der Transformation für Gerätestatus Erfassung und Geräte Ansicht finden Sie unter [D3DXSPRITE](d3dxsprite.md).</span><span class="sxs-lookup"><span data-stu-id="3109c-119">For a description of the flags and for information on how to control device state capture and device view transforms, see [D3DXSPRITE](d3dxsprite.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3109c-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3109c-120">Return value</span></span>

<span data-ttu-id="3109c-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3109c-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3109c-122">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3109c-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3109c-123">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DERR \_ ouesfvideomemory, D3DXERR \_ InvalidData, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="3109c-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3109c-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3109c-124">Remarks</span></span>

<span data-ttu-id="3109c-125">Diese Methode muss innerhalb von [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3109c-125">This method must be called from inside a [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) .</span></span> <span data-ttu-id="3109c-126">.</span><span class="sxs-lookup"><span data-stu-id="3109c-126">.</span></span> <span data-ttu-id="3109c-127">.</span><span class="sxs-lookup"><span data-stu-id="3109c-127">.</span></span> <span data-ttu-id="3109c-128">[**IDirect3DDevice9:: EndScene**](/windows/desktop/api) -Sequenz.</span><span class="sxs-lookup"><span data-stu-id="3109c-128">[**IDirect3DDevice9::EndScene**](/windows/desktop/api) sequence.</span></span> <span data-ttu-id="3109c-129">**ID3DXSprite:: begin** kann nicht als Ersatz für **IDirect3DDevice9:: BeginScene** oder [**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3109c-129">**ID3DXSprite::Begin** cannot be used as a substitute for either **IDirect3DDevice9::BeginScene** or [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md).</span></span>

<span data-ttu-id="3109c-130">Mit dieser Methode werden die folgenden Zustände auf dem Gerät festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3109c-130">This method will set the following states on the device.</span></span>

<span data-ttu-id="3109c-131">Rendering-Zustände:</span><span class="sxs-lookup"><span data-stu-id="3109c-131">Render States:</span></span>



| <span data-ttu-id="3109c-132">Type ([**D3DRENDERSTATETYPE**](./d3drenderstatetype.md))</span><span class="sxs-lookup"><span data-stu-id="3109c-132">Type ([**D3DRENDERSTATETYPE**](./d3drenderstatetype.md))</span></span> | <span data-ttu-id="3109c-133">Wert</span><span class="sxs-lookup"><span data-stu-id="3109c-133">Value</span></span>                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3109c-134">D3DRS \_ AlphaBlendEnable</span><span class="sxs-lookup"><span data-stu-id="3109c-134">D3DRS\_ALPHABLENDENABLE</span></span>                                       | <span data-ttu-id="3109c-135">TRUE</span><span class="sxs-lookup"><span data-stu-id="3109c-135">TRUE</span></span>                                                                                                              |
| <span data-ttu-id="3109c-136">D3DRS \_ alphafunc</span><span class="sxs-lookup"><span data-stu-id="3109c-136">D3DRS\_ALPHAFUNC</span></span>                                              | <span data-ttu-id="3109c-137">D3DCMP \_ größer</span><span class="sxs-lookup"><span data-stu-id="3109c-137">D3DCMP\_GREATER</span></span>                                                                                                   |
| <span data-ttu-id="3109c-138">D3DRS \_ Alpha Aref</span><span class="sxs-lookup"><span data-stu-id="3109c-138">D3DRS\_ALPHAREF</span></span>                                               | <span data-ttu-id="3109c-139">0x00</span><span class="sxs-lookup"><span data-stu-id="3109c-139">0x00</span></span>                                                                                                              |
| <span data-ttu-id="3109c-140">D3DRS \_ Alpha atestenable</span><span class="sxs-lookup"><span data-stu-id="3109c-140">D3DRS\_ALPHATESTENABLE</span></span>                                        | <span data-ttu-id="3109c-141">Alpha acmpcaps</span><span class="sxs-lookup"><span data-stu-id="3109c-141">AlphaCmpCaps</span></span>                                                                                                      |
| <span data-ttu-id="3109c-142">D3DRS \_ blendop</span><span class="sxs-lookup"><span data-stu-id="3109c-142">D3DRS\_BLENDOP</span></span>                                                | <span data-ttu-id="3109c-143">D3DBLENDOP \_ Hinzufügen</span><span class="sxs-lookup"><span data-stu-id="3109c-143">D3DBLENDOP\_ADD</span></span>                                                                                                   |
| <span data-ttu-id="3109c-144">D3DRS \_ Clipping</span><span class="sxs-lookup"><span data-stu-id="3109c-144">D3DRS\_CLIPPING</span></span>                                               | <span data-ttu-id="3109c-145">TRUE</span><span class="sxs-lookup"><span data-stu-id="3109c-145">TRUE</span></span>                                                                                                              |
| <span data-ttu-id="3109c-146">D3DRS \_ clipplaneenable</span><span class="sxs-lookup"><span data-stu-id="3109c-146">D3DRS\_CLIPPLANEENABLE</span></span>                                        | <span data-ttu-id="3109c-147">false</span><span class="sxs-lookup"><span data-stu-id="3109c-147">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="3109c-148">D3DRS \_ colorschreiteenable</span><span class="sxs-lookup"><span data-stu-id="3109c-148">D3DRS\_COLORWRITEENABLE</span></span>                                       | <span data-ttu-id="3109c-149">D3DCOLORWRITEENABLE \_ alpha \| D3DCOLORWRITEENABLE \_ blau \| D3DCOLORWRITEENABLE \_ grün \| D3DCOLORWRITEENABLE \_ rot</span><span class="sxs-lookup"><span data-stu-id="3109c-149">D3DCOLORWRITEENABLE\_ALPHA \| D3DCOLORWRITEENABLE\_BLUE \| D3DCOLORWRITEENABLE\_GREEN \| D3DCOLORWRITEENABLE\_RED</span></span> |
| <span data-ttu-id="3109c-150">D3DRS \_ CullMode</span><span class="sxs-lookup"><span data-stu-id="3109c-150">D3DRS\_CULLMODE</span></span>                                               | <span data-ttu-id="3109c-151">D3DCULL \_ None</span><span class="sxs-lookup"><span data-stu-id="3109c-151">D3DCULL\_NONE</span></span>                                                                                                     |
| <span data-ttu-id="3109c-152">D3DRS \_ destblend</span><span class="sxs-lookup"><span data-stu-id="3109c-152">D3DRS\_DESTBLEND</span></span>                                              | <span data-ttu-id="3109c-153">D3DBLEND- \_ invsrcalpha</span><span class="sxs-lookup"><span data-stu-id="3109c-153">D3DBLEND\_INVSRCALPHA</span></span>                                                                                             |
| <span data-ttu-id="3109c-154">D3DRS \_ DiffuseMaterialSource</span><span class="sxs-lookup"><span data-stu-id="3109c-154">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>                                  | <span data-ttu-id="3109c-155">D3DMCS \_ COLOR1</span><span class="sxs-lookup"><span data-stu-id="3109c-155">D3DMCS\_COLOR1</span></span>                                                                                                    |
| <span data-ttu-id="3109c-156">D3DRS \_ enableadaptivetess</span><span class="sxs-lookup"><span data-stu-id="3109c-156">D3DRS\_ENABLEADAPTIVETESSELLATION</span></span>                             | <span data-ttu-id="3109c-157">false</span><span class="sxs-lookup"><span data-stu-id="3109c-157">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="3109c-158">D3DRS \_ FillMode</span><span class="sxs-lookup"><span data-stu-id="3109c-158">D3DRS\_FILLMODE</span></span>                                               | <span data-ttu-id="3109c-159">D3DFILL \_ Solid</span><span class="sxs-lookup"><span data-stu-id="3109c-159">D3DFILL\_SOLID</span></span>                                                                                                    |
| <span data-ttu-id="3109c-160">D3DRS \_ fogenable</span><span class="sxs-lookup"><span data-stu-id="3109c-160">D3DRS\_FOGENABLE</span></span>                                              | <span data-ttu-id="3109c-161">false</span><span class="sxs-lookup"><span data-stu-id="3109c-161">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="3109c-162">D3DRS \_ indexedvertexblendenable</span><span class="sxs-lookup"><span data-stu-id="3109c-162">D3DRS\_INDEXEDVERTEXBLENDENABLE</span></span>                               | <span data-ttu-id="3109c-163">false</span><span class="sxs-lookup"><span data-stu-id="3109c-163">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="3109c-164">D3DRS- \_ Beleuchtung</span><span class="sxs-lookup"><span data-stu-id="3109c-164">D3DRS\_LIGHTING</span></span>                                               | <span data-ttu-id="3109c-165">false</span><span class="sxs-lookup"><span data-stu-id="3109c-165">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="3109c-166">D3DRS \_ RANGEFOGENABLE</span><span class="sxs-lookup"><span data-stu-id="3109c-166">D3DRS\_RANGEFOGENABLE</span></span>                                         | <span data-ttu-id="3109c-167">false</span><span class="sxs-lookup"><span data-stu-id="3109c-167">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="3109c-168">D3DRS \_ separatealphablendenable</span><span class="sxs-lookup"><span data-stu-id="3109c-168">D3DRS\_SEPARATEALPHABLENDENABLE</span></span>                               | <span data-ttu-id="3109c-169">false</span><span class="sxs-lookup"><span data-stu-id="3109c-169">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="3109c-170">D3DRS \_ SHADEMODE</span><span class="sxs-lookup"><span data-stu-id="3109c-170">D3DRS\_SHADEMODE</span></span>                                              | <span data-ttu-id="3109c-171">D3DSHADE- \_ Gouraud</span><span class="sxs-lookup"><span data-stu-id="3109c-171">D3DSHADE\_GOURAUD</span></span>                                                                                                 |
| <span data-ttu-id="3109c-172">D3DRS \_ specularenable</span><span class="sxs-lookup"><span data-stu-id="3109c-172">D3DRS\_SPECULARENABLE</span></span>                                         | <span data-ttu-id="3109c-173">false</span><span class="sxs-lookup"><span data-stu-id="3109c-173">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="3109c-174">D3DRS \_ srcblend</span><span class="sxs-lookup"><span data-stu-id="3109c-174">D3DRS\_SRCBLEND</span></span>                                               | <span data-ttu-id="3109c-175">D3DBLEND \_ srcalpha</span><span class="sxs-lookup"><span data-stu-id="3109c-175">D3DBLEND\_SRCALPHA</span></span>                                                                                                |
| <span data-ttu-id="3109c-176">D3DRS \_ srgbschreiteenable</span><span class="sxs-lookup"><span data-stu-id="3109c-176">D3DRS\_SRGBWRITEENABLE</span></span>                                        | <span data-ttu-id="3109c-177">false</span><span class="sxs-lookup"><span data-stu-id="3109c-177">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="3109c-178">D3DRS \_ Schablone</span><span class="sxs-lookup"><span data-stu-id="3109c-178">D3DRS\_STENCILENABLE</span></span>                                          | <span data-ttu-id="3109c-179">false</span><span class="sxs-lookup"><span data-stu-id="3109c-179">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="3109c-180">D3DRS \_ vertexblend</span><span class="sxs-lookup"><span data-stu-id="3109c-180">D3DRS\_VERTEXBLEND</span></span>                                            | <span data-ttu-id="3109c-181">false</span><span class="sxs-lookup"><span data-stu-id="3109c-181">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="3109c-182">D3DRS \_ WRAP0</span><span class="sxs-lookup"><span data-stu-id="3109c-182">D3DRS\_WRAP0</span></span>                                                  | <span data-ttu-id="3109c-183">0</span><span class="sxs-lookup"><span data-stu-id="3109c-183">0</span></span>                                                                                                                 |



 

<span data-ttu-id="3109c-184">Textur Stufen Zustände:</span><span class="sxs-lookup"><span data-stu-id="3109c-184">Texture Stage States:</span></span>



| <span data-ttu-id="3109c-185">Phasen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="3109c-185">Stage Identifier</span></span> | <span data-ttu-id="3109c-186">Type ([**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md))</span><span class="sxs-lookup"><span data-stu-id="3109c-186">Type ([**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md))</span></span> | <span data-ttu-id="3109c-187">Wert</span><span class="sxs-lookup"><span data-stu-id="3109c-187">Value</span></span>            |
|------------------|---------------------------------------------------------------------------|------------------|
| <span data-ttu-id="3109c-188">0</span><span class="sxs-lookup"><span data-stu-id="3109c-188">0</span></span>                | <span data-ttu-id="3109c-189">D3DTSS \_ ALPHAARG1</span><span class="sxs-lookup"><span data-stu-id="3109c-189">D3DTSS\_ALPHAARG1</span></span>                                                         | <span data-ttu-id="3109c-190">D3DTA- \_ Textur</span><span class="sxs-lookup"><span data-stu-id="3109c-190">D3DTA\_TEXTURE</span></span>   |
| <span data-ttu-id="3109c-191">0</span><span class="sxs-lookup"><span data-stu-id="3109c-191">0</span></span>                | <span data-ttu-id="3109c-192">D3DTSS \_ ALPHAARG2</span><span class="sxs-lookup"><span data-stu-id="3109c-192">D3DTSS\_ALPHAARG2</span></span>                                                         | <span data-ttu-id="3109c-193">D3DTA \_ diffuses</span><span class="sxs-lookup"><span data-stu-id="3109c-193">D3DTA\_DIFFUSE</span></span>   |
| <span data-ttu-id="3109c-194">0</span><span class="sxs-lookup"><span data-stu-id="3109c-194">0</span></span>                | <span data-ttu-id="3109c-195">D3DTSS \_ alphaop</span><span class="sxs-lookup"><span data-stu-id="3109c-195">D3DTSS\_ALPHAOP</span></span>                                                           | <span data-ttu-id="3109c-196">D3DTOP \_ modulate</span><span class="sxs-lookup"><span data-stu-id="3109c-196">D3DTOP\_MODULATE</span></span> |
| <span data-ttu-id="3109c-197">0</span><span class="sxs-lookup"><span data-stu-id="3109c-197">0</span></span>                | <span data-ttu-id="3109c-198">D3DTSS \_ COLORARG1</span><span class="sxs-lookup"><span data-stu-id="3109c-198">D3DTSS\_COLORARG1</span></span>                                                         | <span data-ttu-id="3109c-199">D3DTA- \_ Textur</span><span class="sxs-lookup"><span data-stu-id="3109c-199">D3DTA\_TEXTURE</span></span>   |
| <span data-ttu-id="3109c-200">0</span><span class="sxs-lookup"><span data-stu-id="3109c-200">0</span></span>                | <span data-ttu-id="3109c-201">D3DTSS \_ COLORARG2</span><span class="sxs-lookup"><span data-stu-id="3109c-201">D3DTSS\_COLORARG2</span></span>                                                         | <span data-ttu-id="3109c-202">D3DTA \_ diffuses</span><span class="sxs-lookup"><span data-stu-id="3109c-202">D3DTA\_DIFFUSE</span></span>   |
| <span data-ttu-id="3109c-203">0</span><span class="sxs-lookup"><span data-stu-id="3109c-203">0</span></span>                | <span data-ttu-id="3109c-204">D3DTSS \_ colorop</span><span class="sxs-lookup"><span data-stu-id="3109c-204">D3DTSS\_COLOROP</span></span>                                                           | <span data-ttu-id="3109c-205">D3DTOP \_ modulate</span><span class="sxs-lookup"><span data-stu-id="3109c-205">D3DTOP\_MODULATE</span></span> |
| <span data-ttu-id="3109c-206">0</span><span class="sxs-lookup"><span data-stu-id="3109c-206">0</span></span>                | <span data-ttu-id="3109c-207">D3DTSS \_ texcoordindex</span><span class="sxs-lookup"><span data-stu-id="3109c-207">D3DTSS\_TEXCOORDINDEX</span></span>                                                     | <span data-ttu-id="3109c-208">0</span><span class="sxs-lookup"><span data-stu-id="3109c-208">0</span></span>                |
| <span data-ttu-id="3109c-209">0</span><span class="sxs-lookup"><span data-stu-id="3109c-209">0</span></span>                | <span data-ttu-id="3109c-210">D3DTSS \_ texturetransformflags</span><span class="sxs-lookup"><span data-stu-id="3109c-210">D3DTSS\_TEXTURETRANSFORMFLAGS</span></span>                                             | <span data-ttu-id="3109c-211">D3DTTFF \_ Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="3109c-211">D3DTTFF\_DISABLE</span></span> |
| <span data-ttu-id="3109c-212">1</span><span class="sxs-lookup"><span data-stu-id="3109c-212">1</span></span>                | <span data-ttu-id="3109c-213">D3DTSS \_ alphaop</span><span class="sxs-lookup"><span data-stu-id="3109c-213">D3DTSS\_ALPHAOP</span></span>                                                           | <span data-ttu-id="3109c-214">D3DTOP \_ Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="3109c-214">D3DTOP\_DISABLE</span></span>  |
| <span data-ttu-id="3109c-215">1</span><span class="sxs-lookup"><span data-stu-id="3109c-215">1</span></span>                | <span data-ttu-id="3109c-216">D3DTSS \_ colorop</span><span class="sxs-lookup"><span data-stu-id="3109c-216">D3DTSS\_COLOROP</span></span>                                                           | <span data-ttu-id="3109c-217">D3DTOP \_ Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="3109c-217">D3DTOP\_DISABLE</span></span>  |



 

<span data-ttu-id="3109c-218">Samplerzustände:</span><span class="sxs-lookup"><span data-stu-id="3109c-218">Sampler States:</span></span>



| <span data-ttu-id="3109c-219">Sampler-Phasen Index</span><span class="sxs-lookup"><span data-stu-id="3109c-219">Sampler Stage Index</span></span> | <span data-ttu-id="3109c-220">Type ([**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md))</span><span class="sxs-lookup"><span data-stu-id="3109c-220">Type ([**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md))</span></span> | <span data-ttu-id="3109c-221">Wert</span><span class="sxs-lookup"><span data-stu-id="3109c-221">Value</span></span>                                                                                                          |
|---------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3109c-222">0</span><span class="sxs-lookup"><span data-stu-id="3109c-222">0</span></span>                   | <span data-ttu-id="3109c-223">D3DSAMP \_ adressu</span><span class="sxs-lookup"><span data-stu-id="3109c-223">D3DSAMP\_ADDRESSU</span></span>                                               | <span data-ttu-id="3109c-224">D3DTADDRESS- \_ Klammer</span><span class="sxs-lookup"><span data-stu-id="3109c-224">D3DTADDRESS\_CLAMP</span></span>                                                                                             |
| <span data-ttu-id="3109c-225">0</span><span class="sxs-lookup"><span data-stu-id="3109c-225">0</span></span>                   | <span data-ttu-id="3109c-226">D3DSAMP \_ adressssv</span><span class="sxs-lookup"><span data-stu-id="3109c-226">D3DSAMP\_ADDRESSV</span></span>                                               | <span data-ttu-id="3109c-227">D3DTADDRESS- \_ Klammer</span><span class="sxs-lookup"><span data-stu-id="3109c-227">D3DTADDRESS\_CLAMP</span></span>                                                                                             |
| <span data-ttu-id="3109c-228">0</span><span class="sxs-lookup"><span data-stu-id="3109c-228">0</span></span>                   | <span data-ttu-id="3109c-229">D3DSAMP- \_ MagFilter</span><span class="sxs-lookup"><span data-stu-id="3109c-229">D3DSAMP\_MAGFILTER</span></span>                                              | <span data-ttu-id="3109c-230">D3DTEXF \_ anisotrope, wenn TextureFilterCaps D3DPTFILTERCAPS \_ magfanisotrope enthält; andernfalls D3DTEXF \_ linear</span><span class="sxs-lookup"><span data-stu-id="3109c-230">D3DTEXF\_ANISOTROPIC if TextureFilterCaps includes D3DPTFILTERCAPS\_MAGFANISOTROPIC; otherwise D3DTEXF\_LINEAR</span></span> |
| <span data-ttu-id="3109c-231">0</span><span class="sxs-lookup"><span data-stu-id="3109c-231">0</span></span>                   | <span data-ttu-id="3109c-232">D3DSAMP \_ MaxMipLevel</span><span class="sxs-lookup"><span data-stu-id="3109c-232">D3DSAMP\_MAXMIPLEVEL</span></span>                                            | <span data-ttu-id="3109c-233">0</span><span class="sxs-lookup"><span data-stu-id="3109c-233">0</span></span>                                                                                                              |
| <span data-ttu-id="3109c-234">0</span><span class="sxs-lookup"><span data-stu-id="3109c-234">0</span></span>                   | <span data-ttu-id="3109c-235">D3DSAMP \_ MaxAnisotropy</span><span class="sxs-lookup"><span data-stu-id="3109c-235">D3DSAMP\_MAXANISOTROPY</span></span>                                          | <span data-ttu-id="3109c-236">Maxanisotropie</span><span class="sxs-lookup"><span data-stu-id="3109c-236">MaxAnisotropy</span></span>                                                                                                  |
| <span data-ttu-id="3109c-237">0</span><span class="sxs-lookup"><span data-stu-id="3109c-237">0</span></span>                   | <span data-ttu-id="3109c-238">D3DSAMP \_ MinFilter</span><span class="sxs-lookup"><span data-stu-id="3109c-238">D3DSAMP\_MINFILTER</span></span>                                              | <span data-ttu-id="3109c-239">D3DTEXF \_ anisotrope, wenn TextureFilterCaps D3DPTFILTERCAPS \_ minfanisotrope enthält; andernfalls D3DTEXF \_ linear</span><span class="sxs-lookup"><span data-stu-id="3109c-239">D3DTEXF\_ANISOTROPIC if TextureFilterCaps includes D3DPTFILTERCAPS\_MINFANISOTROPIC; otherwise D3DTEXF\_LINEAR</span></span> |
| <span data-ttu-id="3109c-240">0</span><span class="sxs-lookup"><span data-stu-id="3109c-240">0</span></span>                   | <span data-ttu-id="3109c-241">D3DSAMP \_ MipFilter</span><span class="sxs-lookup"><span data-stu-id="3109c-241">D3DSAMP\_MIPFILTER</span></span>                                              | <span data-ttu-id="3109c-242">D3DTEXF \_ linear, wenn TextureFilterCaps D3DPTFILTERCAPS \_ mipflinear enthält; andernfalls D3DTEXF \_ Point</span><span class="sxs-lookup"><span data-stu-id="3109c-242">D3DTEXF\_LINEAR if TextureFilterCaps includes D3DPTFILTERCAPS\_MIPFLINEAR; otherwise D3DTEXF\_POINT</span></span>            |
| <span data-ttu-id="3109c-243">0</span><span class="sxs-lookup"><span data-stu-id="3109c-243">0</span></span>                   | <span data-ttu-id="3109c-244">D3DSAMP \_ mipmaplodbias</span><span class="sxs-lookup"><span data-stu-id="3109c-244">D3DSAMP\_MIPMAPLODBIAS</span></span>                                          | <span data-ttu-id="3109c-245">0</span><span class="sxs-lookup"><span data-stu-id="3109c-245">0</span></span>                                                                                                              |
| <span data-ttu-id="3109c-246">0</span><span class="sxs-lookup"><span data-stu-id="3109c-246">0</span></span>                   | <span data-ttu-id="3109c-247">D3DSAMP \_ srgbtexture</span><span class="sxs-lookup"><span data-stu-id="3109c-247">D3DSAMP\_SRGBTEXTURE</span></span>                                            | <span data-ttu-id="3109c-248">0</span><span class="sxs-lookup"><span data-stu-id="3109c-248">0</span></span>                                                                                                              |



 

> [!Note]  
> <span data-ttu-id="3109c-249">Diese Methode deaktiviert N-Patches.</span><span class="sxs-lookup"><span data-stu-id="3109c-249">This method disables N-patches.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3109c-250">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3109c-250">Requirements</span></span>



| <span data-ttu-id="3109c-251">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3109c-251">Requirement</span></span> | <span data-ttu-id="3109c-252">Wert</span><span class="sxs-lookup"><span data-stu-id="3109c-252">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3109c-253">Header</span><span class="sxs-lookup"><span data-stu-id="3109c-253">Header</span></span><br/>  | <dl> <span data-ttu-id="3109c-254"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="3109c-254"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="3109c-255">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3109c-255">Library</span></span><br/> | <dl> <span data-ttu-id="3109c-256"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3109c-256"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3109c-257">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3109c-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3109c-258">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="3109c-258">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="3109c-259">D3DXSPRITE</span><span class="sxs-lookup"><span data-stu-id="3109c-259">D3DXSPRITE</span></span>](d3dxsprite.md)
</dt> </dl>

 

 
