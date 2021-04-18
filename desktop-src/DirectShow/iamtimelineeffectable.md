---
description: Die iamtimelineeffectable-Schnittstelle stellt Methoden zum Hinzufügen von Effekten zu einem Timeline-Objekt in DirectShow-Bearbeitungs Diensten (de) und zum Bearbeiten der Auswirkungen auf ein Objekt bereit.
ms.assetid: 70f2da64-e16a-4d4d-9522-042b5fa2855c
title: Iamtimelineeffectable-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bc67483f44515c2ce18825de5b6657d51e2c3826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368537"
---
# <a name="iamtimelineeffectable-interface"></a><span data-ttu-id="40468-103">Iamtimelineeffectable-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="40468-103">IAMTimelineEffectable interface</span></span>

> [!Note]  
> <span data-ttu-id="40468-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="40468-104">\[Deprecated.</span></span> <span data-ttu-id="40468-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="40468-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="40468-106">Die `IAMTimelineEffectable` -Schnittstelle stellt Methoden zum Hinzufügen von Effekten zu einem Timeline-Objekt in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) (de) und zum Bearbeiten der Auswirkungen auf ein Objekt bereit.</span><span class="sxs-lookup"><span data-stu-id="40468-106">The `IAMTimelineEffectable` interface provides methods for adding effects to a timeline object in [DirectShow Editing Services](directshow-editing-services.md) (DES), and for manipulating the effects on an object.</span></span> <span data-ttu-id="40468-107">Diese Schnittstelle wird von allen Objekten implementiert, auf die Effekte angewendet werden können. Dies schließt Quellen, Spuren und Kompositionen ein.</span><span class="sxs-lookup"><span data-stu-id="40468-107">All objects that can have effects applied to them implement this interface; this includes sources, tracks, and compositions.</span></span>

<span data-ttu-id="40468-108">Ein Objekt, das diese Schnittstelle implementiert, kann eine beliebige Anzahl von Auswirkungen haben.</span><span class="sxs-lookup"><span data-stu-id="40468-108">An object that implements this interface can have any number of effects.</span></span> <span data-ttu-id="40468-109">Die Rendering-Engine wendet die Auswirkungen für jedes Objekt in der Reihenfolge ihrer Priorität an, beginnend mit der Prioritätsstufe 0.</span><span class="sxs-lookup"><span data-stu-id="40468-109">For each object, the render engine applies its effects in order of priority, starting with priority level 0.</span></span>

## <a name="members"></a><span data-ttu-id="40468-110">Member</span><span class="sxs-lookup"><span data-stu-id="40468-110">Members</span></span>

<span data-ttu-id="40468-111">Die **iamtimelineeffectable** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="40468-111">The **IAMTimelineEffectable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="40468-112">**Iamtimelineeffectable** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="40468-112">**IAMTimelineEffectable** also has these types of members:</span></span>

-   [<span data-ttu-id="40468-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="40468-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="40468-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="40468-114">Methods</span></span>

<span data-ttu-id="40468-115">Die **iamtimelineeffectable** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="40468-115">The **IAMTimelineEffectable** interface has these methods.</span></span>



| <span data-ttu-id="40468-116">Methode</span><span class="sxs-lookup"><span data-stu-id="40468-116">Method</span></span>                                                                     | <span data-ttu-id="40468-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40468-117">Description</span></span>                                                                   |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="40468-118">**Effectgetcount**</span><span class="sxs-lookup"><span data-stu-id="40468-118">**EffectGetCount**</span></span>](iamtimelineeffectable-effectgetcount.md)             | <span data-ttu-id="40468-119">Ruft die Anzahl der Effekte für dieses-Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="40468-119">Retrieves the number of effects on this object.</span></span><br/>                    |
| [<span data-ttu-id="40468-120">**Effectinsbefore**</span><span class="sxs-lookup"><span data-stu-id="40468-120">**EffectInsBefore**</span></span>](iamtimelineeffectable-effectinsbefore.md)           | <span data-ttu-id="40468-121">Fügt einen Effekt auf der angegebenen Prioritäts Ebene in das-Objekt ein.</span><span class="sxs-lookup"><span data-stu-id="40468-121">Inserts an effect into the object at the specified priority level.</span></span><br/> |
| [<span data-ttu-id="40468-122">**Effecungwapprioritäten**</span><span class="sxs-lookup"><span data-stu-id="40468-122">**EffectSwapPriorities**</span></span>](iamtimelineeffectable-effectswappriorities.md) | <span data-ttu-id="40468-123">Schaltet die Prioritäts Ebenen von zwei Effekten um.</span><span class="sxs-lookup"><span data-stu-id="40468-123">Switches the priority levels of two effects.</span></span><br/>                       |
| [<span data-ttu-id="40468-124">**GetEffect**</span><span class="sxs-lookup"><span data-stu-id="40468-124">**GetEffect**</span></span>](iamtimelineeffectable-geteffect.md)                       | <span data-ttu-id="40468-125">Ruft den Effekt auf der angegebenen Prioritäts Ebene ab.</span><span class="sxs-lookup"><span data-stu-id="40468-125">Retrieves the effect at the specified priority level.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="40468-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40468-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="40468-127">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="40468-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="40468-128">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="40468-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="40468-129">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="40468-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="40468-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40468-130">Requirements</span></span>



| <span data-ttu-id="40468-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40468-131">Requirement</span></span> | <span data-ttu-id="40468-132">Wert</span><span class="sxs-lookup"><span data-stu-id="40468-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40468-133">Header</span><span class="sxs-lookup"><span data-stu-id="40468-133">Header</span></span><br/>  | <dl> <span data-ttu-id="40468-134"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="40468-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="40468-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="40468-135">Library</span></span><br/> | <dl> <span data-ttu-id="40468-136"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="40468-136"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
