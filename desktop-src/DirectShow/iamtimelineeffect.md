---
description: Die iamtimelineeffect-Schnittstelle stellt Methoden zum Bearbeiten von Audio-und Video Effekten in DirectShow-Bearbeitungs Diensten bereit.
ms.assetid: 3cc8a5f8-3f57-4e2b-82dd-827e04c771f7
title: Iamtimelineeffect-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8b9936616b9c4487849053d36c6a63290bd16b5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372003"
---
# <a name="iamtimelineeffect-interface"></a><span data-ttu-id="4d7ff-103">Iamtimelineeffect-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4d7ff-103">IAMTimelineEffect interface</span></span>

> [!Note]  
> <span data-ttu-id="4d7ff-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="4d7ff-104">\[Deprecated.</span></span> <span data-ttu-id="4d7ff-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="4d7ff-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4d7ff-106">Die `IAMTimelineEffect` -Schnittstelle stellt Methoden zum Bearbeiten von Audio-und Video Effekten in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) bereit.</span><span class="sxs-lookup"><span data-stu-id="4d7ff-106">The `IAMTimelineEffect` interface provides methods for manipulating audio and video effects in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="4d7ff-107">Einem Zeitachsen Objekt, das die [**iamtimelineeffectable**](iamtimelineeffectable.md) -Schnittstelle verfügbar macht, kann ein Effekt hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4d7ff-107">An effect can be added to any timeline object that exposes the [**IAMTimelineEffectable**](iamtimelineeffectable.md) interface.</span></span> <span data-ttu-id="4d7ff-108">Um Eigenschaften für einen Effekt festzulegen, verwenden Sie die [**ipropertysetter**](ipropertysetter.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4d7ff-108">To set properties on an effect, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

<span data-ttu-id="4d7ff-109">Das des des-Effekts-Objekts ist tatsächlich ein Wrapper für eines von zwei anderen Objekten:</span><span class="sxs-lookup"><span data-stu-id="4d7ff-109">The DES effect object is actually a wrapper for one of two other objects:</span></span>

-   <span data-ttu-id="4d7ff-110">Für Audioeffekte ist jeder DirectShow-audiowirkungs Filter.</span><span class="sxs-lookup"><span data-stu-id="4d7ff-110">For audio effects, any DirectShow audio effect filter.</span></span>
-   <span data-ttu-id="4d7ff-111">Für Video Effekte und 1-Input-DirectX-Transformations Objekt.</span><span class="sxs-lookup"><span data-stu-id="4d7ff-111">For video effects, and 1-input DirectX Transform object.</span></span>

<span data-ttu-id="4d7ff-112">Microsoft unterstützt die Entwicklung von DirectX-Transformations Objekten von Drittanbietern nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="4d7ff-112">Microsoft no longer supports the development of third-party DirectX Transform objects.</span></span>

<span data-ttu-id="4d7ff-113">Um das Filter-oder DirectX-Transformations Objekt für einen Effekt anzugeben, müssen Sie die [**iamtimelineobj:: setsubobjectguid**](iamtimelineobj-setsubobjectguid.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4d7ff-113">To specify the filter or DirectX Transform object for an effect, call the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method.</span></span>

<span data-ttu-id="4d7ff-114">Um ein Effect-Objekt zu erstellen, rufen Sie [**iamtimeline:: kreateemptynode**](iamtimeline-createemptynode.md) mit dem Wert der Wert Zeitachse des \_ Haupt \_ Typs auf \_ .</span><span class="sxs-lookup"><span data-stu-id="4d7ff-114">To create an effect object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_EFFECT.</span></span> <span data-ttu-id="4d7ff-115">Sie können den zurückgegebenen [**iamtimelineobj**](iamtimelineobj.md) -Zeiger für die- `IAMTimelineEffect` Schnittstelle Abfragen.</span><span class="sxs-lookup"><span data-stu-id="4d7ff-115">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the `IAMTimelineEffect` interface.</span></span>

## <a name="members"></a><span data-ttu-id="4d7ff-116">Member</span><span class="sxs-lookup"><span data-stu-id="4d7ff-116">Members</span></span>

<span data-ttu-id="4d7ff-117">Die **iamtimelineeffect** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4d7ff-117">The **IAMTimelineEffect** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4d7ff-118">**Iamtimelineeffect** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4d7ff-118">**IAMTimelineEffect** also has these types of members:</span></span>

-   [<span data-ttu-id="4d7ff-119">Methoden</span><span class="sxs-lookup"><span data-stu-id="4d7ff-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4d7ff-120">Methoden</span><span class="sxs-lookup"><span data-stu-id="4d7ff-120">Methods</span></span>

<span data-ttu-id="4d7ff-121">Die **iamtimelineeffect** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="4d7ff-121">The **IAMTimelineEffect** interface has these methods.</span></span>



| <span data-ttu-id="4d7ff-122">Methode</span><span class="sxs-lookup"><span data-stu-id="4d7ff-122">Method</span></span>                                                           | <span data-ttu-id="4d7ff-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4d7ff-123">Description</span></span>                                       |
|:-----------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="4d7ff-124">**Effectgetpriority**</span><span class="sxs-lookup"><span data-stu-id="4d7ff-124">**EffectGetPriority**</span></span>](iamtimelineeffect-effectgetpriority.md) | <span data-ttu-id="4d7ff-125">Ruft die Prioritäts Ebene des Effekts ab.</span><span class="sxs-lookup"><span data-stu-id="4d7ff-125">Retrieves the effect's priority level.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4d7ff-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d7ff-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4d7ff-127">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="4d7ff-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4d7ff-128">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="4d7ff-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4d7ff-129">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4d7ff-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4d7ff-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d7ff-130">Requirements</span></span>



| <span data-ttu-id="4d7ff-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d7ff-131">Requirement</span></span> | <span data-ttu-id="4d7ff-132">Wert</span><span class="sxs-lookup"><span data-stu-id="4d7ff-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d7ff-133">Header</span><span class="sxs-lookup"><span data-stu-id="4d7ff-133">Header</span></span><br/>  | <dl> <span data-ttu-id="4d7ff-134"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="4d7ff-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4d7ff-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4d7ff-135">Library</span></span><br/> | <dl> <span data-ttu-id="4d7ff-136"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="4d7ff-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d7ff-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d7ff-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d7ff-138">Arbeiten mit Effekten und Übergängen</span><span class="sxs-lookup"><span data-stu-id="4d7ff-138">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
