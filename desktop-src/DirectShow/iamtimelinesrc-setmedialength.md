---
description: Die setmedialength-Methode gibt die Dauer der Quelldatei an.
ms.assetid: 0a68ad50-91d5-4cb3-95ef-35b9460ac3e4
title: 'Iamtimelinesrc:: setmedialength-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d585e9076606a77c8ecd03701ad41ab421eacd27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369258"
---
# <a name="iamtimelinesrcsetmedialength-method"></a><span data-ttu-id="0f91c-103">Iamtimelinesrc:: setmedialength-Methode</span><span class="sxs-lookup"><span data-stu-id="0f91c-103">IAMTimelineSrc::SetMediaLength method</span></span>

> [!Note]  
> <span data-ttu-id="0f91c-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="0f91c-104">\[Deprecated.</span></span> <span data-ttu-id="0f91c-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="0f91c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0f91c-106">Die- `SetMediaLength` Methode gibt die Dauer der Quelldatei an.</span><span class="sxs-lookup"><span data-stu-id="0f91c-106">The `SetMediaLength` method specifies the duration of the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f91c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f91c-107">Syntax</span></span>


```C++
HRESULT SetMediaLength(
   REFERENCE_TIME Length
);
```



## <a name="parameters"></a><span data-ttu-id="0f91c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f91c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f91c-109">*Länge*</span><span class="sxs-lookup"><span data-stu-id="0f91c-109">*Length*</span></span> 
</dt> <dd>

<span data-ttu-id="0f91c-110">Medien Länge in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="0f91c-110">Media length, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f91c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f91c-111">Return value</span></span>

<span data-ttu-id="0f91c-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="0f91c-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0f91c-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0f91c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f91c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f91c-114">Remarks</span></span>

<span data-ttu-id="0f91c-115">Sie können potenzielle Renderingfehler vermeiden, indem Sie die Medien Länge festlegen, bevor Sie die Zeit für das Medien Ende festlegen.</span><span class="sxs-lookup"><span data-stu-id="0f91c-115">You can avoid potential rendering errors by setting the media length before you set the media stop time.</span></span> <span data-ttu-id="0f91c-116">Wenn Sie die Zeit für das Beenden des Mediums festlegen, wird der von des auf die Medien Länge überprüft.</span><span class="sxs-lookup"><span data-stu-id="0f91c-116">When you set the media stop time, DES checks it against the media length.</span></span>

<span data-ttu-id="0f91c-117">Diese Methode überprüft den *length* -Parameter nicht, aber der Wert muss der tatsächlichen Dauer der Quelldatei entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0f91c-117">This method does not validate the *Length* parameter, but the value must equal the actual duration of the source file.</span></span> <span data-ttu-id="0f91c-118">Rufen Sie die Dauer der Quelldatei ab, indem [**Sie imediadet:: get \_ streamlength**](imediadet-get-streamlength.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0f91c-118">Obtain the source file duration by calling [**IMediaDet::get\_StreamLength**](imediadet-get-streamlength.md).</span></span>

> [!Note]  
> <span data-ttu-id="0f91c-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="0f91c-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0f91c-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="0f91c-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0f91c-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0f91c-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0f91c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f91c-122">Requirements</span></span>



| <span data-ttu-id="0f91c-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f91c-123">Requirement</span></span> | <span data-ttu-id="0f91c-124">Wert</span><span class="sxs-lookup"><span data-stu-id="0f91c-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f91c-125">Header</span><span class="sxs-lookup"><span data-stu-id="0f91c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0f91c-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="0f91c-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0f91c-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0f91c-127">Library</span></span><br/> | <dl> <span data-ttu-id="0f91c-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="0f91c-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f91c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f91c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f91c-130">**Iamtimelinesrc-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0f91c-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="0f91c-131">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="0f91c-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




