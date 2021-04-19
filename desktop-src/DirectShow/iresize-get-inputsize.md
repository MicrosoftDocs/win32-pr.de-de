---
description: Die get \_ inputsize-Methode gibt die aktuelle Eingabe Größe des Filter Werts der Größenänderung zurück.
ms.assetid: 7066a044-52ea-4851-83f2-f1fb323c2251
title: 'Iresize:: get_InputSize-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_InputSize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fab61edf6dc4469f06437483172161fbbe77e76d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370810"
---
# <a name="iresizeget_inputsize-method"></a><span data-ttu-id="2cf7f-103">Iresize:: get \_ inputsize-Methode</span><span class="sxs-lookup"><span data-stu-id="2cf7f-103">IResize::get\_InputSize method</span></span>

> [!Note]  
> <span data-ttu-id="2cf7f-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="2cf7f-104">\[Deprecated.</span></span> <span data-ttu-id="2cf7f-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="2cf7f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2cf7f-106">Die `get_InputSize` -Methode gibt die aktuelle Eingabe Größe des Filter der Größenänderung zurück.</span><span class="sxs-lookup"><span data-stu-id="2cf7f-106">The `get_InputSize` method returns the resizer filter's current input size.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cf7f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cf7f-107">Syntax</span></span>


```C++
HRESULT get_InputSize(
  [out] int *piHeight,
  [out] int *piWidth
);
```



## <a name="parameters"></a><span data-ttu-id="2cf7f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cf7f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cf7f-109">*piheight* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2cf7f-109">*piHeight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2cf7f-110">Empfängt die Höhe des Videos in Pixel.</span><span class="sxs-lookup"><span data-stu-id="2cf7f-110">Receives the video height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="2cf7f-111">*piwidth* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2cf7f-111">*piWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2cf7f-112">Empfängt die Video Breite in Pixel.</span><span class="sxs-lookup"><span data-stu-id="2cf7f-112">Receives the video width, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cf7f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2cf7f-113">Return value</span></span>

<span data-ttu-id="2cf7f-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="2cf7f-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2cf7f-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2cf7f-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cf7f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2cf7f-116">Remarks</span></span>

<span data-ttu-id="2cf7f-117">Wenn die Eingabe-PIN des Filters nicht verbunden ist, wird ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2cf7f-117">If the filter's input pin is not connected, return an error code.</span></span> <span data-ttu-id="2cf7f-118">Andernfalls wird die Breite und Höhe des Videos zurückgegeben, wie durch den Medientyp der Eingabe-PIN angegeben.</span><span class="sxs-lookup"><span data-stu-id="2cf7f-118">Otherwise, return the width and height of the video, as specified by the input pin's media type.</span></span>

> [!Note]  
> <span data-ttu-id="2cf7f-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="2cf7f-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2cf7f-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="2cf7f-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2cf7f-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2cf7f-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2cf7f-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2cf7f-122">Requirements</span></span>



| <span data-ttu-id="2cf7f-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2cf7f-123">Requirement</span></span> | <span data-ttu-id="2cf7f-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2cf7f-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cf7f-125">Version</span><span class="sxs-lookup"><span data-stu-id="2cf7f-125">Version</span></span><br/> | <span data-ttu-id="2cf7f-126">DirectX 9,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="2cf7f-126">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="2cf7f-127">Header</span><span class="sxs-lookup"><span data-stu-id="2cf7f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="2cf7f-128"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="2cf7f-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2cf7f-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2cf7f-129">Library</span></span><br/> | <dl> <span data-ttu-id="2cf7f-130"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="2cf7f-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cf7f-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2cf7f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cf7f-132">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="2cf7f-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="2cf7f-133">**Iresize-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="2cf7f-133">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




