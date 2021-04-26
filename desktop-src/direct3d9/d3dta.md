---
description: 'Texturargumentkonst constants werden als Werte für die folgenden Member des aufzählten D3DTEXTURESTAGESTATETYPE-Typs verwendet:'
ms.assetid: 36b2b715-5ced-4246-840e-8ea343521ef4
title: D3DTA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898e1bb66f74a1087a9da186599469bb195734ce
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995287"
---
# <a name="d3dta"></a><span data-ttu-id="8abf5-103">D3DTA</span><span class="sxs-lookup"><span data-stu-id="8abf5-103">D3DTA</span></span>

<span data-ttu-id="8abf5-104">Texturargumentkonst constants werden als Werte für die folgenden Member des [**aufzählten D3DTEXTURESTAGESTATETYPE-Typs**](./d3dtexturestagestatetype.md) verwendet:</span><span class="sxs-lookup"><span data-stu-id="8abf5-104">Texture argument constants are used as values for the following members of the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type:</span></span>

-   <span data-ttu-id="8abf5-105">D3DTSS \_ ALPHAARG0</span><span class="sxs-lookup"><span data-stu-id="8abf5-105">D3DTSS\_ALPHAARG0</span></span>
-   <span data-ttu-id="8abf5-106">D3DTSS \_ ALPHAARG1</span><span class="sxs-lookup"><span data-stu-id="8abf5-106">D3DTSS\_ALPHAARG1</span></span>
-   <span data-ttu-id="8abf5-107">D3DTSS \_ ALPHAARG2</span><span class="sxs-lookup"><span data-stu-id="8abf5-107">D3DTSS\_ALPHAARG2</span></span>
-   <span data-ttu-id="8abf5-108">D3DTSS \_ COLORARG0</span><span class="sxs-lookup"><span data-stu-id="8abf5-108">D3DTSS\_COLORARG0</span></span>
-   <span data-ttu-id="8abf5-109">D3DTSS \_ COLORARG1</span><span class="sxs-lookup"><span data-stu-id="8abf5-109">D3DTSS\_COLORARG1</span></span>
-   <span data-ttu-id="8abf5-110">D3DTSS \_ COLORARG2</span><span class="sxs-lookup"><span data-stu-id="8abf5-110">D3DTSS\_COLORARG2</span></span>
-   <span data-ttu-id="8abf5-111">D3DTSS \_ RESULTARG</span><span class="sxs-lookup"><span data-stu-id="8abf5-111">D3DTSS\_RESULTARG</span></span>

<span data-ttu-id="8abf5-112">Legen Sie Texturargumente fest, und rufen Sie sie ab, indem Sie die [**Methoden SetTextureStageState**](/windows/desktop/api) und [**GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8abf5-112">Set and retrieve texture arguments by calling the [**SetTextureStageState**](/windows/desktop/api) and [**GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) methods.</span></span>

<span data-ttu-id="8abf5-113">Argumentflags</span><span class="sxs-lookup"><span data-stu-id="8abf5-113">Argument flags</span></span>

<span data-ttu-id="8abf5-114">Sie können ein Argumentflag mit einem Modifizierer kombinieren, aber zwei Argumentflags können nicht kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="8abf5-114">You can combine an argument flag with a modifier, but two argument flags cannot be combined.</span></span>



| <span data-ttu-id="8abf5-115">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="8abf5-115">\#define</span></span>          | <span data-ttu-id="8abf5-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8abf5-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8abf5-117">D3DTA-KONSTANTE \_</span><span class="sxs-lookup"><span data-stu-id="8abf5-117">D3DTA\_CONSTANT</span></span>   | <span data-ttu-id="8abf5-118">Wählen Sie eine Konstante aus einer Texturphase aus.</span><span class="sxs-lookup"><span data-stu-id="8abf5-118">Select a constant from a texture stage.</span></span> <span data-ttu-id="8abf5-119">Der Standardwert ist 0xffffffff.</span><span class="sxs-lookup"><span data-stu-id="8abf5-119">The default value is 0xffffffff.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="8abf5-120">D3DTA \_ CURRENT</span><span class="sxs-lookup"><span data-stu-id="8abf5-120">D3DTA\_CURRENT</span></span>    | <span data-ttu-id="8abf5-121">Das Texturargument ist das Ergebnis der vorherigen Mischungsphase.</span><span class="sxs-lookup"><span data-stu-id="8abf5-121">The texture argument is the result of the previous blending stage.</span></span> <span data-ttu-id="8abf5-122">In der ersten Texturphase (Phase 0) entspricht dieses Argument D3DTA \_ DIFFUSE.</span><span class="sxs-lookup"><span data-stu-id="8abf5-122">In the first texture stage (stage 0), this argument is equivalent to D3DTA\_DIFFUSE.</span></span> <span data-ttu-id="8abf5-123">Wenn in der vorherigen Mischungsphase eine Bumpmaptextur verwendet wird (D3DTOP \_ BUMPENVMAP-Vorgang), wählt das System die Textur aus der Stufe vor der Bumpmaptextur aus.</span><span class="sxs-lookup"><span data-stu-id="8abf5-123">If the previous blending stage uses a bump-map texture (the D3DTOP\_BUMPENVMAP operation), the system chooses the texture from the stage before the bump-map texture.</span></span> <span data-ttu-id="8abf5-124">Wenn s die aktuelle Texturphase darstellt und s - 1 eine Bumpmaptextur enthält, wird dieses Argument zur Ergebnisausgabe von textur stage s - 2.</span><span class="sxs-lookup"><span data-stu-id="8abf5-124">If s represents the current texture stage and s - 1 contains a bump-map texture, this argument becomes the result output by texture stage s - 2.</span></span> <span data-ttu-id="8abf5-125">Berechtigungen sind Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8abf5-125">Permissions are read/write.</span></span> |
| <span data-ttu-id="8abf5-126">D3DTA \_ DIFFUSE</span><span class="sxs-lookup"><span data-stu-id="8abf5-126">D3DTA\_DIFFUSE</span></span>    | <span data-ttu-id="8abf5-127">Das Texturargument ist die diffuse Farbe, die während der Gouraud-Schattierung von Scheitelpunktkomponenten interpoliert wird.</span><span class="sxs-lookup"><span data-stu-id="8abf5-127">The texture argument is the diffuse color interpolated from vertex components during Gouraud shading.</span></span> <span data-ttu-id="8abf5-128">Wenn der Scheitelpunkt keine diffuse Farbe enthält, wird die Standardfarbe 0xffffffff.</span><span class="sxs-lookup"><span data-stu-id="8abf5-128">If the vertex does not contain a diffuse color, the default color is 0xffffffff.</span></span> <span data-ttu-id="8abf5-129">Berechtigungen sind schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8abf5-129">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="8abf5-130">D3DTA \_ SELECTMASK</span><span class="sxs-lookup"><span data-stu-id="8abf5-130">D3DTA\_SELECTMASK</span></span> | <span data-ttu-id="8abf5-131">Maskierungswert für alle Argumente; wird beim Festlegen von Texturargumenten nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8abf5-131">Mask value for all arguments; not used when setting texture arguments.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="8abf5-132">D3DTA \_ SPECULAR</span><span class="sxs-lookup"><span data-stu-id="8abf5-132">D3DTA\_SPECULAR</span></span>   | <span data-ttu-id="8abf5-133">Das Texturargument ist die Glanzfarbe, die während der Gouraud-Schattierung von Scheitelpunktkomponenten interpoliert wird.</span><span class="sxs-lookup"><span data-stu-id="8abf5-133">The texture argument is the specular color interpolated from vertex components during Gouraud shading.</span></span> <span data-ttu-id="8abf5-134">Wenn der Scheitelpunkt keine Glanzfarbe enthält, wird die Standardfarbe 0xffffffff.</span><span class="sxs-lookup"><span data-stu-id="8abf5-134">If the vertex does not contain a specular color, the default color is 0xffffffff.</span></span> <span data-ttu-id="8abf5-135">Berechtigungen sind schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8abf5-135">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="8abf5-136">D3DTA \_ TEMP</span><span class="sxs-lookup"><span data-stu-id="8abf5-136">D3DTA\_TEMP</span></span>       | <span data-ttu-id="8abf5-137">Das Texturargument ist eine temporäre Registerfarbe für Lese- oder Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8abf5-137">The texture argument is a temporary register color for read or write.</span></span> <span data-ttu-id="8abf5-138">D3DTA \_ TEMP wird unterstützt, wenn die [D3DPMISCCAPS \_ TSSARGTEMP-Gerätefunktion](d3dpmisccaps.md) vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8abf5-138">D3DTA\_TEMP is supported if the [D3DPMISCCAPS\_TSSARGTEMP](d3dpmisccaps.md) device capability is present.</span></span> <span data-ttu-id="8abf5-139">Der Standardwert für das Register ist (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="8abf5-139">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span> <span data-ttu-id="8abf5-140">Berechtigungen sind Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8abf5-140">Permissions are read/write.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="8abf5-141">D3DTA \_ TEXTURE</span><span class="sxs-lookup"><span data-stu-id="8abf5-141">D3DTA\_TEXTURE</span></span>    | <span data-ttu-id="8abf5-142">Das Texturargument ist die Texturfarbe für diese Texturphase.</span><span class="sxs-lookup"><span data-stu-id="8abf5-142">The texture argument is the texture color for this texture stage.</span></span> <span data-ttu-id="8abf5-143">Berechtigungen sind schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8abf5-143">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="8abf5-144">\_D3DTA-TFACTOR</span><span class="sxs-lookup"><span data-stu-id="8abf5-144">D3DTA\_TFACTOR</span></span>    | <span data-ttu-id="8abf5-145">Das Texturargument ist der Texturfaktor, der in einem vorherigen Aufruf von [**SetRenderState**](/windows/desktop/api) mit dem [**D3DRS \_ TEXTUREFACTOR-Renderzustandswert**](./d3drenderstatetype.md) festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="8abf5-145">The texture argument is the texture factor set in a previous call to the [**SetRenderState**](/windows/desktop/api) with the [**D3DRS\_TEXTUREFACTOR**](./d3drenderstatetype.md) render-state value.</span></span> <span data-ttu-id="8abf5-146">Berechtigungen sind schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8abf5-146">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="8abf5-147">Modifiziererflags</span><span class="sxs-lookup"><span data-stu-id="8abf5-147">Modifier flags</span></span>

<span data-ttu-id="8abf5-148">Ein Argumentflag kann mit einem der folgenden Modifiziererflags kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="8abf5-148">An argument flag may be combined with one of the following modifier flags.</span></span>



| <span data-ttu-id="8abf5-149">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="8abf5-149">\#define</span></span>              | <span data-ttu-id="8abf5-150">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8abf5-150">Description</span></span>                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8abf5-151">D3DTA \_ ALPHAREPLICATE</span><span class="sxs-lookup"><span data-stu-id="8abf5-151">D3DTA\_ALPHAREPLICATE</span></span> | <span data-ttu-id="8abf5-152">Replizieren Sie die Alphainformationen in alle Farbkanäle, bevor der Vorgang abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="8abf5-152">Replicate the alpha information to all color channels before the operation completes.</span></span> <span data-ttu-id="8abf5-153">Dies ist ein Lesemodifizierer.</span><span class="sxs-lookup"><span data-stu-id="8abf5-153">This is a read modifier.</span></span> |
| <span data-ttu-id="8abf5-154">\_D3DTA-KOMPLEMENT</span><span class="sxs-lookup"><span data-stu-id="8abf5-154">D3DTA\_COMPLEMENT</span></span>     | <span data-ttu-id="8abf5-155">Nehmen Sie das Komplement des Arguments x, (1.0 - x).</span><span class="sxs-lookup"><span data-stu-id="8abf5-155">Take the complement of the argument x, (1.0 - x).</span></span> <span data-ttu-id="8abf5-156">Dies ist ein Lesemodifizierer.</span><span class="sxs-lookup"><span data-stu-id="8abf5-156">This is a read modifier.</span></span>                                     |



 

## <a name="constant-information"></a><span data-ttu-id="8abf5-157">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="8abf5-157">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="8abf5-158">Header</span><span class="sxs-lookup"><span data-stu-id="8abf5-158">Header</span></span>                   | <span data-ttu-id="8abf5-159">d3d9types.h</span><span class="sxs-lookup"><span data-stu-id="8abf5-159">d3d9types.h</span></span> |
| <span data-ttu-id="8abf5-160">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="8abf5-160">Minimum operating system</span></span> | <span data-ttu-id="8abf5-161">Windows 98</span><span class="sxs-lookup"><span data-stu-id="8abf5-161">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="8abf5-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8abf5-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8abf5-163">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="8abf5-163">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
