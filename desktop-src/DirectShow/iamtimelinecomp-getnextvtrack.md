---
description: Die getnextvtrack-Methode ruft den nächsten virtuellen Titel nach einer angegebenen virtuellen Spur ab.
ms.assetid: c43e6b16-a3e4-4407-b48d-b04c4bb66688
title: 'Iamtimelinecomp:: getnextvtrack-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetNextVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0e5a4500c2b53703a13b509f112453e65c954f96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359758"
---
# <a name="iamtimelinecompgetnextvtrack-method"></a><span data-ttu-id="b2b04-103">Iamtimelinecomp:: getnextvtrack-Methode</span><span class="sxs-lookup"><span data-stu-id="b2b04-103">IAMTimelineComp::GetNextVTrack method</span></span>

> [!Note]  
> <span data-ttu-id="b2b04-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="b2b04-104">\[Deprecated.</span></span> <span data-ttu-id="b2b04-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="b2b04-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b2b04-106">Die- `GetNextVTrack` Methode ruft den nächsten virtuellen Titel nach einer angegebenen virtuellen Spur ab.</span><span class="sxs-lookup"><span data-stu-id="b2b04-106">The `GetNextVTrack` method retrieves the next virtual track after a specified virtual track.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2b04-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2b04-107">Syntax</span></span>


```C++
HRESULT GetNextVTrack(
        IAMTimelineObj *pVirtualTrack,
  [out] IAMTimelineObj **ppNextVirtualTrack
);
```



## <a name="parameters"></a><span data-ttu-id="b2b04-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2b04-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2b04-109">*pvirtualtrack*</span><span class="sxs-lookup"><span data-stu-id="b2b04-109">*pVirtualTrack*</span></span> 
</dt> <dd>

<span data-ttu-id="b2b04-110">Zeiger auf den vorherigen virtuellen Titel oder **null** , um den ersten virtuellen Titel in der Komposition abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b2b04-110">Pointer to the previous virtual track, or **NULL** to retrieve the first virtual track in the composition.</span></span>

</dd> <dt>

<span data-ttu-id="b2b04-111">*ppnextvirtualtrack* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b2b04-111">*ppNextVirtualTrack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2b04-112">Empfängt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle der nächsten virtuellen Spur in der Reihenfolge ihrer Priorität.</span><span class="sxs-lookup"><span data-stu-id="b2b04-112">Receives a pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the next virtual track, in order of priority.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2b04-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2b04-113">Return value</span></span>

<span data-ttu-id="b2b04-114">Gibt s \_ OK zurück, wenn die Methode einen virtuellen Track abruft, \_ andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="b2b04-114">Returns S\_OK if the method retrieves a virtual track, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2b04-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2b04-115">Remarks</span></span>

<span data-ttu-id="b2b04-116">Wenn die Methode erfolgreich ausgeführt wird, weist die zurückgegebene **iamtimelineobj** -Schnittstelle einen ausstehenden Verweis Zähler auf.</span><span class="sxs-lookup"><span data-stu-id="b2b04-116">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="b2b04-117">Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="b2b04-117">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="b2b04-118">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="b2b04-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b2b04-119">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="b2b04-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b2b04-120">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b2b04-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b2b04-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2b04-121">Requirements</span></span>



| <span data-ttu-id="b2b04-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2b04-122">Requirement</span></span> | <span data-ttu-id="b2b04-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b2b04-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2b04-124">Header</span><span class="sxs-lookup"><span data-stu-id="b2b04-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b2b04-125"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="b2b04-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b2b04-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b2b04-126">Library</span></span><br/> | <dl> <span data-ttu-id="b2b04-127"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="b2b04-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2b04-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2b04-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2b04-129">**Iamtimelinecomp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b2b04-129">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="b2b04-130">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="b2b04-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




