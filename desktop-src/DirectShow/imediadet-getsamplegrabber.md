---
description: Die getsamplegrabber-Methode ruft einen Zeiger auf die isamplegrabber-Schnittstelle ab, die einer Anwendung das Abrufen einzelner Beispiele aus einem Mediendaten Strom ermöglicht.
ms.assetid: ecfa1909-f1ba-40ac-a0fc-8bfbeed8d148
title: 'Imediadet:: getsamplegrabber-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetSampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e83de26f1c2186293265dc39db603e0a9cf31436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368519"
---
# <a name="imediadetgetsamplegrabber-method"></a><span data-ttu-id="b5936-103">Imediadet:: getsamplegrabber-Methode</span><span class="sxs-lookup"><span data-stu-id="b5936-103">IMediaDet::GetSampleGrabber method</span></span>

> [!Note]  
> <span data-ttu-id="b5936-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="b5936-104">\[Deprecated.</span></span> <span data-ttu-id="b5936-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="b5936-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b5936-106">Die- `GetSampleGrabber` Methode ruft einen Zeiger auf die [**isamplegrabber**](isamplegrabber.md) -Schnittstelle ab, die einer Anwendung das Abrufen einzelner Beispiele aus einem Mediendaten Strom ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="b5936-106">The `GetSampleGrabber` method retrieves a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface, which enables an application to retrieve individual samples from a media stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5936-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5936-107">Syntax</span></span>


```C++
HRESULT GetSampleGrabber(
  [out] ISampleGrabber **ppVal
);
```



## <a name="parameters"></a><span data-ttu-id="b5936-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5936-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5936-109">*ppval* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b5936-109">*ppVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5936-110">Empfängt einen Zeiger auf die [**isamplegrabber**](isamplegrabber.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b5936-110">Receives a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5936-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5936-111">Return value</span></span>

<span data-ttu-id="b5936-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b5936-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b5936-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b5936-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5936-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5936-114">Remarks</span></span>

<span data-ttu-id="b5936-115">Rufen Sie [**imediadet:: enterbitmapgrabmode**](imediadet-enterbitmapgrabmode.md) auf, bevor Sie diese Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b5936-115">Call [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md) before calling this method.</span></span> <span data-ttu-id="b5936-116">Mit der [**isamplegrabber**](isamplegrabber.md) -Schnittstelle können Sie einzelne Medien Beispiele aus dem Stream abrufen.</span><span class="sxs-lookup"><span data-stu-id="b5936-116">The [**ISampleGrabber**](isamplegrabber.md) interface enables you to retrieve individual media samples from the stream.</span></span> <span data-ttu-id="b5936-117">Wenn Sie nur eine Bitmap aus einem Videoframe benötigen, können Sie stattdessen die [**imediadet:: getbitmapbits**](imediadet-getbitmapbits.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b5936-117">If you just need a bitmap from a video frame, call the [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) method instead.</span></span> <span data-ttu-id="b5936-118">Die **isamplegrabber** -Schnittstelle ist flexibler, erfordert aber mehr Arbeit durch die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b5936-118">The **ISampleGrabber** interface is more flexible, but requires more work by the application.</span></span>

<span data-ttu-id="b5936-119">Wenn diese Methode erfolgreich ausgeführt wird, hat die von ihr zurückgegebene [**isamplegrabber**](isamplegrabber.md) -Schnittstelle einen ausstehenden Verweis Zähler.</span><span class="sxs-lookup"><span data-stu-id="b5936-119">If this method succeeds, the [**ISampleGrabber**](isamplegrabber.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="b5936-120">Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="b5936-120">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="b5936-121">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="b5936-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b5936-122">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="b5936-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b5936-123">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b5936-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b5936-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5936-124">Requirements</span></span>



| <span data-ttu-id="b5936-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5936-125">Requirement</span></span> | <span data-ttu-id="b5936-126">Wert</span><span class="sxs-lookup"><span data-stu-id="b5936-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5936-127">Header</span><span class="sxs-lookup"><span data-stu-id="b5936-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b5936-128"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="b5936-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b5936-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b5936-129">Library</span></span><br/> | <dl> <span data-ttu-id="b5936-130"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="b5936-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5936-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5936-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5936-132">**Imediadet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b5936-132">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="b5936-133">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="b5936-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




