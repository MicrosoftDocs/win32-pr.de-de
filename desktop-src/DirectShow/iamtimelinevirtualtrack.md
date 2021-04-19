---
description: Die iamtimelinevirtualtrack-Schnittstelle stellt Methoden für das Arbeiten mit virtuellen Spuren in DirectShow-Bearbeitungs Diensten (de) bereit. Komposition und Spuren unterstützen diese Schnittstelle.
ms.assetid: 69d1d2ea-d33f-406d-a9ca-ddfb890bed34
title: Iamtimelinevirtualtrack-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineVirtualTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2295f1c336270818242f0d992a369e6a66f9237a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370662"
---
# <a name="iamtimelinevirtualtrack-interface"></a><span data-ttu-id="605ae-104">Iamtimelinevirtualtrack-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="605ae-104">IAMTimelineVirtualTrack interface</span></span>

> [!Note]  
> <span data-ttu-id="605ae-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="605ae-105">\[Deprecated.</span></span> <span data-ttu-id="605ae-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="605ae-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="605ae-107">Die- `IAMTimelineVirtualTrack` Schnittstelle stellt Methoden zum Arbeiten mit virtuellen Spuren in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) bereit.</span><span class="sxs-lookup"><span data-stu-id="605ae-107">The `IAMTimelineVirtualTrack` interface provides methods for working with virtual tracks in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="605ae-108">Komposition und Spuren unterstützen diese Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="605ae-108">Compositions and tracks support this interface.</span></span>

## <a name="members"></a><span data-ttu-id="605ae-109">Member</span><span class="sxs-lookup"><span data-stu-id="605ae-109">Members</span></span>

<span data-ttu-id="605ae-110">Die **iamtimelinevirtualtrack** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="605ae-110">The **IAMTimelineVirtualTrack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="605ae-111">**Iamtimelinevirtualtrack** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="605ae-111">**IAMTimelineVirtualTrack** also has these types of members:</span></span>

-   [<span data-ttu-id="605ae-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="605ae-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="605ae-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="605ae-113">Methods</span></span>

<span data-ttu-id="605ae-114">Die **iamtimelinevirtualtrack** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="605ae-114">The **IAMTimelineVirtualTrack** interface has these methods.</span></span>



| <span data-ttu-id="605ae-115">Methode</span><span class="sxs-lookup"><span data-stu-id="605ae-115">Method</span></span>                                                               | <span data-ttu-id="605ae-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="605ae-116">Description</span></span>                                       |
|:---------------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="605ae-117">**Settrackdirty**</span><span class="sxs-lookup"><span data-stu-id="605ae-117">**SetTrackDirty**</span></span>](iamtimelinevirtualtrack-settrackdirty.md)       | <span data-ttu-id="605ae-118">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="605ae-118">Not supported.</span></span><br/>                         |
| [<span data-ttu-id="605ae-119">**Trackgetpriority**</span><span class="sxs-lookup"><span data-stu-id="605ae-119">**TrackGetPriority**</span></span>](iamtimelinevirtualtrack-trackgetpriority.md) | <span data-ttu-id="605ae-120">Ruft die Prioritäts Ebene des-Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="605ae-120">Retrieves the object's priority level.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="605ae-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="605ae-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="605ae-122">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="605ae-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="605ae-123">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="605ae-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="605ae-124">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="605ae-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="605ae-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="605ae-125">Requirements</span></span>



| <span data-ttu-id="605ae-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="605ae-126">Requirement</span></span> | <span data-ttu-id="605ae-127">Wert</span><span class="sxs-lookup"><span data-stu-id="605ae-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="605ae-128">Header</span><span class="sxs-lookup"><span data-stu-id="605ae-128">Header</span></span><br/>  | <dl> <span data-ttu-id="605ae-129"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="605ae-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="605ae-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="605ae-130">Library</span></span><br/> | <dl> <span data-ttu-id="605ae-131"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="605ae-131"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
