---
description: Die getsourcescount-Methode ruft die Anzahl der Quellen in der Spur ab.
ms.assetid: eb7f249f-355f-454d-9fe6-c3271fd13fc7
title: 'Iamtimelinetrack:: getsourcescount-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSourcesCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0e143b16e5cdc1e193760c0b97846be07eb72c0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354059"
---
# <a name="iamtimelinetrackgetsourcescount-method"></a><span data-ttu-id="82470-103">Iamtimelinetrack:: getsourcescount-Methode</span><span class="sxs-lookup"><span data-stu-id="82470-103">IAMTimelineTrack::GetSourcesCount method</span></span>

> [!Note]  
> <span data-ttu-id="82470-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="82470-104">\[Deprecated.</span></span> <span data-ttu-id="82470-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="82470-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="82470-106">Die- `GetSourcesCount` Methode ruft die Anzahl der Quellen in der Spur ab.</span><span class="sxs-lookup"><span data-stu-id="82470-106">The `GetSourcesCount` method retrieves the number of sources in the track.</span></span>

## <a name="syntax"></a><span data-ttu-id="82470-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="82470-107">Syntax</span></span>


```C++
HRESULT GetSourcesCount(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="82470-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="82470-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82470-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="82470-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="82470-110">Empfängt die Anzahl der Quellen in der Verfolgung.</span><span class="sxs-lookup"><span data-stu-id="82470-110">Receives the number of sources in the track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82470-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="82470-111">Return value</span></span>

<span data-ttu-id="82470-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="82470-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="82470-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="82470-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="82470-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82470-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="82470-115">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="82470-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="82470-116">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="82470-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="82470-117">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="82470-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="82470-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82470-118">Requirements</span></span>



| <span data-ttu-id="82470-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82470-119">Requirement</span></span> | <span data-ttu-id="82470-120">Wert</span><span class="sxs-lookup"><span data-stu-id="82470-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82470-121">Header</span><span class="sxs-lookup"><span data-stu-id="82470-121">Header</span></span><br/>  | <dl> <span data-ttu-id="82470-122"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="82470-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="82470-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="82470-123">Library</span></span><br/> | <dl> <span data-ttu-id="82470-124"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="82470-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82470-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82470-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82470-126">**Iamtimelinetrack-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="82470-126">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="82470-127">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="82470-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




