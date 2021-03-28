---
title: texcrd-PS
description: Kopiert Texturkoordinaten Daten aus dem Iterator der Quell Textur Koordinate als Farbdaten im Ziel Register.
ms.assetid: b3330d70-6e18-4494-a01c-51f0a282e305
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e1b7bda7ab06c4af43eaa40393d2c5d64b09d9f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993399"
---
# <a name="texcrd---ps"></a><span data-ttu-id="01d63-103">texcrd-PS</span><span class="sxs-lookup"><span data-stu-id="01d63-103">texcrd - ps</span></span>

<span data-ttu-id="01d63-104">Kopiert Texturkoordinaten Daten aus dem Iterator der Quell Textur Koordinate als Farbdaten im Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="01d63-104">Copies texture coordinate data from the source texture coordinate iterator register as color data in the destination register.</span></span>

## <a name="syntax"></a><span data-ttu-id="01d63-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="01d63-105">Syntax</span></span>



| <span data-ttu-id="01d63-106">texcrd DST, src</span><span class="sxs-lookup"><span data-stu-id="01d63-106">texcrd dst, src</span></span> |
|-----------------|



 

<span data-ttu-id="01d63-107">where</span><span class="sxs-lookup"><span data-stu-id="01d63-107">where</span></span>

-   <span data-ttu-id="01d63-108">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="01d63-108">dst is the destination register.</span></span>
-   <span data-ttu-id="01d63-109">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="01d63-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="01d63-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01d63-110">Remarks</span></span>



| <span data-ttu-id="01d63-111">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="01d63-111">Pixel shader versions</span></span> | <span data-ttu-id="01d63-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="01d63-112">1\_1</span></span> | <span data-ttu-id="01d63-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="01d63-113">1\_2</span></span> | <span data-ttu-id="01d63-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="01d63-114">1\_3</span></span> | <span data-ttu-id="01d63-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="01d63-115">1\_4</span></span> | <span data-ttu-id="01d63-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="01d63-116">2\_0</span></span> | <span data-ttu-id="01d63-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="01d63-117">2\_x</span></span> | <span data-ttu-id="01d63-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="01d63-118">2\_sw</span></span> | <span data-ttu-id="01d63-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="01d63-119">3\_0</span></span> | <span data-ttu-id="01d63-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="01d63-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="01d63-121">texcrd</span><span class="sxs-lookup"><span data-stu-id="01d63-121">texcrd</span></span>                |      |      |      | <span data-ttu-id="01d63-122">x</span><span class="sxs-lookup"><span data-stu-id="01d63-122">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="01d63-123">Diese Anweisung interpretiert Koordinatendaten als Farbdaten (RGBA).</span><span class="sxs-lookup"><span data-stu-id="01d63-123">This instruction interprets coordinate data as color data (RGBA).</span></span>

<span data-ttu-id="01d63-124">Von dieser Anweisung wird keine Textur entnommen.</span><span class="sxs-lookup"><span data-stu-id="01d63-124">No texture is sampled by this instruction.</span></span> <span data-ttu-id="01d63-125">Nur für diese Textur Stufe festgelegte Texturkoordinaten sind relevant.</span><span class="sxs-lookup"><span data-stu-id="01d63-125">Only texture coordinates set on this texture stage are relevant.</span></span>

<span data-ttu-id="01d63-126">Beachten Sie bei der Verwendung von texcrd die folgenden Details dazu, wie Daten aus dem Quell Register in das Ziel Register kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="01d63-126">When using texcrd, keep in mind the following detail about how data is copied from the source register to the destination register.</span></span> <span data-ttu-id="01d63-127">Das Quell Textur-Koordinaten Register (t \# ) enthält Daten im Bereich \[ -D3DCAPS9. MaxTextureRepeat, D3DCAPS9. MaxTextureRepeat \] , während das Ziel Register (r \# ) nur Daten im (wahrscheinlichen kleineren) Bereich enthalten kann, \[ D3DCAPS9. PixelShader1xMaxValue, D3DCAPS9. PixelShader1xMaxValue \] .</span><span class="sxs-lookup"><span data-stu-id="01d63-127">The source texture coordinate register (t\#) holds data in the range \[-D3DCAPS9.MaxTextureRepeat, D3DCAPS9.MaxTextureRepeat\], while the destination register (r\#) can hold data only in the (likely smaller) range \[-D3DCAPS9.PixelShader1xMaxValue, D3DCAPS9.PixelShader1xMaxValue\].</span></span> <span data-ttu-id="01d63-128">Beachten Sie, dass für Pixel Shader \_ , Version 1 4, D3DCAPS9. PixelShader1xMaxValue muss mindestens acht sein.</span><span class="sxs-lookup"><span data-stu-id="01d63-128">Note that for pixel shader version 1\_4, D3DCAPS9.PixelShader1xMaxValue must be a minimum of eight.</span></span> <span data-ttu-id="01d63-129">Die texcrd-Anweisung bei der Klammer von Quelldaten, die sich außerhalb des Bereichs des Ziel Registers befinden, verhält sich wahrscheinlich auf unterschiedlicher Hardware anders.</span><span class="sxs-lookup"><span data-stu-id="01d63-129">The texcrd instruction, in the process of clamping source data that is out of range of the destination register, is likely to behave differently on different hardware.</span></span> <span data-ttu-id="01d63-130">Die erste Pixel-Shader Version 1 \_ 4 Hardware auf dem Markt führt eine spezielle Klammer für Werte außerhalb des Bereichs aus.</span><span class="sxs-lookup"><span data-stu-id="01d63-130">The first pixel shader version 1\_4 hardware on the market will perform a special clamp for values outside of range.</span></span> <span data-ttu-id="01d63-131">Diese Klemme ist darauf ausgelegt, eine Zahl zu schaffen, die in das Ziel Register passt, aber auch, um das Verhalten der Textur Adressierung für außerhalb des Gültigkeits Bereichs stehende Daten beizubehalten (siehe [**D3DTEXTUREADDRESS**](/windows/desktop/direct3d9/d3dtextureaddress)), wenn die Daten anschließend für die Textur Stichprobe verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="01d63-131">This clamp is designed to produce a number that can fit into the destination register, but also to preserve texture addressing behavior for out-of-range data (see [**D3DTEXTUREADDRESS**](/windows/desktop/direct3d9/d3dtextureaddress)) if the data were to be subsequently used for texture sampling.</span></span> <span data-ttu-id="01d63-132">Neue Hardware von unterschiedlichen Herstellern zeigt dieses Verhalten jedoch möglicherweise nicht an und kann nur Daten an den Ziel Registrierungsbereich anpassen.</span><span class="sxs-lookup"><span data-stu-id="01d63-132">However, new hardware from different manufacturers might not exhibit this behavior and might just chop data to fit the destination register range.</span></span> <span data-ttu-id="01d63-133">Daher besteht die sicherste Vorgehensweise bei der Verwendung von PixelShader Version 1 \_ 4 texcrd darin, Texturkoordinaten Daten nur in den Pixelshader anzugeben, der sich bereits im Bereich von \[ -8, 8 befindet, \] sodass Sie sich nicht auf die Art und Weise von Hardware Klammern verlassen können.</span><span class="sxs-lookup"><span data-stu-id="01d63-133">Therefore, the safest course of action when using pixel shader version 1\_4 texcrd is to supply texture coordinate data only into the pixel shader that is already within the range \[-8,8\] so that you do not rely on the way hardware clamps.</span></span>

<span data-ttu-id="01d63-134">Anders als texcoord \_ gibt texcrd keine Werte zwischen 0 und 1 an.</span><span class="sxs-lookup"><span data-stu-id="01d63-134">Unlike texcoord\_, texcrd does not clamp values between 0 and 1.</span></span>

<span data-ttu-id="01d63-135">Regeln für die Verwendung von texcrd:</span><span class="sxs-lookup"><span data-stu-id="01d63-135">Rules for using texcrd :</span></span>

1.  <span data-ttu-id="01d63-136">Derselbe. XYZ-oder. xyw-Modifizierer muss auf jeden Lesevorgang eines einzelnen t (n)-Registers innerhalb einer texcrd-oder texld-Anweisung angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="01d63-136">The same .xyz or .xyw modifier must be applied to every read of an individual t(n) register within a texcrd or texld instruction.</span></span>
2.  <span data-ttu-id="01d63-137">Das vierte kanalergebnis von texcrd ist in allen Fällen nicht festgelegt/nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="01d63-137">The fourth channel result of texcrd is unset/undefined in all cases.</span></span>
3.  <span data-ttu-id="01d63-138">Der dritte Kanal ist für den xyw DW-Fall nicht festgelegt/nicht definiert \_ .</span><span class="sxs-lookup"><span data-stu-id="01d63-138">The third channel is unset/undefined for the xyw\_dw case.</span></span>

## <a name="examples"></a><span data-ttu-id="01d63-139">Beispiele</span><span class="sxs-lookup"><span data-stu-id="01d63-139">Examples</span></span>

<span data-ttu-id="01d63-140">Der vollständige Satz zulässiger Syntax für texcrd, wobei alle gültigen Kombinationen aus quellmodifizierer/Selektor und Ziel Schreib Maske berücksichtigt werden, ist unten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="01d63-140">The complete set of allowed syntax for texcrd, taking into account all valid source modifier/selector and destination write mask combinations, is shown below.</span></span> <span data-ttu-id="01d63-141">Beachten Sie, dass die. RGBA-und. xyzw-Notation austauschbar verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="01d63-141">Note that the .rgba and .xyzw notation can be used interchangeably.</span></span>

<span data-ttu-id="01d63-142">Kopiert die ersten drei Kanäle von Texturkoordinaten iteratorregister, t (n), in r (m).</span><span class="sxs-lookup"><span data-stu-id="01d63-142">Copies first three channels of texture coordinate iterator register, t(n), into r(m).</span></span> <span data-ttu-id="01d63-143">Der vierte Kanal von r (m) ist nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="01d63-143">The fourth channel of r(m) is uninitialized.</span></span>


```
texcrd  r(m).rgb, t(n).xyz  

// Produces the same result as the previous instruction
texcrd  r(m).rgb, t(n)
```



<span data-ttu-id="01d63-144">Legt die ersten, zweiten und vierten Komponenten von t (n) in die ersten drei Kanäle von r (m) ab.</span><span class="sxs-lookup"><span data-stu-id="01d63-144">Puts first, second, and fourth components of t(n) into first three channels of r(m).</span></span> <span data-ttu-id="01d63-145">Der vierte Kanal von r (m) ist nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="01d63-145">The fourth channel of r(m) is uninitialized.</span></span>


```
texcrd  r(m).rgb, t(n).xyw
```



<span data-ttu-id="01d63-146">Im folgenden finden Sie ein Beispiel für eine Projective Teilung mithilfe des \_ DW-Modifizierers.</span><span class="sxs-lookup"><span data-stu-id="01d63-146">Here is a projective divide example using the \_dw modifier.</span></span>

<span data-ttu-id="01d63-147">In diesem Beispiel werden x/w und y/w aus t (n) in die ersten beiden Kanäle von r (m) kopiert.</span><span class="sxs-lookup"><span data-stu-id="01d63-147">This example copies x/w and y/w from t(n) into the first two channels of r(m).</span></span> <span data-ttu-id="01d63-148">Der dritte und vierte Kanal von r (m) sind nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="01d63-148">The third and fourth channels of r(m) are uninitialized.</span></span> <span data-ttu-id="01d63-149">Alle Daten, die zuvor in den dritten Kanal von r (m) geschrieben wurden, gehen verloren.</span><span class="sxs-lookup"><span data-stu-id="01d63-149">Any data previously written to the third channel of r(m) will be lost.</span></span> <span data-ttu-id="01d63-150">Die Daten im vierten Kanal von r (m) gehen aufgrund des Phasen Markers verloren.</span><span class="sxs-lookup"><span data-stu-id="01d63-150">Data in the fourth channel of r(m) is lost due to the phase marker.</span></span> <span data-ttu-id="01d63-151">Bei Version 1 \_ 4 \_ wird das Flag D3DTTFF projiziert ignoriert.</span><span class="sxs-lookup"><span data-stu-id="01d63-151">For version 1\_4, the D3DTTFF\_PROJECTED flag is ignored.</span></span>


```
texcrd  r(m).rg,  t(n)_dw.xyw
```



## <a name="related-topics"></a><span data-ttu-id="01d63-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="01d63-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01d63-153">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="01d63-153">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 