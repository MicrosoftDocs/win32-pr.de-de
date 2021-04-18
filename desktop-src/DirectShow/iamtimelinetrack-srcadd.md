---
description: Die srcadd-Methode fügt der Spur eine Quelle hinzu.
ms.assetid: 71c62e92-02d6-4c6f-8121-2052d6cc832c
title: 'Iamtimelinetrack:: srcadd-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.SrcAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e3d1d727fb6a99e3dea9ec2659838df1bfcd392b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357565"
---
# <a name="iamtimelinetracksrcadd-method"></a><span data-ttu-id="ac4aa-103">Iamtimelinetrack:: srcadd-Methode</span><span class="sxs-lookup"><span data-stu-id="ac4aa-103">IAMTimelineTrack::SrcAdd method</span></span>

> [!Note]  
> <span data-ttu-id="ac4aa-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="ac4aa-104">\[Deprecated.</span></span> <span data-ttu-id="ac4aa-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="ac4aa-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ac4aa-106">Die- `SrcAdd` Methode fügt der Spur eine Quelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="ac4aa-106">The `SrcAdd` method adds a source to the track.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac4aa-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac4aa-107">Syntax</span></span>


```C++
HRESULT SrcAdd(
   IAMTimelineObj *pSrc
);
```



## <a name="parameters"></a><span data-ttu-id="ac4aa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac4aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac4aa-109">*pSrc*</span><span class="sxs-lookup"><span data-stu-id="ac4aa-109">*pSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="ac4aa-110">Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des Quell Objekts.</span><span class="sxs-lookup"><span data-stu-id="ac4aa-110">Pointer to the source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac4aa-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac4aa-111">Return value</span></span>

<span data-ttu-id="ac4aa-112">Gibt \_ bei Erfolg S OK zurück.</span><span class="sxs-lookup"><span data-stu-id="ac4aa-112">Returns S\_OK if successful.</span></span> <span data-ttu-id="ac4aa-113">Gibt "E nointerface" zurück, \_ Wenn das Objekt kein Quell Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="ac4aa-113">Returns E\_NOINTERFACE if the object is not a source object.</span></span> <span data-ttu-id="ac4aa-114">Andernfalls wird ein **HRESULT** -Wert zurückgegeben, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="ac4aa-114">Otherwise, returns an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac4aa-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac4aa-115">Remarks</span></span>

<span data-ttu-id="ac4aa-116">Legen Sie die Start-und Endzeiten der Quelle vor dem Aufrufen dieser Methode fest.</span><span class="sxs-lookup"><span data-stu-id="ac4aa-116">Set the source's start and stop times before calling this method.</span></span> <span data-ttu-id="ac4aa-117">(Aufrufen von [**iamtimelineobj:: setstartstation**](iamtimelineobj-setstartstop.md).)</span><span class="sxs-lookup"><span data-stu-id="ac4aa-117">(Call [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md).)</span></span>

<span data-ttu-id="ac4aa-118">Derzeit kann des nicht gleichzeitig mehr als 75 Quellen gleichzeitig erzeugen, die mit Video Compression Manager-Codecs (VCM) komprimiert wurden.</span><span class="sxs-lookup"><span data-stu-id="ac4aa-118">Currently, DES cannot simultaneously render more than 75 sources that were compressed with Video Compression Manager (VCM) codecs.</span></span> <span data-ttu-id="ac4aa-119">Wenn das Projekt als Ganzes mehr als 75 derartige Quellen enthält, müssen Sie auch die dynamische Neuverbindung verwenden, oder des kann das Projekt nicht in der Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ac4aa-119">Also, if the project as a whole contains more than 75 such sources, you must use dynamic reconnection or DES cannot preview the project.</span></span> <span data-ttu-id="ac4aa-120">Weitere Informationen finden Sie unter " [**unenderengine:: setdynamikreconnectlevel**](irenderengine-setdynamicreconnectlevel.md)".</span><span class="sxs-lookup"><span data-stu-id="ac4aa-120">For more information, see [**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span></span>

> [!Note]  
> <span data-ttu-id="ac4aa-121">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="ac4aa-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ac4aa-122">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="ac4aa-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ac4aa-123">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ac4aa-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ac4aa-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac4aa-124">Requirements</span></span>



| <span data-ttu-id="ac4aa-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac4aa-125">Requirement</span></span> | <span data-ttu-id="ac4aa-126">Wert</span><span class="sxs-lookup"><span data-stu-id="ac4aa-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac4aa-127">Header</span><span class="sxs-lookup"><span data-stu-id="ac4aa-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ac4aa-128"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="ac4aa-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ac4aa-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ac4aa-129">Library</span></span><br/> | <dl> <span data-ttu-id="ac4aa-130"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="ac4aa-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac4aa-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac4aa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac4aa-132">**Iamtimelinetrack-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ac4aa-132">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="ac4aa-133">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="ac4aa-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




