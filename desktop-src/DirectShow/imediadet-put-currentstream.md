---
description: Die Put \_ currentstream-Methode gibt die Datenstrom Nummer an, die vom Medien Detektor verwendet werden soll.
ms.assetid: 01fb7ccf-9b45-434c-b574-f3027d85ea8a
title: Imediadet::p ut_CurrentStream-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_CurrentStream
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 864848f646e4a9e06ca12e2bfec742c1741d77e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372370"
---
# <a name="imediadetput_currentstream-method"></a><span data-ttu-id="6fc9d-103">Imediadet::p UT \_ currentstream-Methode</span><span class="sxs-lookup"><span data-stu-id="6fc9d-103">IMediaDet::put\_CurrentStream method</span></span>

> [!Note]  
> <span data-ttu-id="6fc9d-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="6fc9d-104">\[Deprecated.</span></span> <span data-ttu-id="6fc9d-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="6fc9d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6fc9d-106">Die- `put_CurrentStream` Methode gibt die Datenstrom Nummer an, die vom Medien Detektor verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6fc9d-106">The `put_CurrentStream` method specifies the stream number for the media detector to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fc9d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fc9d-107">Syntax</span></span>


```C++
HRESULT put_CurrentStream(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="6fc9d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6fc9d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fc9d-109">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6fc9d-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fc9d-110">Die streamnummer.</span><span class="sxs-lookup"><span data-stu-id="6fc9d-110">Stream number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fc9d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6fc9d-111">Return value</span></span>

<span data-ttu-id="6fc9d-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="6fc9d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6fc9d-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6fc9d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fc9d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6fc9d-114">Remarks</span></span>

<span data-ttu-id="6fc9d-115">Rufen Sie vor dem Aufrufen dieser Methode [**imediadet::p UT \_ filename**](imediadet-put-filename.md) auf, um den Dateinamen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6fc9d-115">Before calling this method, call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) to set the file name.</span></span> <span data-ttu-id="6fc9d-116">Wenden Sie [**imediadet:: get \_ outputstreams**](imediadet-get-outputstreams.md) an, um die Anzahl der in der Quelldatei enthaltenen Streams zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="6fc9d-116">Call [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) to determine the number of streams contained in the source file.</span></span>

<span data-ttu-id="6fc9d-117">Wenn sich der Medien Detektor im bitmapingmodus befindet, gibt diese Methode E \_ invalidArg zurück.</span><span class="sxs-lookup"><span data-stu-id="6fc9d-117">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="6fc9d-118">Weitere Informationen finden Sie unter [**imediadet:: enterbitmapgrabmode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="6fc9d-118">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="6fc9d-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="6fc9d-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6fc9d-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="6fc9d-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6fc9d-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6fc9d-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6fc9d-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fc9d-122">Requirements</span></span>



| <span data-ttu-id="6fc9d-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6fc9d-123">Requirement</span></span> | <span data-ttu-id="6fc9d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="6fc9d-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fc9d-125">Header</span><span class="sxs-lookup"><span data-stu-id="6fc9d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="6fc9d-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="6fc9d-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6fc9d-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6fc9d-127">Library</span></span><br/> | <dl> <span data-ttu-id="6fc9d-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="6fc9d-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fc9d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fc9d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fc9d-130">**Imediadet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="6fc9d-130">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="6fc9d-131">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="6fc9d-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




