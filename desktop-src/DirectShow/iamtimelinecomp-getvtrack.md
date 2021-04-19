---
description: Die getvtrack-Methode ruft den virtuellen Track mit der angegebenen Priorität ab.
ms.assetid: e866064b-a511-4f0c-8cb1-62e4f1c42347
title: 'Iamtimelinecomp:: getvtrack-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 06c205f700cbdb98fdc5f45bdd2ca7727e2456f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356047"
---
# <a name="iamtimelinecompgetvtrack-method"></a><span data-ttu-id="dabcf-103">Iamtimelinecomp:: getvtrack-Methode</span><span class="sxs-lookup"><span data-stu-id="dabcf-103">IAMTimelineComp::GetVTrack method</span></span>

> [!Note]  
> <span data-ttu-id="dabcf-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="dabcf-104">\[Deprecated.</span></span> <span data-ttu-id="dabcf-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="dabcf-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="dabcf-106">Die- `GetVTrack` Methode ruft den virtuellen Track mit der angegebenen Priorität ab.</span><span class="sxs-lookup"><span data-stu-id="dabcf-106">The `GetVTrack` method retrieves the virtual track at the specified priority.</span></span>

## <a name="syntax"></a><span data-ttu-id="dabcf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dabcf-107">Syntax</span></span>


```C++
HRESULT GetVTrack(
  [out] IAMTimelineObj **ppVirtualTrack,
        long           Which
);
```



## <a name="parameters"></a><span data-ttu-id="dabcf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dabcf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dabcf-109">*ppvirtualtrack* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dabcf-109">*ppVirtualTrack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dabcf-110">Empfängt die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des virtuellen Titels.</span><span class="sxs-lookup"><span data-stu-id="dabcf-110">Receives the virtual track's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="dabcf-111">*,*</span><span class="sxs-lookup"><span data-stu-id="dabcf-111">*Which*</span></span> 
</dt> <dd>

<span data-ttu-id="dabcf-112">Priorität des abzurufenden virtuellen Titels.</span><span class="sxs-lookup"><span data-stu-id="dabcf-112">Priority of the virtual track to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dabcf-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dabcf-113">Return value</span></span>

<span data-ttu-id="dabcf-114">Gibt einen der folgenden **HRESULT** -Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="dabcf-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="dabcf-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="dabcf-115">Return code</span></span>                                                                                  | <span data-ttu-id="dabcf-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dabcf-116">Description</span></span>                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="dabcf-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dabcf-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="dabcf-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="dabcf-118">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="dabcf-119"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="dabcf-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="dabcf-120">Keine virtuelle Spur mit der angegebenen Priorität.</span><span class="sxs-lookup"><span data-stu-id="dabcf-120">No virtual track with the specified priority.</span></span><br/> |
| <dl> <span data-ttu-id="dabcf-121"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="dabcf-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="dabcf-122">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="dabcf-122">**NULL** pointer argument.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="dabcf-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dabcf-123">Remarks</span></span>

<span data-ttu-id="dabcf-124">Wenn die Methode erfolgreich ausgeführt wird, weist die zurückgegebene **iamtimelineobj** -Schnittstelle einen ausstehenden Verweis Zähler auf.</span><span class="sxs-lookup"><span data-stu-id="dabcf-124">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="dabcf-125">Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="dabcf-125">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="dabcf-126">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="dabcf-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="dabcf-127">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="dabcf-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="dabcf-128">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dabcf-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dabcf-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dabcf-129">Requirements</span></span>



| <span data-ttu-id="dabcf-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dabcf-130">Requirement</span></span> | <span data-ttu-id="dabcf-131">Wert</span><span class="sxs-lookup"><span data-stu-id="dabcf-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dabcf-132">Header</span><span class="sxs-lookup"><span data-stu-id="dabcf-132">Header</span></span><br/>  | <dl> <span data-ttu-id="dabcf-133"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="dabcf-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="dabcf-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dabcf-134">Library</span></span><br/> | <dl> <span data-ttu-id="dabcf-135"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="dabcf-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dabcf-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dabcf-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dabcf-137">**Iamtimelinecomp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="dabcf-137">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="dabcf-138">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="dabcf-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




