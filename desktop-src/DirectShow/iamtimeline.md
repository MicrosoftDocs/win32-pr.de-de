---
description: Die iamtimeline-Schnittstelle stellt Methoden zum Bearbeiten der Zeitachse bereit, das zentrale Objekt in Microsoft DirectShow-Bearbeitungs Diensten (des).
ms.assetid: 6750efa0-946c-4ad3-b0df-de55872b94c3
title: Iamtimeline-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc4374a198232625b87448004b667ccd8ce0183b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356050"
---
# <a name="iamtimeline-interface"></a><span data-ttu-id="52152-103">Iamtimeline-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="52152-103">IAMTimeline interface</span></span>

> [!Note]  
> <span data-ttu-id="52152-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="52152-104">\[Deprecated.</span></span> <span data-ttu-id="52152-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="52152-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="52152-106">Die- `IAMTimeline` Schnittstelle stellt Methoden zum Bearbeiten der Zeitachse bereit, das zentrale Objekt in Microsoft [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="52152-106">The `IAMTimeline` interface provides methods for manipulating the timeline, the central object in Microsoft [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="52152-107">Eine Zeitachse ist eine Auflistung von zeitlich geordneten Elementen, z. b. Videoclips, Audioclips, Effekte und Übergänge zwischen Clips.</span><span class="sxs-lookup"><span data-stu-id="52152-107">A timeline is a collection of time-ordered elements, such as video clips, audio clips, effects, and transitions between clips.</span></span> <span data-ttu-id="52152-108">Die Renderingengine verwendet die Zeitachse, um ein Filter Diagramm zu erstellen, aus dem die Anwendung die gerenderte Ausgabe generieren kann.</span><span class="sxs-lookup"><span data-stu-id="52152-108">The render engine uses the timeline to create a filter graph, from which the application can generate the rendered output.</span></span>

<span data-ttu-id="52152-109">`IAMTimeline` führt drei grundlegende Dienste aus.</span><span class="sxs-lookup"><span data-stu-id="52152-109">`IAMTimeline` performs three basic services.</span></span> <span data-ttu-id="52152-110">Es</span><span class="sxs-lookup"><span data-stu-id="52152-110">It</span></span>

-   <span data-ttu-id="52152-111">Erstellt die-Objekte in der Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="52152-111">Creates the objects in the timeline.</span></span>
-   <span data-ttu-id="52152-112">Fungiert als Container für diese Objekte.</span><span class="sxs-lookup"><span data-stu-id="52152-112">Acts as a container for those objects.</span></span>
-   <span data-ttu-id="52152-113">Legt allgemeine Parameter der Zeitachse fest und ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="52152-113">Sets and retrieves general parameters of the timeline.</span></span>

<span data-ttu-id="52152-114">Um das Timeline-Objekt zu erstellen, rufen Sie **cokreateinstance** mit der Klassen-ID CLSID \_ amtimeline auf.</span><span class="sxs-lookup"><span data-stu-id="52152-114">To create the timeline object, call **CoCreateInstance** with the class identifier CLSID\_AMTimeline.</span></span>

## <a name="members"></a><span data-ttu-id="52152-115">Member</span><span class="sxs-lookup"><span data-stu-id="52152-115">Members</span></span>

<span data-ttu-id="52152-116">Die **iamtimeline** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="52152-116">The **IAMTimeline** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="52152-117">**Iamtimeline** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="52152-117">**IAMTimeline** also has these types of members:</span></span>

-   [<span data-ttu-id="52152-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="52152-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="52152-119">Methoden</span><span class="sxs-lookup"><span data-stu-id="52152-119">Methods</span></span>

<span data-ttu-id="52152-120">Die **iamtimeline** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="52152-120">The **IAMTimeline** interface has these methods.</span></span>



| <span data-ttu-id="52152-121">Methode</span><span class="sxs-lookup"><span data-stu-id="52152-121">Method</span></span>                                                             | <span data-ttu-id="52152-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52152-122">Description</span></span>                                                                                                                       |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="52152-123">**AddGroup**</span><span class="sxs-lookup"><span data-stu-id="52152-123">**AddGroup**</span></span>](iamtimeline-addgroup.md)                           | <span data-ttu-id="52152-124">Fügt der Zeitachse eine Gruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="52152-124">Adds a group to the timeline.</span></span><br/>                                                                                          |
| [<span data-ttu-id="52152-125">**Clearallgroups**</span><span class="sxs-lookup"><span data-stu-id="52152-125">**ClearAllGroups**</span></span>](iamtimeline-clearallgroups.md)               | <span data-ttu-id="52152-126">Entfernt alle Gruppen aus der Zeitachse zusammen mit allen Objekten, die in diesen Gruppen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="52152-126">Removes all groups from the timeline, along with all objects contained in those groups.</span></span><br/>                                |
| [<span data-ttu-id="52152-127">**"Kreateemptynode"**</span><span class="sxs-lookup"><span data-stu-id="52152-127">**CreateEmptyNode**</span></span>](iamtimeline-createemptynode.md)             | <span data-ttu-id="52152-128">Erstellt ein neues Timeline-Objekt.</span><span class="sxs-lookup"><span data-stu-id="52152-128">Creates a new timeline object.</span></span><br/>                                                                                         |
| [<span data-ttu-id="52152-129">**Effectsenabled**</span><span class="sxs-lookup"><span data-stu-id="52152-129">**EffectsEnabled**</span></span>](iamtimeline-effectsenabled.md)               | <span data-ttu-id="52152-130">Bestimmt, ob Effekte aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="52152-130">Determines whether effects are enabled.</span></span><br/>                                                                                |
| [<span data-ttu-id="52152-131">**Enableeffects**</span><span class="sxs-lookup"><span data-stu-id="52152-131">**EnableEffects**</span></span>](iamtimeline-enableeffects.md)                 | <span data-ttu-id="52152-132">Aktiviert oder deaktiviert alle Effekte in der Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="52152-132">Enables or disables all effects in the timeline.</span></span><br/>                                                                       |
| [<span data-ttu-id="52152-133">**Enableübergänge**</span><span class="sxs-lookup"><span data-stu-id="52152-133">**EnableTransitions**</span></span>](iamtimeline-enabletransitions.md)         | <span data-ttu-id="52152-134">Aktiviert oder deaktiviert alle Übergänge in der Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="52152-134">Enables or disables all transitions in the timeline.</span></span><br/>                                                                   |
| [<span data-ttu-id="52152-135">**Getgräfin Service Type**</span><span class="sxs-lookup"><span data-stu-id="52152-135">**GetCountOfType**</span></span>](iamtimeline-getcountoftype.md)               | <span data-ttu-id="52152-136">Ruft die Anzahl der Objekte des angegebenen Typs ab, die in einer angegebenen Gruppe und allen untergeordneten Elementen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="52152-136">Retrieves the number of objects of the specified type that are contained in a specified group and all of its children.</span></span><br/> |
| [<span data-ttu-id="52152-137">**Getdefaulteffect**</span><span class="sxs-lookup"><span data-stu-id="52152-137">**GetDefaultEffect**</span></span>](iamtimeline-getdefaulteffect.md)           | <span data-ttu-id="52152-138">Ruft den Standardeffekt ab.</span><span class="sxs-lookup"><span data-stu-id="52152-138">Retrieves the default effect.</span></span><br/>                                                                                          |
| [<span data-ttu-id="52152-139">**Getdefaulteffectb**</span><span class="sxs-lookup"><span data-stu-id="52152-139">**GetDefaultEffectB**</span></span>](iamtimeline-getdefaulteffectb.md)         | <span data-ttu-id="52152-140">Ruft den Standardeffekt als **BSTR** -Wert ab.</span><span class="sxs-lookup"><span data-stu-id="52152-140">Retrieves the default effect as a **BSTR** value.</span></span><br/>                                                                      |
| [<span data-ttu-id="52152-141">**Getdefaultfps**</span><span class="sxs-lookup"><span data-stu-id="52152-141">**GetDefaultFPS**</span></span>](iamtimeline-getdefaultfps.md)                 | <span data-ttu-id="52152-142">Ruft die Standardausgabe Frame Rate in Frames pro Sekunde ab.</span><span class="sxs-lookup"><span data-stu-id="52152-142">Retrieves the default output frame rate, in frames per second.</span></span><br/>                                                         |
| [<span data-ttu-id="52152-143">**Getdefaulttransition**</span><span class="sxs-lookup"><span data-stu-id="52152-143">**GetDefaultTransition**</span></span>](iamtimeline-getdefaulttransition.md)   | <span data-ttu-id="52152-144">Ruft den Standard Übergang ab.</span><span class="sxs-lookup"><span data-stu-id="52152-144">Retrieves the default transition.</span></span><br/>                                                                                      |
| [<span data-ttu-id="52152-145">**Getdefaulttransitionb**</span><span class="sxs-lookup"><span data-stu-id="52152-145">**GetDefaultTransitionB**</span></span>](iamtimeline-getdefaulttransitionb.md) | <span data-ttu-id="52152-146">Ruft den Standard Übergang als **BSTR** -Wert ab.</span><span class="sxs-lookup"><span data-stu-id="52152-146">Retrieves the default transition as a **BSTR** value.</span></span><br/>                                                                  |
| [<span data-ttu-id="52152-147">**Getdirtyrange**</span><span class="sxs-lookup"><span data-stu-id="52152-147">**GetDirtyRange**</span></span>](iamtimeline-getdirtyrange.md)                 | <span data-ttu-id="52152-148">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="52152-148">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="52152-149">**Getduration**</span><span class="sxs-lookup"><span data-stu-id="52152-149">**GetDuration**</span></span>](iamtimeline-getduration.md)                     | <span data-ttu-id="52152-150">Ruft die Dauer der Zeitachse ab.</span><span class="sxs-lookup"><span data-stu-id="52152-150">Retrieves the timeline duration.</span></span><br/>                                                                                       |
| [<span data-ttu-id="52152-151">**GetDuration2**</span><span class="sxs-lookup"><span data-stu-id="52152-151">**GetDuration2**</span></span>](iamtimeline-getduration2.md)                   | <span data-ttu-id="52152-152">Ruft die Dauer der Zeitachse als **Double** ab.</span><span class="sxs-lookup"><span data-stu-id="52152-152">Retrieves the timeline duration as a **double**.</span></span><br/>                                                                       |
| [<span data-ttu-id="52152-153">**GetGroup**</span><span class="sxs-lookup"><span data-stu-id="52152-153">**GetGroup**</span></span>](iamtimeline-getgroup.md)                           | <span data-ttu-id="52152-154">Ruft eine angegebene Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="52152-154">Retrieves a specified group.</span></span><br/>                                                                                           |
| [<span data-ttu-id="52152-155">**Getgroupcount**</span><span class="sxs-lookup"><span data-stu-id="52152-155">**GetGroupCount**</span></span>](iamtimeline-getgroupcount.md)                 | <span data-ttu-id="52152-156">Ruft die Anzahl der Gruppen ab, die in der Zeitachse enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="52152-156">Retrieves the number of groups that are contained in the timeline.</span></span><br/>                                                     |
| [<span data-ttu-id="52152-157">**Getinsertmode**</span><span class="sxs-lookup"><span data-stu-id="52152-157">**GetInsertMode**</span></span>](iamtimeline-getinsertmode.md)                 | <span data-ttu-id="52152-158">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="52152-158">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="52152-159">**IsDirty**</span><span class="sxs-lookup"><span data-stu-id="52152-159">**IsDirty**</span></span>](iamtimeline-isdirty.md)                             | <span data-ttu-id="52152-160">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="52152-160">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="52152-161">**Remgroupfromlist**</span><span class="sxs-lookup"><span data-stu-id="52152-161">**RemGroupFromList**</span></span>](iamtimeline-remgroupfromlist.md)           | <span data-ttu-id="52152-162">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="52152-162">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="52152-163">**Setdefaulteffect**</span><span class="sxs-lookup"><span data-stu-id="52152-163">**SetDefaultEffect**</span></span>](iamtimeline-setdefaulteffect.md)           | <span data-ttu-id="52152-164">Legt den Standardeffekt fest.</span><span class="sxs-lookup"><span data-stu-id="52152-164">Sets the default effect.</span></span><br/>                                                                                               |
| [<span data-ttu-id="52152-165">**Setdefaulteffectb**</span><span class="sxs-lookup"><span data-stu-id="52152-165">**SetDefaultEffectB**</span></span>](iamtimeline-setdefaulteffectb.md)         | <span data-ttu-id="52152-166">Legt den Standardeffekt als **BSTR** -Wert fest.</span><span class="sxs-lookup"><span data-stu-id="52152-166">Sets the default effect as a **BSTR** value.</span></span><br/>                                                                           |
| [<span data-ttu-id="52152-167">**Setdefaultfps**</span><span class="sxs-lookup"><span data-stu-id="52152-167">**SetDefaultFPS**</span></span>](iamtimeline-setdefaultfps.md)                 | <span data-ttu-id="52152-168">Legt die Standardausgabe Frame Rate in Frames pro Sekunde fest.</span><span class="sxs-lookup"><span data-stu-id="52152-168">Sets the default output frame rate, in frames per second.</span></span><br/>                                                              |
| [<span data-ttu-id="52152-169">**Setdefaulttransition**</span><span class="sxs-lookup"><span data-stu-id="52152-169">**SetDefaultTransition**</span></span>](iamtimeline-setdefaulttransition.md)   | <span data-ttu-id="52152-170">Legt den Standard Übergang fest.</span><span class="sxs-lookup"><span data-stu-id="52152-170">Sets the default transition.</span></span><br/>                                                                                           |
| [<span data-ttu-id="52152-171">**Setdefaulttransitionb**</span><span class="sxs-lookup"><span data-stu-id="52152-171">**SetDefaultTransitionB**</span></span>](iamtimeline-setdefaulttransitionb.md) | <span data-ttu-id="52152-172">Legt den Standard Übergang als BSTR-Wert fest.</span><span class="sxs-lookup"><span data-stu-id="52152-172">Sets the default transition as a BSTR value.</span></span><br/>                                                                           |
| [<span data-ttu-id="52152-173">**"Stinsertmode"**</span><span class="sxs-lookup"><span data-stu-id="52152-173">**SetInsertMode**</span></span>](iamtimeline-setinsertmode.md)                 | <span data-ttu-id="52152-174">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="52152-174">Not implemented.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="52152-175">**Setinterestrange**</span><span class="sxs-lookup"><span data-stu-id="52152-175">**SetInterestRange**</span></span>](iamtimeline-setinterestrange.md)           | <span data-ttu-id="52152-176">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="52152-176">Not implemented.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="52152-177">**Transitionsenabled**</span><span class="sxs-lookup"><span data-stu-id="52152-177">**TransitionsEnabled**</span></span>](iamtimeline-transitionsenabled.md)       | <span data-ttu-id="52152-178">Bestimmt, ob Übergänge aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="52152-178">Determines whether transitions are enabled.</span></span><br/>                                                                            |
| [<span data-ttu-id="52152-179">**Validatesourcenames**</span><span class="sxs-lookup"><span data-stu-id="52152-179">**ValidateSourceNames**</span></span>](iamtimeline-validatesourcenames.md)     | <span data-ttu-id="52152-180">Überprüft die Quellnamen in der Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="52152-180">Validates source names in the timeline.</span></span><br/>                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="52152-181">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52152-181">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="52152-182">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="52152-182">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="52152-183">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="52152-183">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="52152-184">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="52152-184">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="52152-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52152-185">Requirements</span></span>



| <span data-ttu-id="52152-186">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52152-186">Requirement</span></span> | <span data-ttu-id="52152-187">Wert</span><span class="sxs-lookup"><span data-stu-id="52152-187">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52152-188">Header</span><span class="sxs-lookup"><span data-stu-id="52152-188">Header</span></span><br/>  | <dl> <span data-ttu-id="52152-189"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="52152-189"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="52152-190">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="52152-190">Library</span></span><br/> | <dl> <span data-ttu-id="52152-191"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="52152-191"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
