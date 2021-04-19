---
description: Die idxtcompositor-Schnittstelle legt Eigenschaften für den compositorübergang fest. Diese Schnittstelle wird vom DirectShow-Bearbeitungs Dienst (des) intern verwendet, wenn der compositorübergang gerendert wird.
ms.assetid: 519f1e00-4b67-4014-906b-043f2478baa7
title: Idxtcompositor-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c2e19f555fe01cbec3763bc1dc76d11aeb5f5ecb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356032"
---
# <a name="idxtcompositor-interface"></a><span data-ttu-id="9cd07-103">Idxtcompositor-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9cd07-103">IDxtCompositor interface</span></span>

> [!Note]  
> <span data-ttu-id="9cd07-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="9cd07-104">\[Deprecated.</span></span> <span data-ttu-id="9cd07-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="9cd07-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9cd07-106">Die- `IDxtCompositor` Schnittstelle legt Eigenschaften für den [compositorübergang](compositor-transition.md) fest.</span><span class="sxs-lookup"><span data-stu-id="9cd07-106">The `IDxtCompositor` interface sets properties on the [Compositor](compositor-transition.md) transition.</span></span>

<span data-ttu-id="9cd07-107">Diese Schnittstelle wird vom DirectShow-Bearbeitungs Dienst (des) intern verwendet, wenn der compositorübergang gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="9cd07-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the Compositor transition.</span></span> <span data-ttu-id="9cd07-108">Die-Anwendungen müssen diese Schnittstelle nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="9cd07-108">DES applications do not have to use this interface.</span></span> <span data-ttu-id="9cd07-109">Um die Eigenschaften für einen Übergang in des festzulegen, verwenden Sie die [**ipropertysetter**](ipropertysetter.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9cd07-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

<span data-ttu-id="9cd07-110">Der Compositor-Übergang setzt ein Vordergrundbild auf ein Hintergrundbild zusammen.</span><span class="sxs-lookup"><span data-stu-id="9cd07-110">The Compositor transition composites a foreground image onto a background image.</span></span> <span data-ttu-id="9cd07-111">Das *Quell Rechteck* definiert den Abschnitt des Vordergrund Bilds, das zusammengesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="9cd07-111">The *source rectangle* defines the section of the foreground image that is composited.</span></span> <span data-ttu-id="9cd07-112">Das *Ziel Rechteck* definiert den Abschnitt des Hintergrund Bilds, das das Vordergrundbild empfängt.</span><span class="sxs-lookup"><span data-stu-id="9cd07-112">The *destination rectangle* defines the section of the background image that receives the foreground image.</span></span> <span data-ttu-id="9cd07-113">Das folgende Diagramm veranschaulicht diese Rechtecke.</span><span class="sxs-lookup"><span data-stu-id="9cd07-113">The following diagram illustrates these rectangles.</span></span>

![Eigenschaften des compositorübergangs](images/compmeasure.png)

## <a name="members"></a><span data-ttu-id="9cd07-115">Member</span><span class="sxs-lookup"><span data-stu-id="9cd07-115">Members</span></span>

<span data-ttu-id="9cd07-116">Die **idxtcompositor** -Schnittstelle erbt von **idxeffect**.</span><span class="sxs-lookup"><span data-stu-id="9cd07-116">The **IDxtCompositor** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="9cd07-117">**Idxtcompositor** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9cd07-117">**IDxtCompositor** also has these types of members:</span></span>

-   [<span data-ttu-id="9cd07-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="9cd07-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9cd07-119">Methoden</span><span class="sxs-lookup"><span data-stu-id="9cd07-119">Methods</span></span>

<span data-ttu-id="9cd07-120">Die **idxtcompositor** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="9cd07-120">The **IDxtCompositor** interface has these methods.</span></span>



| <span data-ttu-id="9cd07-121">Methode</span><span class="sxs-lookup"><span data-stu-id="9cd07-121">Method</span></span>                                                   | <span data-ttu-id="9cd07-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9cd07-122">Description</span></span>                                                         |
|:---------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="9cd07-123">**\_Höhe erhalten**</span><span class="sxs-lookup"><span data-stu-id="9cd07-123">**get\_Height**</span></span>](idxtcompositor-get-height.md)         | <span data-ttu-id="9cd07-124">Ruft die Höhe des Ziel Rechtecks ab.</span><span class="sxs-lookup"><span data-stu-id="9cd07-124">Retrieves the height of the target rectangle.</span></span><br/>            |
| [<span data-ttu-id="9cd07-125">**\_OffsetX erhalten**</span><span class="sxs-lookup"><span data-stu-id="9cd07-125">**get\_OffsetX**</span></span>](idxtcompositor-get-offsetx.md)       | <span data-ttu-id="9cd07-126">Ruft den horizontalen Offset des Ziel Rechtecks ab.</span><span class="sxs-lookup"><span data-stu-id="9cd07-126">Retrieves the horizontal offset of the target rectangle.</span></span><br/> |
| [<span data-ttu-id="9cd07-127">**\_offität abrufen**</span><span class="sxs-lookup"><span data-stu-id="9cd07-127">**get\_OffsetY**</span></span>](idxtcompositor-get-offsety.md)       | <span data-ttu-id="9cd07-128">Ruft den vertikalen Offset des Ziel Rechtecks ab.</span><span class="sxs-lookup"><span data-stu-id="9cd07-128">Retrieves the vertical offset of the target rectangle.</span></span><br/>   |
| [<span data-ttu-id="9cd07-129">**\_srcHeight erhalten**</span><span class="sxs-lookup"><span data-stu-id="9cd07-129">**get\_SrcHeight**</span></span>](idxtcompositor-get-srcheight.md)   | <span data-ttu-id="9cd07-130">Ruft die Höhe des Quell Rechtecks ab.</span><span class="sxs-lookup"><span data-stu-id="9cd07-130">Retrieves the height of the source rectangle.</span></span><br/>            |
| [<span data-ttu-id="9cd07-131">**\_srcoffsetx erhalten**</span><span class="sxs-lookup"><span data-stu-id="9cd07-131">**get\_SrcOffsetX**</span></span>](idxtcompositor-get-srcoffsetx.md) | <span data-ttu-id="9cd07-132">Ruft den horizontalen Offset des Quell Rechtecks ab.</span><span class="sxs-lookup"><span data-stu-id="9cd07-132">Retrieves the horizontal offset of the source rectangle.</span></span><br/> |
| [<span data-ttu-id="9cd07-133">**\_srcoff-Ty abrufen**</span><span class="sxs-lookup"><span data-stu-id="9cd07-133">**get\_SrcOffsetY**</span></span>](idxtcompositor-get-srcoffsety.md) | <span data-ttu-id="9cd07-134">Ruft den vertikalen Offset des Quell Rechtecks ab.</span><span class="sxs-lookup"><span data-stu-id="9cd07-134">Retrieves the vertical offset of the source rectangle.</span></span><br/>   |
| [<span data-ttu-id="9cd07-135">**\_srcWidth erhalten**</span><span class="sxs-lookup"><span data-stu-id="9cd07-135">**get\_SrcWidth**</span></span>](idxtcompositor-get-srcwidth.md)     | <span data-ttu-id="9cd07-136">Ruft die Breite des Quell Rechtecks ab.</span><span class="sxs-lookup"><span data-stu-id="9cd07-136">Retrieves the width of the source rectangle.</span></span><br/>             |
| [<span data-ttu-id="9cd07-137">**\_Breite erhalten**</span><span class="sxs-lookup"><span data-stu-id="9cd07-137">**get\_Width**</span></span>](idxtcompositor-get-width.md)           | <span data-ttu-id="9cd07-138">Ruft die Breite des Ziel Rechtecks ab.</span><span class="sxs-lookup"><span data-stu-id="9cd07-138">Retrieves the width of the target rectangle.</span></span><br/>             |
| [<span data-ttu-id="9cd07-139">**\_Höhe ablegen**</span><span class="sxs-lookup"><span data-stu-id="9cd07-139">**put\_Height**</span></span>](idxtcompositor-put-height.md)         | <span data-ttu-id="9cd07-140">Gibt die Höhe des Ziel Rechtecks an.</span><span class="sxs-lookup"><span data-stu-id="9cd07-140">Specifies the height of the target rectangle.</span></span><br/>            |
| [<span data-ttu-id="9cd07-141">**\_OffsetX ablegen**</span><span class="sxs-lookup"><span data-stu-id="9cd07-141">**put\_OffsetX**</span></span>](idxtcompositor-put-offsetx.md)       | <span data-ttu-id="9cd07-142">Gibt den horizontalen Offset des Ziel Rechtecks an.</span><span class="sxs-lookup"><span data-stu-id="9cd07-142">Specifies the horizontal offset of the target rectangle.</span></span><br/> |
| [<span data-ttu-id="9cd07-143">**Put \_ offty**</span><span class="sxs-lookup"><span data-stu-id="9cd07-143">**put\_OffsetY**</span></span>](idxtcompositor-put-offsety.md)       | <span data-ttu-id="9cd07-144">Gibt den vertikalen Offset des Ziel Rechtecks an.</span><span class="sxs-lookup"><span data-stu-id="9cd07-144">Specifies the vertical offset of the target rectangle.</span></span><br/>   |
| [<span data-ttu-id="9cd07-145">**\_srcHeight platzieren**</span><span class="sxs-lookup"><span data-stu-id="9cd07-145">**put\_SrcHeight**</span></span>](idxtcompositor-put-srcheight.md)   | <span data-ttu-id="9cd07-146">Gibt die Höhe des Quell Rechtecks an.</span><span class="sxs-lookup"><span data-stu-id="9cd07-146">Specifies the height of the source rectangle.</span></span><br/>            |
| [<span data-ttu-id="9cd07-147">**\_srcoffsetx platzieren**</span><span class="sxs-lookup"><span data-stu-id="9cd07-147">**put\_SrcOffsetX**</span></span>](idxtcompositor-put-srcoffsetx.md) | <span data-ttu-id="9cd07-148">Gibt den horizontalen Offset des Quell Rechtecks an.</span><span class="sxs-lookup"><span data-stu-id="9cd07-148">Specifies the horizontal offset of the source rectangle.</span></span><br/> |
| [<span data-ttu-id="9cd07-149">**\_srcoff-Ty platzieren**</span><span class="sxs-lookup"><span data-stu-id="9cd07-149">**put\_SrcOffsetY**</span></span>](idxtcompositor-put-srcoffsety.md) | <span data-ttu-id="9cd07-150">Gibt den vertikalen Offset des Quell Rechtecks an.</span><span class="sxs-lookup"><span data-stu-id="9cd07-150">Specifies the vertical offset of the source rectangle.</span></span><br/>   |
| [<span data-ttu-id="9cd07-151">**\_srcWidth platzieren**</span><span class="sxs-lookup"><span data-stu-id="9cd07-151">**put\_SrcWidth**</span></span>](idxtcompositor-put-srcwidth.md)     | <span data-ttu-id="9cd07-152">Gibt die Breite des Quell Rechtecks an.</span><span class="sxs-lookup"><span data-stu-id="9cd07-152">Specifies the width of the source rectangle.</span></span><br/>             |
| [<span data-ttu-id="9cd07-153">**\_Breite platzieren**</span><span class="sxs-lookup"><span data-stu-id="9cd07-153">**put\_Width**</span></span>](idxtcompositor-put-width.md)           | <span data-ttu-id="9cd07-154">Gibt die Breite des Ziel Rechtecks an.</span><span class="sxs-lookup"><span data-stu-id="9cd07-154">Specifies the width of the target rectangle.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="9cd07-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9cd07-155">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9cd07-156">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="9cd07-156">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9cd07-157">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="9cd07-157">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9cd07-158">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9cd07-158">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9cd07-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9cd07-159">Requirements</span></span>



| <span data-ttu-id="9cd07-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9cd07-160">Requirement</span></span> | <span data-ttu-id="9cd07-161">Wert</span><span class="sxs-lookup"><span data-stu-id="9cd07-161">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9cd07-162">Header</span><span class="sxs-lookup"><span data-stu-id="9cd07-162">Header</span></span><br/>  | <dl> <span data-ttu-id="9cd07-163"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="9cd07-163"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9cd07-164">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9cd07-164">Library</span></span><br/> | <dl> <span data-ttu-id="9cd07-165"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="9cd07-165"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




