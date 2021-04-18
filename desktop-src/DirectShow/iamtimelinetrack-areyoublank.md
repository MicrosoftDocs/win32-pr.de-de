---
description: Die areyoublank-Methode bestimmt, ob der Titel leer ist (enthält keine Quell Objekte).
ms.assetid: 05d02753-6e40-4307-9445-c3cbc835f75e
title: 'Iamtimelinetrack:: areyoublank-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.AreYouBlank
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 289fac360f989504d3eb5108f8c2388ac4a06b09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364588"
---
# <a name="iamtimelinetrackareyoublank-method"></a><span data-ttu-id="f0c45-103">Iamtimelinetrack:: areyoublank-Methode</span><span class="sxs-lookup"><span data-stu-id="f0c45-103">IAMTimelineTrack::AreYouBlank method</span></span>

> [!Note]  
> <span data-ttu-id="f0c45-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="f0c45-104">\[Deprecated.</span></span> <span data-ttu-id="f0c45-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="f0c45-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f0c45-106">Die- `AreYouBlank` Methode bestimmt, ob der Titel leer ist (enthält keine Quell Objekte).</span><span class="sxs-lookup"><span data-stu-id="f0c45-106">The `AreYouBlank` method determines whether the track is blank (contains no source objects).</span></span>

## <a name="syntax"></a><span data-ttu-id="f0c45-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0c45-107">Syntax</span></span>


```C++
HRESULT AreYouBlank(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="f0c45-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0c45-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0c45-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="f0c45-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="f0c45-110">Empfängt einen booleschen Wert, der angibt, ob der Titel leer ist.</span><span class="sxs-lookup"><span data-stu-id="f0c45-110">Receives a Boolean value specifying whether the track is blank.</span></span> <span data-ttu-id="f0c45-111">Wenn der Wert **true** ist, ist der Titel leer und enthält keine Quell Objekte.</span><span class="sxs-lookup"><span data-stu-id="f0c45-111">If the value is **TRUE**, the track is blank and contains no source objects.</span></span> <span data-ttu-id="f0c45-112">Wenn der Wert **false** ist, ist der Titel nicht leer.</span><span class="sxs-lookup"><span data-stu-id="f0c45-112">If **FALSE**, the track is not blank.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0c45-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0c45-113">Return value</span></span>

<span data-ttu-id="f0c45-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f0c45-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f0c45-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f0c45-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0c45-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0c45-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f0c45-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="f0c45-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f0c45-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="f0c45-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f0c45-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f0c45-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f0c45-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0c45-120">Requirements</span></span>



| <span data-ttu-id="f0c45-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0c45-121">Requirement</span></span> | <span data-ttu-id="f0c45-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f0c45-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0c45-123">Header</span><span class="sxs-lookup"><span data-stu-id="f0c45-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f0c45-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="f0c45-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f0c45-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f0c45-125">Library</span></span><br/> | <dl> <span data-ttu-id="f0c45-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="f0c45-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0c45-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0c45-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0c45-128">**Iamtimelinetrack-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f0c45-128">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="f0c45-129">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="f0c45-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




