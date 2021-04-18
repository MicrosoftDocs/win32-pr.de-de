---
description: Die iamtimelinetrans-Schnittstelle stellt Methoden zum Bearbeiten von Übergängen in DirectShow-Bearbeitungs Diensten bereit.
ms.assetid: e29ff0cc-0e48-4a72-8a1b-051ed62c8130
title: Iamtimelinetrans-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cd3c39d0a5434befdd5607b340fef936644bf48e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365805"
---
# <a name="iamtimelinetrans-interface"></a><span data-ttu-id="17dc1-103">Iamtimelinetrans-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="17dc1-103">IAMTimelineTrans interface</span></span>

> [!Note]  
> <span data-ttu-id="17dc1-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="17dc1-104">\[Deprecated.</span></span> <span data-ttu-id="17dc1-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="17dc1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="17dc1-106">Die- `IAMTimelineTrans` Schnittstelle stellt Methoden zum Ändern von Übergängen in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) bereit.</span><span class="sxs-lookup"><span data-stu-id="17dc1-106">The `IAMTimelineTrans` interface provides methods for manipulating transitions in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="17dc1-107">Ein Übergang ist ein Fortschritt zwischen einer Video Ebene und dem gerenderten zusammengesetzten aller Video Ebenen mit niedrigerer Priorität.</span><span class="sxs-lookup"><span data-stu-id="17dc1-107">A transition is a progression between one video layer and the rendered composite of all video layers with a lower priority.</span></span> <span data-ttu-id="17dc1-108">Einem Zeitachsen Objekt, das die [**iamtimelinetransable**](iamtimelinetransable.md) -Schnittstelle verfügbar macht, kann ein Übergang hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="17dc1-108">A transition can be added to any timeline object that exposes the [**IAMTimelineTransable**](iamtimelinetransable.md) interface.</span></span> <span data-ttu-id="17dc1-109">Um Eigenschaften für einen Übergang festzulegen, verwenden Sie die [**ipropertysetter**](ipropertysetter.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="17dc1-109">To set properties on a transition, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

<span data-ttu-id="17dc1-110">Das des-Übergangs Objekt ist tatsächlich ein Wrapper für ein DirectX-Transformations Objekt.</span><span class="sxs-lookup"><span data-stu-id="17dc1-110">The DES transition object is actually a wrapper for a DirectX Transform object.</span></span> <span data-ttu-id="17dc1-111">Ein DirectX-Transformations Objekt mit 2 Eingaben kann verwendet werden, um den visuellen Effekt für den Übergang zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="17dc1-111">Any 2-input DirectX Transform object can be used to implement the visual effect for the transition.</span></span> <span data-ttu-id="17dc1-112">Microsoft unterstützt die Entwicklung von DirectX-Transformations Objekten von Drittanbietern nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="17dc1-112">Microsoft no longer supports the development of third-party DirectX Transform objects.</span></span> <span data-ttu-id="17dc1-113">Um das DirectX-Transformations Objekt für einen Übergang anzugeben, müssen Sie die [**iamtimelineobj:: setsubobjectguid**](iamtimelineobj-setsubobjectguid.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="17dc1-113">To specify the DirectX Transform object for a transition, call the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method.</span></span>

<span data-ttu-id="17dc1-114">Um ein Übergangs Objekt zu erstellen, rufen Sie [**iamtimeline:: kreateemptynode**](iamtimeline-createemptynode.md) mit dem Wert der Zeitachsen \_ \_ Haupttyp auf \_ .</span><span class="sxs-lookup"><span data-stu-id="17dc1-114">To create a transition object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_TRANSITION.</span></span> <span data-ttu-id="17dc1-115">Sie können den zurückgegebenen [**iamtimelineobj**](iamtimelineobj.md) -Zeiger für die- `IAMTimelineTrans` Schnittstelle Abfragen.</span><span class="sxs-lookup"><span data-stu-id="17dc1-115">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the `IAMTimelineTrans` interface.</span></span>

## <a name="members"></a><span data-ttu-id="17dc1-116">Member</span><span class="sxs-lookup"><span data-stu-id="17dc1-116">Members</span></span>

<span data-ttu-id="17dc1-117">Die **iamtimelinetrans** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="17dc1-117">The **IAMTimelineTrans** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="17dc1-118">**Iamtimelinetrans** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="17dc1-118">**IAMTimelineTrans** also has these types of members:</span></span>

-   [<span data-ttu-id="17dc1-119">Methoden</span><span class="sxs-lookup"><span data-stu-id="17dc1-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="17dc1-120">Methoden</span><span class="sxs-lookup"><span data-stu-id="17dc1-120">Methods</span></span>

<span data-ttu-id="17dc1-121">Die **iamtimelinetrans** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="17dc1-121">The **IAMTimelineTrans** interface has these methods.</span></span>



| <span data-ttu-id="17dc1-122">Methode</span><span class="sxs-lookup"><span data-stu-id="17dc1-122">Method</span></span>                                                  | <span data-ttu-id="17dc1-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17dc1-123">Description</span></span>                                                                            |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="17dc1-124">**Getcutpoint**</span><span class="sxs-lookup"><span data-stu-id="17dc1-124">**GetCutPoint**</span></span>](iamtimelinetrans-getcutpoint.md)     | <span data-ttu-id="17dc1-125">Ruft den Ausschneide Punkt ab.</span><span class="sxs-lookup"><span data-stu-id="17dc1-125">Retrieves the cut point.</span></span><br/>                                                    |
| [<span data-ttu-id="17dc1-126">**GetCutPoint2**</span><span class="sxs-lookup"><span data-stu-id="17dc1-126">**GetCutPoint2**</span></span>](iamtimelinetrans-getcutpoint2.md)   | <span data-ttu-id="17dc1-127">Ruft den Ausschneide Punkt als [**ref-Zeit**](reftime.md) Wert ab.</span><span class="sxs-lookup"><span data-stu-id="17dc1-127">Retrieves the cut point, as a [**REFTIME**](reftime.md) value.</span></span><br/>             |
| [<span data-ttu-id="17dc1-128">**Getcutsonly**</span><span class="sxs-lookup"><span data-stu-id="17dc1-128">**GetCutsOnly**</span></span>](iamtimelinetrans-getcutsonly.md)     | <span data-ttu-id="17dc1-129">Bestimmt, ob der Übergang als Ausschneide gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="17dc1-129">Determines whether the transition is rendered as a cut.</span></span><br/>                     |
| [<span data-ttu-id="17dc1-130">**Ge-wapinputs**</span><span class="sxs-lookup"><span data-stu-id="17dc1-130">**GetSwapInputs**</span></span>](iamtimelinetrans-getswapinputs.md) | <span data-ttu-id="17dc1-131">Ruft einen Wert ab, der angibt, ob die Übergangs Eingaben ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="17dc1-131">Retrieves a value that indicates whether the transition inputs are swapped.</span></span><br/> |
| [<span data-ttu-id="17dc1-132">**Setcutpoint**</span><span class="sxs-lookup"><span data-stu-id="17dc1-132">**SetCutPoint**</span></span>](iamtimelinetrans-setcutpoint.md)     | <span data-ttu-id="17dc1-133">Legt den Ausschneide Punkt fest.</span><span class="sxs-lookup"><span data-stu-id="17dc1-133">Sets the cut point.</span></span><br/>                                                         |
| [<span data-ttu-id="17dc1-134">**SetCutPoint2**</span><span class="sxs-lookup"><span data-stu-id="17dc1-134">**SetCutPoint2**</span></span>](iamtimelinetrans-setcutpoint2.md)   | <span data-ttu-id="17dc1-135">Legt den Ausschneide Punkt als [**ref**](reftime.md) -Zeitwert fest.</span><span class="sxs-lookup"><span data-stu-id="17dc1-135">Sets the cut point, as a [**REFTIME**](reftime.md) value.</span></span><br/>                  |
| [<span data-ttu-id="17dc1-136">**Setcutsonly**</span><span class="sxs-lookup"><span data-stu-id="17dc1-136">**SetCutsOnly**</span></span>](iamtimelinetrans-setcutsonly.md)     | <span data-ttu-id="17dc1-137">Gibt an, ob der Übergang als Ausschneide gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="17dc1-137">Specifies whether the transition is rendered as a cut.</span></span><br/>                      |
| [<span data-ttu-id="17dc1-138">**"-Wapinputs"**</span><span class="sxs-lookup"><span data-stu-id="17dc1-138">**SetSwapInputs**</span></span>](iamtimelinetrans-setswapinputs.md) | <span data-ttu-id="17dc1-139">Gibt an, ob die Übergangs Eingaben ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="17dc1-139">Specifies whether the transition inputs are swapped.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="17dc1-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17dc1-140">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="17dc1-141">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="17dc1-141">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="17dc1-142">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="17dc1-142">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="17dc1-143">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="17dc1-143">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="17dc1-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17dc1-144">Requirements</span></span>



| <span data-ttu-id="17dc1-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17dc1-145">Requirement</span></span> | <span data-ttu-id="17dc1-146">Wert</span><span class="sxs-lookup"><span data-stu-id="17dc1-146">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17dc1-147">Header</span><span class="sxs-lookup"><span data-stu-id="17dc1-147">Header</span></span><br/>  | <dl> <span data-ttu-id="17dc1-148"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="17dc1-148"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="17dc1-149">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="17dc1-149">Library</span></span><br/> | <dl> <span data-ttu-id="17dc1-150"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="17dc1-150"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17dc1-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17dc1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17dc1-152">Arbeiten mit Effekten und Übergängen</span><span class="sxs-lookup"><span data-stu-id="17dc1-152">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
