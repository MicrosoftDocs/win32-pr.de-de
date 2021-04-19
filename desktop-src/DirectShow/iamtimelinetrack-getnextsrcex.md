---
description: Die getnexzrcex-Methode ruft die nächste Quelle nach der angegebenen Quelle ab.
ms.assetid: cda3d079-eeb5-42a9-8854-5c90ae0e2c07
title: 'Iamtimelinetrack:: getnextrcex-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrcEx
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 274a4f6800d995e2b456dbd55adf81cf82aa84a9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369434"
---
# <a name="iamtimelinetrackgetnextsrcex-method"></a><span data-ttu-id="df9ea-103">Iamtimelinetrack:: getnexzrcex-Methode</span><span class="sxs-lookup"><span data-stu-id="df9ea-103">IAMTimelineTrack::GetNextSrcEx method</span></span>

> [!Note]  
> <span data-ttu-id="df9ea-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="df9ea-104">\[Deprecated.</span></span> <span data-ttu-id="df9ea-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="df9ea-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="df9ea-106">Die- `GetNextSrcEx` Methode ruft die nächste Quelle nach der angegebenen Quelle ab.</span><span class="sxs-lookup"><span data-stu-id="df9ea-106">The `GetNextSrcEx` method retrieves the next source after the specified source.</span></span>

## <a name="syntax"></a><span data-ttu-id="df9ea-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="df9ea-107">Syntax</span></span>


```C++
HRESULT GetNextSrcEx(
        IAMTimelineObj *pLast,
  [out] IAMTimelineObj **ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="df9ea-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="df9ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df9ea-109">*bildet*</span><span class="sxs-lookup"><span data-stu-id="df9ea-109">*pLast*</span></span> 
</dt> <dd>

<span data-ttu-id="df9ea-110">Zeiger auf das vorherige Quell Objekt oder **null** , um die erste Quelle in der Spur abzurufen.</span><span class="sxs-lookup"><span data-stu-id="df9ea-110">Pointer to the previous source object, or **NULL** to retrieve the first source in the track.</span></span>

</dd> <dt>

<span data-ttu-id="df9ea-111">*ppnext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="df9ea-111">*ppNext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df9ea-112">Empfängt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des nächsten Quell Objekts.</span><span class="sxs-lookup"><span data-stu-id="df9ea-112">Receives a pointer to the next source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df9ea-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df9ea-113">Return value</span></span>

<span data-ttu-id="df9ea-114">Gibt "s OK" zurück \_ , wenn die Methode eine Quelle abruft, \_ andernfalls "false".</span><span class="sxs-lookup"><span data-stu-id="df9ea-114">Returns S\_OK if the method retrieves a source, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="df9ea-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df9ea-115">Remarks</span></span>

<span data-ttu-id="df9ea-116">Wenn die Methode S OK zurückgibt \_ , weist die zurückgegebene **iamtimelineobj** -Schnittstelle einen ausstehenden Verweis Zähler auf.</span><span class="sxs-lookup"><span data-stu-id="df9ea-116">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="df9ea-117">Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="df9ea-117">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="df9ea-118">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="df9ea-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="df9ea-119">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="df9ea-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="df9ea-120">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="df9ea-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="df9ea-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df9ea-121">Requirements</span></span>



| <span data-ttu-id="df9ea-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df9ea-122">Requirement</span></span> | <span data-ttu-id="df9ea-123">Wert</span><span class="sxs-lookup"><span data-stu-id="df9ea-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df9ea-124">Header</span><span class="sxs-lookup"><span data-stu-id="df9ea-124">Header</span></span><br/>  | <dl> <span data-ttu-id="df9ea-125"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="df9ea-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="df9ea-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="df9ea-126">Library</span></span><br/> | <dl> <span data-ttu-id="df9ea-127"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="df9ea-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df9ea-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df9ea-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df9ea-129">**Iamtimelinetrack-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="df9ea-129">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="df9ea-130">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="df9ea-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




