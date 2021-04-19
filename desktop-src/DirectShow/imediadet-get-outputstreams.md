---
description: Die get \_ outputstreams-Methode ruft die Anzahl der in der Medienquelle enthaltenen Audiodaten-und Videostreams ab. Alle anderen Streamtypen, z. b. Datenströme, werden ignoriert.
ms.assetid: 9acd0a1e-c968-4c3b-a71a-b6aa2219a8cd
title: 'Imediadet:: get_OutputStreams-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_OutputStreams
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0fa53a5ab5c315c4bedb3804ae7cefa618399590
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369206"
---
# <a name="imediadetget_outputstreams-method"></a><span data-ttu-id="13643-104">Imediadet:: get \_ outputstreams-Methode</span><span class="sxs-lookup"><span data-stu-id="13643-104">IMediaDet::get\_OutputStreams method</span></span>

> [!Note]  
> <span data-ttu-id="13643-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="13643-105">\[Deprecated.</span></span> <span data-ttu-id="13643-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="13643-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="13643-107">Die `get_OutputStreams` -Methode ruft die Anzahl der in der Medienquelle enthaltenen Audiodaten und Videostreams ab.</span><span class="sxs-lookup"><span data-stu-id="13643-107">The `get_OutputStreams` method retrieves the number of audio and video streams contained in the media source.</span></span> <span data-ttu-id="13643-108">Alle anderen Streamtypen, z. b. Datenströme, werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="13643-108">Any other stream types, such as data streams, are ignored.</span></span>

## <a name="syntax"></a><span data-ttu-id="13643-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="13643-109">Syntax</span></span>


```C++
HRESULT get_OutputStreams(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="13643-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="13643-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13643-111">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="13643-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="13643-112">Empfängt die Anzahl der Ausgabestreams.</span><span class="sxs-lookup"><span data-stu-id="13643-112">Receives the number of output streams.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13643-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13643-113">Return value</span></span>

<span data-ttu-id="13643-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="13643-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="13643-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13643-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="13643-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13643-116">Remarks</span></span>

<span data-ttu-id="13643-117">Rufen Sie vor dem Aufrufen dieser Methode [**imediadet::p UT \_ filename**](imediadet-put-filename.md) auf, um den Dateinamen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="13643-117">Before calling this method, call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) to set the file name.</span></span> <span data-ttu-id="13643-118">Wenn sich der Medien Detektor im bitmapingmodus befindet, gibt diese Methode E \_ invalidArg zurück.</span><span class="sxs-lookup"><span data-stu-id="13643-118">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="13643-119">Weitere Informationen finden Sie unter [**imediadet:: enterbitmapgrabmode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="13643-119">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="13643-120">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="13643-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="13643-121">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="13643-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="13643-122">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="13643-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="13643-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13643-123">Requirements</span></span>



| <span data-ttu-id="13643-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13643-124">Requirement</span></span> | <span data-ttu-id="13643-125">Wert</span><span class="sxs-lookup"><span data-stu-id="13643-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13643-126">Header</span><span class="sxs-lookup"><span data-stu-id="13643-126">Header</span></span><br/>  | <dl> <span data-ttu-id="13643-127"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="13643-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="13643-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="13643-128">Library</span></span><br/> | <dl> <span data-ttu-id="13643-129"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="13643-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13643-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13643-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13643-131">**Imediadet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="13643-131">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="13643-132">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="13643-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




