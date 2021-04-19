---
description: Die idxtjpeg-Schnittstelle legt Eigenschaften für den SMPTE-zurücksetzen-Übergang fest. Diese Schnittstelle wird intern von DirectShow-Bearbeitungs Diensten (de) verwendet, wenn Sie den Übergang der SMPTE-Löschung rendert.
ms.assetid: ce1920d4-ebe5-42d1-a2eb-d71ddeaf14fe
title: Idxtjpeg-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e9c32bee3f4041abaa9529036b7bc78250ac2487
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351278"
---
# <a name="idxtjpeg-interface"></a><span data-ttu-id="3f31f-103">Idxtjpeg-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3f31f-103">IDxtJpeg interface</span></span>

> [!Note]  
> <span data-ttu-id="3f31f-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="3f31f-104">\[Deprecated.</span></span> <span data-ttu-id="3f31f-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="3f31f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3f31f-106">Die- `IDxtJpeg` Schnittstelle legt Eigenschaften für den [SMPTE](smpte-wipe-transition.md) -zurücksetzen-Übergang fest.</span><span class="sxs-lookup"><span data-stu-id="3f31f-106">The `IDxtJpeg` interface sets properties on the [SMPTE Wipe](smpte-wipe-transition.md) transition.</span></span>

<span data-ttu-id="3f31f-107">Diese Schnittstelle wird intern von DirectShow-Bearbeitungs Diensten (de) verwendet, wenn Sie den Übergang der SMPTE-Löschung rendert.</span><span class="sxs-lookup"><span data-stu-id="3f31f-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the SMPTE Wipe transition.</span></span> <span data-ttu-id="3f31f-108">Die-Anwendungen müssen diese Schnittstelle nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="3f31f-108">DES applications do not need to use this interface.</span></span> <span data-ttu-id="3f31f-109">Um die Eigenschaften für einen Übergang in des festzulegen, verwenden Sie die [**ipropertysetter**](ipropertysetter.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3f31f-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="3f31f-110">Member</span><span class="sxs-lookup"><span data-stu-id="3f31f-110">Members</span></span>

<span data-ttu-id="3f31f-111">Die **idxtjpeg** -Schnittstelle erbt von **idxeffect**.</span><span class="sxs-lookup"><span data-stu-id="3f31f-111">The **IDxtJpeg** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="3f31f-112">**Idxtjpeg** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3f31f-112">**IDxtJpeg** also has these types of members:</span></span>

-   [<span data-ttu-id="3f31f-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="3f31f-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3f31f-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="3f31f-114">Methods</span></span>

<span data-ttu-id="3f31f-115">Die **idxtjpeg** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="3f31f-115">The **IDxtJpeg** interface has these methods.</span></span>



| <span data-ttu-id="3f31f-116">Methode</span><span class="sxs-lookup"><span data-stu-id="3f31f-116">Method</span></span>                                                     | <span data-ttu-id="3f31f-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f31f-117">Description</span></span>                                                                               |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f31f-118">**ApplyChanges**</span><span class="sxs-lookup"><span data-stu-id="3f31f-118">**ApplyChanges**</span></span>](idxtjpeg-applychanges.md)              | <span data-ttu-id="3f31f-119">Wendet alle geänderten Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="3f31f-119">Applies any properties that have changed.</span></span><br/>                                      |
| [<span data-ttu-id="3f31f-120">**\_BorderColor erhalten**</span><span class="sxs-lookup"><span data-stu-id="3f31f-120">**get\_BorderColor**</span></span>](idxtjpeg-get-bordercolor.md)       | <span data-ttu-id="3f31f-121">Ruft die Farbe des Rahmens um die Ränder des Entwurfsmusters ab.</span><span class="sxs-lookup"><span data-stu-id="3f31f-121">Retrieves the color of the border around the edges of the wipe pattern.</span></span><br/>        |
| [<span data-ttu-id="3f31f-122">**\_borderweichheit erhalten**</span><span class="sxs-lookup"><span data-stu-id="3f31f-122">**get\_BorderSoftness**</span></span>](idxtjpeg-get-bordersoftness.md) | <span data-ttu-id="3f31f-123">Ruft die Breite des unscharf-Bereichs um die Ränder des-tokenmusters ab.</span><span class="sxs-lookup"><span data-stu-id="3f31f-123">Retrieves the width of the blurry region around the edges of the wipe pattern.</span></span><br/> |
| [<span data-ttu-id="3f31f-124">**\_BorderWidth erhalten**</span><span class="sxs-lookup"><span data-stu-id="3f31f-124">**get\_BorderWidth**</span></span>](idxtjpeg-get-borderwidth.md)       | <span data-ttu-id="3f31f-125">Ruft die Breite des vollständigen Rahmens entlang der Kanten des Abbild Musters ab.</span><span class="sxs-lookup"><span data-stu-id="3f31f-125">Retrieves the width of the solid border along the edges of the wipe pattern.</span></span><br/>   |
| [<span data-ttu-id="3f31f-126">**\_maskname erhalten**</span><span class="sxs-lookup"><span data-stu-id="3f31f-126">**get\_MaskName**</span></span>](idxtjpeg-get-maskname.md)             | <span data-ttu-id="3f31f-127">Ruft den Namen einer JPEG-Datei ab, die als abzurufende Maske verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f31f-127">Retrieves the name of a JPEG file to be used as the wipe mask.</span></span><br/>                 |
| [<span data-ttu-id="3f31f-128">**\_masknum-**</span><span class="sxs-lookup"><span data-stu-id="3f31f-128">**get\_MaskNum**</span></span>](idxtjpeg-get-masknum.md)               | <span data-ttu-id="3f31f-129">Ruft den SMPTE-Code zum Löschen der Löschung ab.</span><span class="sxs-lookup"><span data-stu-id="3f31f-129">Retrieves the SMPTE wipe code of the wipe.</span></span><br/>                                     |
| [<span data-ttu-id="3f31f-130">**\_OffsetX erhalten**</span><span class="sxs-lookup"><span data-stu-id="3f31f-130">**get\_OffsetX**</span></span>](idxtjpeg-get-offsetx.md)               | <span data-ttu-id="3f31f-131">Ruft den horizontalen Offset des Ursprungs zum Löschen ab.</span><span class="sxs-lookup"><span data-stu-id="3f31f-131">Retrieves the horizontal offset of the wipe origin.</span></span><br/>                            |
| [<span data-ttu-id="3f31f-132">**\_offität abrufen**</span><span class="sxs-lookup"><span data-stu-id="3f31f-132">**get\_OffsetY**</span></span>](idxtjpeg-get-offsety.md)               | <span data-ttu-id="3f31f-133">Ruft den vertikalen Offset des Ursprungs zum Löschen ab.</span><span class="sxs-lookup"><span data-stu-id="3f31f-133">Retrieves the vertical offset of the wipe origin.</span></span><br/>                              |
| [<span data-ttu-id="3f31f-134">**\_Repli-Ex repliholen**</span><span class="sxs-lookup"><span data-stu-id="3f31f-134">**get\_ReplicateX**</span></span>](idxtjpeg-get-replicatex.md)         | <span data-ttu-id="3f31f-135">Ruft ab, wie oft das Abbild der Löschung horizontal repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="3f31f-135">Retrieves the number of times the wipe pattern is replicated horizontally.</span></span><br/>     |
| [<span data-ttu-id="3f31f-136">**\_replierhalten**</span><span class="sxs-lookup"><span data-stu-id="3f31f-136">**get\_ReplicateY**</span></span>](idxtjpeg-get-replicatey.md)         | <span data-ttu-id="3f31f-137">Ruft die Häufigkeit ab, mit der das Muster für das Löschen vertikal repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="3f31f-137">Retrieves the number of times the wipe pattern is replicated vertically.</span></span><br/>       |
| [<span data-ttu-id="3f31f-138">**\_ScaleX erhalten**</span><span class="sxs-lookup"><span data-stu-id="3f31f-138">**get\_ScaleX**</span></span>](idxtjpeg-get-scalex.md)                 | <span data-ttu-id="3f31f-139">Ruft den Betrag ab, um den das Löschen horizontal gestreckt wird.</span><span class="sxs-lookup"><span data-stu-id="3f31f-139">Retrieves the amount by which the wipe is stretched horizontally.</span></span><br/>              |
| [<span data-ttu-id="3f31f-140">**get \_ ScaleY**</span><span class="sxs-lookup"><span data-stu-id="3f31f-140">**get\_ScaleY**</span></span>](idxtjpeg-get-scaley.md)                 | <span data-ttu-id="3f31f-141">Ruft den Betrag ab, um den das Löschen vertikal gestreckt wird.</span><span class="sxs-lookup"><span data-stu-id="3f31f-141">Retrieves the amount by which the wipe is stretched vertically.</span></span><br/>                |
| [<span data-ttu-id="3f31f-142">**Loaddefsettings**</span><span class="sxs-lookup"><span data-stu-id="3f31f-142">**LoadDefSettings**</span></span>](idxtjpeg-loaddefsettings.md)        | <span data-ttu-id="3f31f-143">Stellt die Standardeinstellungen des Übergangs Übergangs wieder her.</span><span class="sxs-lookup"><span data-stu-id="3f31f-143">Restores the default settings of the Wipe transition.</span></span><br/>                          |
| [<span data-ttu-id="3f31f-144">**\_BorderColor platzieren**</span><span class="sxs-lookup"><span data-stu-id="3f31f-144">**put\_BorderColor**</span></span>](idxtjpeg-put-bordercolor.md)       | <span data-ttu-id="3f31f-145">Gibt die Farbe des Rahmens um die Ränder des-Token für das Löschen an.</span><span class="sxs-lookup"><span data-stu-id="3f31f-145">Specifies the color of the border around the edges of the wipe pattern.</span></span><br/>        |
| [<span data-ttu-id="3f31f-146">**\_borderweichheit platzieren**</span><span class="sxs-lookup"><span data-stu-id="3f31f-146">**put\_BorderSoftness**</span></span>](idxtjpeg-put-bordersoftness.md) | <span data-ttu-id="3f31f-147">Gibt die Breite des unscharf-Bereichs um die Ränder des Abbild Musters an.</span><span class="sxs-lookup"><span data-stu-id="3f31f-147">Specifies the width of the blurry region around the edges of the wipe pattern.</span></span><br/> |
| [<span data-ttu-id="3f31f-148">**\_BorderWidth platzieren**</span><span class="sxs-lookup"><span data-stu-id="3f31f-148">**put\_BorderWidth**</span></span>](idxtjpeg-put-borderwidth.md)       | <span data-ttu-id="3f31f-149">Gibt die Breite des vollständigen Rahmens entlang der Kanten des Abbild Musters an.</span><span class="sxs-lookup"><span data-stu-id="3f31f-149">Specifies the width of the solid border along the edges of the wipe pattern.</span></span><br/>   |
| [<span data-ttu-id="3f31f-150">**Put \_ maskname**</span><span class="sxs-lookup"><span data-stu-id="3f31f-150">**put\_MaskName**</span></span>](idxtjpeg-put-maskname.md)             | <span data-ttu-id="3f31f-151">Gibt den Namen einer JPEG-Datei an, die als abzurufende Maske verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f31f-151">Specifies the name of a JPEG file to use as the wipe mask.</span></span><br/>                     |
| [<span data-ttu-id="3f31f-152">**\_masknum platzieren**</span><span class="sxs-lookup"><span data-stu-id="3f31f-152">**put\_MaskNum**</span></span>](idxtjpeg-put-masknum.md)               | <span data-ttu-id="3f31f-153">Gibt den SMPTE-Code zum Löschen der Löschung an.</span><span class="sxs-lookup"><span data-stu-id="3f31f-153">Specifies the SMPTE wipe code of the wipe.</span></span><br/>                                     |
| [<span data-ttu-id="3f31f-154">**\_OffsetX ablegen**</span><span class="sxs-lookup"><span data-stu-id="3f31f-154">**put\_OffsetX**</span></span>](idxtjpeg-put-offsetx.md)               | <span data-ttu-id="3f31f-155">Gibt den horizontalen Offset des Ursprungs für das Löschen an.</span><span class="sxs-lookup"><span data-stu-id="3f31f-155">Specifies the horizontal offset of the wipe origin.</span></span><br/>                            |
| [<span data-ttu-id="3f31f-156">**Put \_ offty**</span><span class="sxs-lookup"><span data-stu-id="3f31f-156">**put\_OffsetY**</span></span>](idxtjpeg-put-offsety.md)               | <span data-ttu-id="3f31f-157">Gibt den vertikalen Offset des Ursprungs für das Löschen an.</span><span class="sxs-lookup"><span data-stu-id="3f31f-157">Specifies the vertical offset of the wipe origin.</span></span><br/>                              |
| [<span data-ttu-id="3f31f-158">**\_Repli-Ex platzieren**</span><span class="sxs-lookup"><span data-stu-id="3f31f-158">**put\_ReplicateX**</span></span>](idxtjpeg-put-replicatex.md)         | <span data-ttu-id="3f31f-159">Gibt an, wie oft das Muster für die Löschung horizontal repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="3f31f-159">Specifies the number of times the wipe pattern is replicated horizontally.</span></span><br/>     |
| [<span data-ttu-id="3f31f-160">**versetzen von \_ Repli|**</span><span class="sxs-lookup"><span data-stu-id="3f31f-160">**put\_ReplicateY**</span></span>](idxtjpeg-put-replicatey.md)         | <span data-ttu-id="3f31f-161">Gibt an, wie oft das Muster für die Löschung vertikal repliziert wird.</span><span class="sxs-lookup"><span data-stu-id="3f31f-161">Specifies the number of times the wipe pattern is replicated vertically.</span></span><br/>       |
| [<span data-ttu-id="3f31f-162">**\_ScaleX platzieren**</span><span class="sxs-lookup"><span data-stu-id="3f31f-162">**put\_ScaleX**</span></span>](idxtjpeg-put-scalex.md)                 | <span data-ttu-id="3f31f-163">Gibt den Betrag an, um den das Löschen horizontal gestreckt wird.</span><span class="sxs-lookup"><span data-stu-id="3f31f-163">Specifies the amount by which the wipe is stretched horizontally.</span></span><br/>              |
| [<span data-ttu-id="3f31f-164">**\_skaley platzieren**</span><span class="sxs-lookup"><span data-stu-id="3f31f-164">**put\_ScaleY**</span></span>](idxtjpeg-put-scaley.md)                 | <span data-ttu-id="3f31f-165">Gibt den Betrag an, um den das Löschen vertikal gestreckt wird.</span><span class="sxs-lookup"><span data-stu-id="3f31f-165">Specifies the amount by which the wipe is stretched vertically.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="3f31f-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f31f-166">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3f31f-167">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="3f31f-167">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3f31f-168">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="3f31f-168">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3f31f-169">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3f31f-169">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3f31f-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f31f-170">Requirements</span></span>



| <span data-ttu-id="3f31f-171">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f31f-171">Requirement</span></span> | <span data-ttu-id="3f31f-172">Wert</span><span class="sxs-lookup"><span data-stu-id="3f31f-172">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f31f-173">Header</span><span class="sxs-lookup"><span data-stu-id="3f31f-173">Header</span></span><br/>  | <dl> <span data-ttu-id="3f31f-174"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="3f31f-174"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3f31f-175">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3f31f-175">Library</span></span><br/> | <dl> <span data-ttu-id="3f31f-176"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="3f31f-176"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




