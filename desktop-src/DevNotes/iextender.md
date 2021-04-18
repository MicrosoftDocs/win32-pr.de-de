---
description: Die IExtender-Schnittstelle stellt eine Reihe von grundlegenden Eigenschaften bereit, die der-Schnittstelle eines-Steuer Elements hinzugefügt werden. Programmierer können diese Eigenschaften verwenden, als wären Sie Teil des-Steuer Elements.
ms.assetid: 901873bd-af6a-415e-865f-21769367c99f
title: IExtender-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IExtender
- IExtender.Align
- IExtender.get_Align
- IExtender.put_Align
- IExtender.Enabled
- IExtender.get_Enabled
- IExtender.put_Enabled
- IExtender.Height
- IExtender.get_Height
- IExtender.put_Height
- IExtender.Left
- IExtender.get_Left
- IExtender.put_Left
- IExtender.TabStop
- IExtender.get_TabStop
- IExtender.put_TabStop
- IExtender.Top
- IExtender.get_Top
- IExtender.put_Top
- IExtender.Visible
- IExtender.get_Visible
- IExtender.put_Visible
- IExtender.Width
- IExtender.get_Width
- IExtender.put_Width
- IExtender.Name
- IExtender.get_Name
- IExtender.Parent
- IExtender.get_Parent
- IExtender.Hwnd
- IExtender.get_Hwnd
- IExtender.Container
- IExtender.get_Container
api_type:
- COM
api_location:
- Ole2disp.dll
- Oleaut32.dll
ms.openlocfilehash: fd600de816889e1c644a0e6074d9b8a97e0ec80c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368302"
---
# <a name="iextender-interface"></a><span data-ttu-id="8c295-104">IExtender-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="8c295-104">IExtender interface</span></span>

<span data-ttu-id="8c295-105">Die **IExtender** -Schnittstelle stellt eine Reihe von grundlegenden Eigenschaften bereit, die der-Schnittstelle eines-Steuer Elements hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="8c295-105">The **IExtender** interface provides a set of basic properties that are added to the interface of a control.</span></span> <span data-ttu-id="8c295-106">Programmierer können diese Eigenschaften verwenden, als wären Sie Teil des-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="8c295-106">Programmers can use these properties as if they were part of the control.</span></span>

## <a name="members"></a><span data-ttu-id="8c295-107">Member</span><span class="sxs-lookup"><span data-stu-id="8c295-107">Members</span></span>

<span data-ttu-id="8c295-108">Die **IExtender** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8c295-108">The **IExtender** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8c295-109">**IExtender** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8c295-109">**IExtender** also has these types of members:</span></span>

-   [<span data-ttu-id="8c295-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="8c295-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="8c295-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8c295-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8c295-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="8c295-112">Methods</span></span>

<span data-ttu-id="8c295-113">Die **iextenderschnittstelle** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="8c295-113">The **IExtender** interface has these methods.</span></span>



| <span data-ttu-id="8c295-114">Methode</span><span class="sxs-lookup"><span data-stu-id="8c295-114">Method</span></span>                         | <span data-ttu-id="8c295-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8c295-115">Description</span></span>                                    |
|:-------------------------------|:-----------------------------------------------|
| [<span data-ttu-id="8c295-116">**Move**</span><span class="sxs-lookup"><span data-stu-id="8c295-116">**Move**</span></span>](iextender-move.md) | <span data-ttu-id="8c295-117">Verschiebt eine MDIForm, ein Formular oder ein Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="8c295-117">Moves an MDIForm, form, or control.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8c295-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8c295-118">Properties</span></span>

<span data-ttu-id="8c295-119">Die **iextenderschnittstelle** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8c295-119">The **IExtender** interface has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="8c295-120">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8c295-120">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="8c295-121">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="8c295-121">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="8c295-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8c295-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="8c295-123">Ausrichten</span><span class="sxs-lookup"><span data-stu-id="8c295-123">Align</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="8c295-124">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8c295-124">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="8c295-125">Gibt einen Wert zurück, der bestimmt, ob ein Objekt in einer beliebigen Größe in einem Formular angezeigt wird, oder ob es am oberen, unteren, linken oder rechten Rand des Formulars angezeigt wird und automatisch an die Breite des Formulars angepasst wird, oder legt diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="8c295-125">Returns or sets a value that determines whether an object is displayed in any size anywhere on a form or whether it is displayed at the top, bottom, left, or right of the form and is automatically sized to fit the width of the form.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8c295-126">Konstante</span><span class="sxs-lookup"><span data-stu-id="8c295-126">Constant</span></span></th>
<th><span data-ttu-id="8c295-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8c295-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8c295-128">vbalignnone 0</span><span class="sxs-lookup"><span data-stu-id="8c295-128">vbAlignNone 0</span></span></td>
<td><span data-ttu-id="8c295-129">(Standard in einem nicht-MDI-Formular) None – die Größe und der Speicherort können zur Entwurfszeit oder im Code festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8c295-129">(Default in a non-MDI form) None—size and location can be set at design time or in code.</span></span> <span data-ttu-id="8c295-130">Die Einstellung wird ignoriert, wenn sich das Objekt in einem MDI-Formular befindet.</span><span class="sxs-lookup"><span data-stu-id="8c295-130">The setting is ignored if the object is on an MDI form.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c295-131">vbaligntop 1</span><span class="sxs-lookup"><span data-stu-id="8c295-131">vbAlignTop 1</span></span></td>
<td><span data-ttu-id="8c295-132">(Standard in einem MDI-Formular) Top – das Objekt befindet sich oben im Formular, und seine Breite entspricht der ScaleWidth-Eigenschafts Einstellung des Formulars.</span><span class="sxs-lookup"><span data-stu-id="8c295-132">(Default in an MDI form) Top—the object is at the top of the form, and its width is equal to the ScaleWidth property setting of the form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c295-133">vbalignbottom 2</span><span class="sxs-lookup"><span data-stu-id="8c295-133">vbAlignBottom 2</span></span></td>
<td><span data-ttu-id="8c295-134">Bottom – das Objekt befindet sich am unteren Rand des Formulars, und seine Breite entspricht der ScaleWidth-Eigenschafts Einstellung des Formulars.</span><span class="sxs-lookup"><span data-stu-id="8c295-134">Bottom—the object is at the bottom of the form, and its width is equal to the ScaleWidth property setting of the form.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8c295-135">vbalignleft 3</span><span class="sxs-lookup"><span data-stu-id="8c295-135">vbAlignLeft 3</span></span></td>
<td><span data-ttu-id="8c295-136">Left – das Objekt befindet sich auf der linken Seite des Formulars, und seine Breite entspricht der ScaleWidth-Eigenschafts Einstellung des Formulars.</span><span class="sxs-lookup"><span data-stu-id="8c295-136">Left—the object is at the left of the form, and its width is equal to the ScaleWidth property setting of the form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8c295-137">vbalignright 4</span><span class="sxs-lookup"><span data-stu-id="8c295-137">vbAlignRight 4</span></span></td>
<td><span data-ttu-id="8c295-138">Right – das-Objekt befindet sich rechts vom Formular, und seine Breite entspricht der ScaleWidth-Eigenschafts Einstellung des Formulars.</span><span class="sxs-lookup"><span data-stu-id="8c295-138">Right—the object is at the right of the form, and its width is equal to the ScaleWidth property setting of the form.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="8c295-139">Container</span><span class="sxs-lookup"><span data-stu-id="8c295-139">Container</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="8c295-140">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8c295-140">Read-only</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="8c295-141">Gibt den Container eines-Steuer Elements in einem Formular zurück.</span><span class="sxs-lookup"><span data-stu-id="8c295-141">Returns the container of a control on a form.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="8c295-142">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="8c295-142">Enabled</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="8c295-143">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8c295-143">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="8c295-144">Gibt einen Wert zurück, der bestimmt, ob ein Formular oder Steuerelement auf benutzergenerierte Ereignisse reagieren kann, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="8c295-144">Returns or sets a value that determines whether a form or control can respond to user-generated events.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="8c295-145">Höhe</span><span class="sxs-lookup"><span data-stu-id="8c295-145">Height</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="8c295-146">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8c295-146">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="8c295-147">Gibt die Höhe eines Objekts zurück oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="8c295-147">Returns or sets the height of an object.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="8c295-148">HWND</span><span class="sxs-lookup"><span data-stu-id="8c295-148">Hwnd</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="8c295-149">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8c295-149">Read-only</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="8c295-150">Gibt ein Handle für ein Formular oder Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="8c295-150">Returns a handle to a form or control.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="8c295-151">Links</span><span class="sxs-lookup"><span data-stu-id="8c295-151">Left</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="8c295-152">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8c295-152">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="8c295-153">Gibt den Abstand zwischen dem inneren linken Rand eines Objekts und dem linken Rand seines Containers zurück oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="8c295-153">Returns or sets the distance between the internal left edge of an object and the left edge of its container.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="8c295-154">Name</span><span class="sxs-lookup"><span data-stu-id="8c295-154">Name</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="8c295-155">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8c295-155">Read-only</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="8c295-156">Gibt den Namen zurück, der im Code zum Identifizieren eines Formulars, eines Steuer Elements oder eines Datenzugriffs Objekts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c295-156">Returns the name used in code to identify a form, control, or data access object.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="8c295-157">Parent</span><span class="sxs-lookup"><span data-stu-id="8c295-157">Parent</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="8c295-158">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8c295-158">Read-only</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="8c295-159">Gibt das Formular, das Objekt oder die Auflistung zurück, das ein Steuerelement oder ein anderes Objekt oder eine andere Auflistung enthält.</span><span class="sxs-lookup"><span data-stu-id="8c295-159">Returns the form, object, or collection that contains a control or another object or collection.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="8c295-160">TabStop</span><span class="sxs-lookup"><span data-stu-id="8c295-160">TabStop</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="8c295-161">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8c295-161">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="8c295-162">Gibt einen Wert zurück oder legt einen Wert fest, der angibt, ob ein Benutzer die <strong>Tab</strong> -Taste verwenden kann, um dem Fokus ein Objekt zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="8c295-162">Returns or sets a value that indicates whether a user can use the <strong>Tab</strong> key to give the focus to an object.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="8c295-163">Oben</span><span class="sxs-lookup"><span data-stu-id="8c295-163">Top</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="8c295-164">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8c295-164">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="8c295-165">Gibt den Abstand zwischen dem internen oberen Rand eines Objekts und dem oberen Rand seines Containers zurück oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="8c295-165">Returns or sets the distance between the internal top edge of an object and the top edge of its container.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="8c295-166">Sichtbar</span><span class="sxs-lookup"><span data-stu-id="8c295-166">Visible</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="8c295-167">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8c295-167">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="8c295-168">Gibt einen Wert zurück, der angibt, ob ein Objekt sichtbar oder ausgeblendet ist, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="8c295-168">Returns or sets a value that indicates whether an object is visible or hidden.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="8c295-169">Breite</span><span class="sxs-lookup"><span data-stu-id="8c295-169">Width</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="8c295-170">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8c295-170">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="8c295-171">Gibt die Breite eines-Objekts zurück oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="8c295-171">Returns or sets the width of an object.</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="8c295-172">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c295-172">Requirements</span></span>



| <span data-ttu-id="8c295-173">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c295-173">Requirement</span></span> | <span data-ttu-id="8c295-174">Wert</span><span class="sxs-lookup"><span data-stu-id="8c295-174">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c295-175">DLL</span><span class="sxs-lookup"><span data-stu-id="8c295-175">DLL</span></span><br/> | <dl> <span data-ttu-id="8c295-176"><dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c295-176"><dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt></span></span> </dl> |



 

 
