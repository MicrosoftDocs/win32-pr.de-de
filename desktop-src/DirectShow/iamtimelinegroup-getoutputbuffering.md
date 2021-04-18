---
description: Die getoutputbuffersend-Methode ruft die Anzahl der Frames ab, die während der Vorschau vorab gerendert werden.
ms.assetid: 93cb8d18-f1b7-48f9-af41-97f010304b05
title: 'Iamtimelinegroup:: getoutputbuffereing-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8213be882ca445775137a946d9064487b25f48af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354839"
---
# <a name="iamtimelinegroupgetoutputbuffering-method"></a><span data-ttu-id="b2d85-103">Iamtimelinegroup:: getoutputbuffereing-Methode</span><span class="sxs-lookup"><span data-stu-id="b2d85-103">IAMTimelineGroup::GetOutputBuffering method</span></span>

> [!Note]  
> <span data-ttu-id="b2d85-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="b2d85-104">\[Deprecated.</span></span> <span data-ttu-id="b2d85-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="b2d85-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b2d85-106">Die- `GetOutputBuffering` Methode ruft die Anzahl der Frames ab, die während der Vorschau vorab gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="b2d85-106">The `GetOutputBuffering` method retrieves the number of frames rendered in advance during preview.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2d85-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2d85-107">Syntax</span></span>


```C++
HRESULT GetOutputBuffering(
  [out] int *pnBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="b2d85-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2d85-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2d85-109">*pnbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b2d85-109">*pnBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2d85-110">Empfängt die Anzahl der gepufferten Frames.</span><span class="sxs-lookup"><span data-stu-id="b2d85-110">Receives the number of buffered frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2d85-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2d85-111">Return value</span></span>

<span data-ttu-id="b2d85-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b2d85-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b2d85-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b2d85-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2d85-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2d85-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b2d85-115">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="b2d85-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b2d85-116">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="b2d85-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b2d85-117">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b2d85-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b2d85-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2d85-118">Requirements</span></span>



| <span data-ttu-id="b2d85-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2d85-119">Requirement</span></span> | <span data-ttu-id="b2d85-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b2d85-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2d85-121">Header</span><span class="sxs-lookup"><span data-stu-id="b2d85-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b2d85-122"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="b2d85-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b2d85-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b2d85-123">Library</span></span><br/> | <dl> <span data-ttu-id="b2d85-124"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="b2d85-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2d85-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2d85-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2d85-126">**Iamtimelinegroup-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b2d85-126">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="b2d85-127">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="b2d85-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




