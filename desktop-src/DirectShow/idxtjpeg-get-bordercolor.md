---
description: Die get \_ BorderColor-Methode ruft die Farbe des Rahmens um die Ränder des Abbild Musters ab.
ms.assetid: 9d36cc49-c174-4b93-a030-ca8d2890c624
title: 'Idxtjpeg:: get_BorderColor-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_BorderColor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7f37c37865caf76839733ada376ec637747977ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361643"
---
# <a name="idxtjpegget_bordercolor-method"></a><span data-ttu-id="6d0d7-103">Idxtjpeg:: get \_ BorderColor-Methode</span><span class="sxs-lookup"><span data-stu-id="6d0d7-103">IDxtJpeg::get\_BorderColor method</span></span>

> [!Note]  
> <span data-ttu-id="6d0d7-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="6d0d7-104">\[Deprecated.</span></span> <span data-ttu-id="6d0d7-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="6d0d7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6d0d7-106">Die- `get_BorderColor` Methode ruft die Farbe des Rahmens um die Ränder des-Abbild Musters ab.</span><span class="sxs-lookup"><span data-stu-id="6d0d7-106">The `get_BorderColor` method retrieves the color of the border around the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d0d7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d0d7-107">Syntax</span></span>


```C++
HRESULT get_BorderColor(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="6d0d7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d0d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d0d7-109">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6d0d7-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6d0d7-110">Empfängt die Farbe.</span><span class="sxs-lookup"><span data-stu-id="6d0d7-110">Receives the color.</span></span> <span data-ttu-id="6d0d7-111">Der zurückgegebene Wert ist eine hexadezimale Zahl im Format 0xRRGGBB, wobei RR der rote Wert, GG der grüne Wert und BB der blaue Wert ist.</span><span class="sxs-lookup"><span data-stu-id="6d0d7-111">The returned value is a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d0d7-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6d0d7-112">Return value</span></span>

<span data-ttu-id="6d0d7-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="6d0d7-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6d0d7-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6d0d7-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d0d7-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d0d7-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6d0d7-116">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="6d0d7-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6d0d7-117">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="6d0d7-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6d0d7-118">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6d0d7-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6d0d7-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d0d7-119">Requirements</span></span>



| <span data-ttu-id="6d0d7-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d0d7-120">Requirement</span></span> | <span data-ttu-id="6d0d7-121">Wert</span><span class="sxs-lookup"><span data-stu-id="6d0d7-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d0d7-122">Header</span><span class="sxs-lookup"><span data-stu-id="6d0d7-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6d0d7-123"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="6d0d7-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6d0d7-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6d0d7-124">Library</span></span><br/> | <dl> <span data-ttu-id="6d0d7-125"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="6d0d7-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d0d7-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d0d7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d0d7-127">**Idxtjpeg-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="6d0d7-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




