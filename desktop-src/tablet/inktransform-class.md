---
description: Stellt eine 3X3-Matrix dar, die wiederum eine affine-Transformation darstellt.
ms.assetid: 79abff2e-d1d3-4a32-9ac2-f46c1b21f742
title: Inktransform-Klasse (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkTransform
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 61641f0fed8ec98321e155f82ff9a35150e7fdcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366228"
---
# <a name="inktransform-class"></a><span data-ttu-id="45c23-103">Inktransform-Klasse</span><span class="sxs-lookup"><span data-stu-id="45c23-103">InkTransform class</span></span>

<span data-ttu-id="45c23-104">Stellt eine 3X3-Matrix dar, die wiederum eine affine-Transformation darstellt.</span><span class="sxs-lookup"><span data-stu-id="45c23-104">Represents a 3x3 matrix that, in turn, represents an affine transformation.</span></span>

<span data-ttu-id="45c23-105">**Inktransform** verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="45c23-105">**InkTransform** has these types of members:</span></span>

-   [<span data-ttu-id="45c23-106">Methoden</span><span class="sxs-lookup"><span data-stu-id="45c23-106">Methods</span></span>](#methods)
-   [<span data-ttu-id="45c23-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45c23-107">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="45c23-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="45c23-108">Methods</span></span>

<span data-ttu-id="45c23-109">Die **inktransform** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="45c23-109">The **InkTransform** class has these methods.</span></span>



| <span data-ttu-id="45c23-110">Methode</span><span class="sxs-lookup"><span data-stu-id="45c23-110">Method</span></span>                                                  | <span data-ttu-id="45c23-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45c23-111">Description</span></span>                                                                                                                 |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45c23-112">**GetTransform**</span><span class="sxs-lookup"><span data-stu-id="45c23-112">**GetTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-gettransform)       | <span data-ttu-id="45c23-113">Ruft **inktransform** als 6-Gleit Komma Zahlen ab.</span><span class="sxs-lookup"><span data-stu-id="45c23-113">Retrieves the **InkTransform** as 6 floats.</span></span><br/>                                                                      |
| [<span data-ttu-id="45c23-114">**Widerzuspiegeln**</span><span class="sxs-lookup"><span data-stu-id="45c23-114">**Reflect**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reflect)                 | <span data-ttu-id="45c23-115">Reflektiert die Transformation in horizontaler oder vertikaler Richtung.</span><span class="sxs-lookup"><span data-stu-id="45c23-115">Reflects the transform in either the horizontal or vertical directions.</span></span><br/>                                          |
| [<span data-ttu-id="45c23-116">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="45c23-116">**Reset**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reset)                     | <span data-ttu-id="45c23-117">Setzt die Transformation auf ihren ursprünglichen Zustand zurück.</span><span class="sxs-lookup"><span data-stu-id="45c23-117">Resets the transform to its original state.</span></span><br/>                                                                      |
| [<span data-ttu-id="45c23-118">**Drehen**</span><span class="sxs-lookup"><span data-stu-id="45c23-118">**Rotate**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-rotate)                   | <span data-ttu-id="45c23-119">Dreht die Transformation um einen Winkel in Grad und gibt optional einen Mittelpunkt für die Drehung an.</span><span class="sxs-lookup"><span data-stu-id="45c23-119">Rotates the transform by an angle measured in degrees, and optionally specifies a center point for the rotation.</span></span><br/> |
| [<span data-ttu-id="45c23-120">**ScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="45c23-120">**ScaleTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-scaletransform) | <span data-ttu-id="45c23-121">Skaliert die Transformation um X-und Y-Faktoren.</span><span class="sxs-lookup"><span data-stu-id="45c23-121">Scales the transform by X and Y factors.</span></span><br/>                                                                         |
| [<span data-ttu-id="45c23-122">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="45c23-122">**SetTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-settransform)       | <span data-ttu-id="45c23-123">Ändert die **inktransform** mit 6 Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="45c23-123">Modifies the **InkTransform** using 6 floats.</span></span><br/>                                                                    |
| [<span data-ttu-id="45c23-124">**Scherz**</span><span class="sxs-lookup"><span data-stu-id="45c23-124">**Shear**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-shear)                     | <span data-ttu-id="45c23-125">Wendet eine Schere mit den angegebenen horizontalen und vertikalen Faktoren an.</span><span class="sxs-lookup"><span data-stu-id="45c23-125">Applies a shear with the specified horizontal and vertical factors.</span></span><br/>                                              |
| [<span data-ttu-id="45c23-126">**Übersetzen**</span><span class="sxs-lookup"><span data-stu-id="45c23-126">**Translate**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-translate)             | <span data-ttu-id="45c23-127">Verschiebt die Transformation um die angegebenen horizontalen und vertikalen Komponenten.</span><span class="sxs-lookup"><span data-stu-id="45c23-127">Moves the transform by the specified horizontal and vertical components.</span></span><br/>                                         |



 

### <a name="properties"></a><span data-ttu-id="45c23-128">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="45c23-128">Properties</span></span>

<span data-ttu-id="45c23-129">Die **inktransform** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="45c23-129">The **InkTransform** class has these properties.</span></span>



| <span data-ttu-id="45c23-130">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="45c23-130">Property</span></span>                                     | <span data-ttu-id="45c23-131">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="45c23-131">Access type</span></span>           | <span data-ttu-id="45c23-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45c23-132">Description</span></span>                                                                                          |
|:---------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45c23-133">**Daten**</span><span class="sxs-lookup"><span data-stu-id="45c23-133">**Data**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_data)<br/> | <span data-ttu-id="45c23-134">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="45c23-134">Read/write</span></span><br/> | <span data-ttu-id="45c23-135">Ruft die Automatisierungs Version der Win32 XForm-Struktur ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="45c23-135">Gets or sets the Automation version of the WIN32 XFORM struct.</span></span><br/>                            |
| [<span data-ttu-id="45c23-136">**eDx**</span><span class="sxs-lookup"><span data-stu-id="45c23-136">**eDx**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edx)<br/>   | <span data-ttu-id="45c23-137">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="45c23-137">Read/write</span></span><br/> | <span data-ttu-id="45c23-138">Ruft die reelle Zahl ab, die das Element in der dritten Zeile (erste Spalte) angibt, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="45c23-138">Gets or sets the real number that specifies the element in the third row, first column.</span></span><br/>   |
| [<span data-ttu-id="45c23-139">**Edy**</span><span class="sxs-lookup"><span data-stu-id="45c23-139">**eDy**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edy)<br/>   | <span data-ttu-id="45c23-140">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="45c23-140">Read/write</span></span><br/> | <span data-ttu-id="45c23-141">Ruft die reelle Zahl ab, die das Element in der dritten Zeile, zweiten Spalte angibt, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="45c23-141">Gets or sets the real number that specifies the element in the third row, second column.</span></span><br/>  |
| [<span data-ttu-id="45c23-142">**eM11**</span><span class="sxs-lookup"><span data-stu-id="45c23-142">**eM11**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em11)<br/> | <span data-ttu-id="45c23-143">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="45c23-143">Read/write</span></span><br/> | <span data-ttu-id="45c23-144">Ruft die reelle Zahl ab, die das Element in der ersten Zeile (erste Spalte) angibt, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="45c23-144">Gets or sets the real number that specifies the element in the first row, first column.</span></span><br/>   |
| [<span data-ttu-id="45c23-145">**eM12**</span><span class="sxs-lookup"><span data-stu-id="45c23-145">**eM12**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em12)<br/> | <span data-ttu-id="45c23-146">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="45c23-146">Read/write</span></span><br/> | <span data-ttu-id="45c23-147">Ruft die reelle Zahl ab, die das Element in der ersten Zeile, zweiten Spalte angibt, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="45c23-147">Gets or sets the real number that specifies the element in the first row, second column.</span></span><br/>  |
| [<span data-ttu-id="45c23-148">**eM21**</span><span class="sxs-lookup"><span data-stu-id="45c23-148">**eM21**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em21)<br/> | <span data-ttu-id="45c23-149">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="45c23-149">Read/write</span></span><br/> | <span data-ttu-id="45c23-150">Ruft die reelle Zahl ab, die das Element in der zweiten Zeile (erste Spalte) angibt, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="45c23-150">Gets or sets the real number that specifies the element in the second row, first column.</span></span><br/>  |
| [<span data-ttu-id="45c23-151">**eM22**</span><span class="sxs-lookup"><span data-stu-id="45c23-151">**eM22**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em22)<br/> | <span data-ttu-id="45c23-152">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="45c23-152">Read/write</span></span><br/> | <span data-ttu-id="45c23-153">Ruft die reelle Zahl ab, die das Element in der zweiten Zeile, zweiten Spalte angibt, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="45c23-153">Gets or sets the real number that specifies the element in the second row, second column.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="45c23-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45c23-154">Remarks</span></span>

<span data-ttu-id="45c23-155">Dieses Objekt kann durch Aufrufen der [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode in C++ instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="45c23-155">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="45c23-156">Das-Objekt speichert nur sechs der neun Zahlen in einer 3X3-Matrix, da alle 3X3-Matrizen, die affine Transformationen darstellen, dieselbe dritte Spalte (0, 0, 1) enthalten.</span><span class="sxs-lookup"><span data-stu-id="45c23-156">The object stores only six of the nine numbers in a 3x3 matrix because all 3x3 matrices that represent affine transformations have the same third column (0, 0, 1).</span></span> <span data-ttu-id="45c23-157">Dieses Objekt wird wiederum verwendet, um Transformations Vorgänge zu beschreiben, z. b. das Verschieben, das Scheren, das Skalieren oder das Drehen in einem [**inkrenderer**](inkrenderer-class.md) -Objekt, [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt oder [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="45c23-157">This object in turn is used to describe transformation operations such as moving, shearing, scaling, or rotating in an [**InkRenderer**](inkrenderer-class.md) object, [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object, or [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

> [!Note]  
> <span data-ttu-id="45c23-158">Das **inktransform** -Objekt korreliert mit der [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="45c23-158">The **InkTransform** object correlates to the [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="45c23-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45c23-159">Requirements</span></span>



| <span data-ttu-id="45c23-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45c23-160">Requirement</span></span> | <span data-ttu-id="45c23-161">Wert</span><span class="sxs-lookup"><span data-stu-id="45c23-161">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45c23-162">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="45c23-162">Minimum supported client</span></span><br/> | <span data-ttu-id="45c23-163">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="45c23-163">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="45c23-164">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="45c23-164">Minimum supported server</span></span><br/> | <span data-ttu-id="45c23-165">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="45c23-165">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="45c23-166">Header</span><span class="sxs-lookup"><span data-stu-id="45c23-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="45c23-167"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="45c23-167"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="45c23-168">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="45c23-168">Library</span></span><br/>                  | <dl> <span data-ttu-id="45c23-169"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45c23-169"><dt>InkObj.dll</dt></span></span> </dl>                               |



 

