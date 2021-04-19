---
description: Die get \_ streamlength-Methode ruft die Dauer des aktuellen Streams ab.
ms.assetid: b3c13abe-cd56-4960-9862-bda47a0e87ed
title: 'Imediadet:: get_StreamLength-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 61fe92fcb845a626fafc8ebb49126a35cf633aea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370274"
---
# <a name="imediadetget_streamlength-method"></a><span data-ttu-id="feade-103">Imediadet:: get \_ streamlength-Methode</span><span class="sxs-lookup"><span data-stu-id="feade-103">IMediaDet::get\_StreamLength method</span></span>

> [!Note]  
> <span data-ttu-id="feade-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="feade-104">\[Deprecated.</span></span> <span data-ttu-id="feade-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="feade-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="feade-106">Die- `get_StreamLength` Methode ruft die Dauer des aktuellen Streams ab.</span><span class="sxs-lookup"><span data-stu-id="feade-106">The `get_StreamLength` method retrieves the duration of the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="feade-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="feade-107">Syntax</span></span>


```C++
HRESULT get_StreamLength(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="feade-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="feade-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="feade-109">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="feade-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="feade-110">Empfängt die Dauer des Streams in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="feade-110">Receives the duration of the stream, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="feade-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="feade-111">Return value</span></span>

<span data-ttu-id="feade-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="feade-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="feade-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="feade-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="feade-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="feade-114">Remarks</span></span>

<span data-ttu-id="feade-115">Bevor Sie diese Methode aufrufen, legen Sie den Dateinamen und den Stream durch Aufrufen von [**imediadet::p UT \_ filename**](imediadet-put-filename.md) und [**imediadet::p UT \_ currentstream**](imediadet-put-currentstream.md)fest.</span><span class="sxs-lookup"><span data-stu-id="feade-115">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="feade-116">Wenn sich der Medien Detektor im bitmapingmodus befindet, gibt diese Methode E \_ invalidArg zurück.</span><span class="sxs-lookup"><span data-stu-id="feade-116">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="feade-117">Weitere Informationen finden Sie unter [**imediadet:: enterbitmapgrabmode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="feade-117">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="feade-118">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="feade-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="feade-119">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="feade-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="feade-120">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="feade-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="feade-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="feade-121">Requirements</span></span>



| <span data-ttu-id="feade-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="feade-122">Requirement</span></span> | <span data-ttu-id="feade-123">Wert</span><span class="sxs-lookup"><span data-stu-id="feade-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="feade-124">Header</span><span class="sxs-lookup"><span data-stu-id="feade-124">Header</span></span><br/>  | <dl> <span data-ttu-id="feade-125"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="feade-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="feade-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="feade-126">Library</span></span><br/> | <dl> <span data-ttu-id="feade-127"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="feade-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="feade-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="feade-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feade-129">**Imediadet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="feade-129">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="feade-130">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="feade-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




