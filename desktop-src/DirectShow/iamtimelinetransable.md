---
description: Die iamtimelinetransable-Schnittstelle fügt Übergänge zu einem Objekt in DirectShow-Bearbeitungs Diensten (des) hinzu.
ms.assetid: 1be9adaa-4145-447c-b307-dabb4419c86c
title: Iamtimelinetransable-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d083b768e8dcf54236945755f4b26ecf13409b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371331"
---
# <a name="iamtimelinetransable-interface"></a><span data-ttu-id="f08f3-103">Iamtimelinetransable-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f08f3-103">IAMTimelineTransable interface</span></span>

> [!Note]  
> <span data-ttu-id="f08f3-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="f08f3-104">\[Deprecated.</span></span> <span data-ttu-id="f08f3-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="f08f3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f08f3-106">Die- `IAMTimelineTransable` Schnittstelle fügt Übergänge zu einem Objekt in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="f08f3-106">The `IAMTimelineTransable` interface adds transitions to an object in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="f08f3-107">Diese Schnittstelle wird von jedem Objekt verfügbar gemacht, auf das Übergänge angewendet werden können, einschließlich der Spuren, der Komposition und der Gruppen.</span><span class="sxs-lookup"><span data-stu-id="f08f3-107">This interface is exposed by any object that can have transitions applied to it, including tracks, compositions, and groups.</span></span> <span data-ttu-id="f08f3-108">Ein Objekt, das diese Schnittstelle implementiert, kann über eine beliebige Anzahl von Übergängen verfügen, aber die Übergänge dürfen sich nicht rechtzeitig überlappen.</span><span class="sxs-lookup"><span data-stu-id="f08f3-108">An object that implements this interface can have any number of transitions, but the transitions must not overlap in time.</span></span>

> [!Note]  
> <span data-ttu-id="f08f3-109">Das Audioformat unterstützt keine Übergänge.</span><span class="sxs-lookup"><span data-stu-id="f08f3-109">Audio does not support transitions.</span></span> <span data-ttu-id="f08f3-110">Objekte in Audiogruppen können die- `IAMTimelineTransable` Schnittstelle verfügbar machen, aber die Anwendung sollte Ihnen keine Übergänge hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f08f3-110">Objects within audio groups can expose the `IAMTimelineTransable` interface, but the application should not add transitions to them.</span></span>

 

## <a name="members"></a><span data-ttu-id="f08f3-111">Member</span><span class="sxs-lookup"><span data-stu-id="f08f3-111">Members</span></span>

<span data-ttu-id="f08f3-112">Die **iamtimelinetransable** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f08f3-112">The **IAMTimelineTransable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f08f3-113">**Iamtimelinetransable** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f08f3-113">**IAMTimelineTransable** also has these types of members:</span></span>

-   [<span data-ttu-id="f08f3-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="f08f3-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f08f3-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="f08f3-115">Methods</span></span>

<span data-ttu-id="f08f3-116">Die **iamtimelinetransable** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f08f3-116">The **IAMTimelineTransable** interface has these methods.</span></span>



| <span data-ttu-id="f08f3-117">Methode</span><span class="sxs-lookup"><span data-stu-id="f08f3-117">Method</span></span>                                                          | <span data-ttu-id="f08f3-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f08f3-118">Description</span></span>                                                                                                                        |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f08f3-119">**Getnexttrans**</span><span class="sxs-lookup"><span data-stu-id="f08f3-119">**GetNextTrans**</span></span>](iamtimelinetransable-getnexttrans.md)       | <span data-ttu-id="f08f3-120">Ruft den ersten Übergang ab, der zum angegebenen Zeitpunkt oder später angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f08f3-120">Retrieves the first transition that appears at the specified time or later.</span></span><br/>                                             |
| [<span data-ttu-id="f08f3-121">**GetNextTrans2**</span><span class="sxs-lookup"><span data-stu-id="f08f3-121">**GetNextTrans2**</span></span>](iamtimelinetransable-getnexttrans2.md)     | <span data-ttu-id="f08f3-122">Ruft den ersten Übergang ab, der zum angegebenen Zeitpunkt oder später angezeigt wird, wobei die Zeit als **ref Time** -Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f08f3-122">Retrieves the first transition that appears at the specified time or later, with the time given as a **REFTIME** value.</span></span><br/> |
| [<span data-ttu-id="f08f3-123">**Gettransattime**</span><span class="sxs-lookup"><span data-stu-id="f08f3-123">**GetTransAtTime**</span></span>](iamtimelinetransable-gettransattime.md)   | <span data-ttu-id="f08f3-124">Ruft den Übergang ab, der dem angegebenen Zeitpunkt am nächsten liegt.</span><span class="sxs-lookup"><span data-stu-id="f08f3-124">Retrieves the transition nearest to the specified time.</span></span><br/>                                                                 |
| [<span data-ttu-id="f08f3-125">**GetTransAtTime2**</span><span class="sxs-lookup"><span data-stu-id="f08f3-125">**GetTransAtTime2**</span></span>](iamtimelinetransable-gettransattime2.md) | <span data-ttu-id="f08f3-126">Ruft den Übergang ab, der dem angegebenen Zeitpunkt am nächsten liegt, der als **reftime** -Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f08f3-126">Retrieves the transition nearest to the specified time, given as a **REFTIME** value.</span></span><br/>                                   |
| [<span data-ttu-id="f08f3-127">**Transadd**</span><span class="sxs-lookup"><span data-stu-id="f08f3-127">**TransAdd**</span></span>](iamtimelinetransable-transadd.md)               | <span data-ttu-id="f08f3-128">Fügt dem-Objekt einen Übergang hinzu.</span><span class="sxs-lookup"><span data-stu-id="f08f3-128">Adds a transition to the object.</span></span><br/>                                                                                        |
| [<span data-ttu-id="f08f3-129">**Transgetcount**</span><span class="sxs-lookup"><span data-stu-id="f08f3-129">**TransGetCount**</span></span>](iamtimelinetransable-transgetcount.md)     | <span data-ttu-id="f08f3-130">Ruft die Anzahl der Übergänge für dieses-Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="f08f3-130">Retrieves the number of transitions on this object.</span></span><br/>                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="f08f3-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f08f3-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f08f3-132">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="f08f3-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f08f3-133">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="f08f3-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f08f3-134">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f08f3-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f08f3-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f08f3-135">Requirements</span></span>



| <span data-ttu-id="f08f3-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f08f3-136">Requirement</span></span> | <span data-ttu-id="f08f3-137">Wert</span><span class="sxs-lookup"><span data-stu-id="f08f3-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f08f3-138">Header</span><span class="sxs-lookup"><span data-stu-id="f08f3-138">Header</span></span><br/>  | <dl> <span data-ttu-id="f08f3-139"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="f08f3-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f08f3-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f08f3-140">Library</span></span><br/> | <dl> <span data-ttu-id="f08f3-141"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="f08f3-141"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
