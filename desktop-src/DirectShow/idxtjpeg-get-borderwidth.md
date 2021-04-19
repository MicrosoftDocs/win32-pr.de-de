---
description: Die get \_ BorderWidth-Methode ruft die Breite des vollständigen Rahmens entlang der Ränder des Abbild Musters ab.
ms.assetid: 85c62524-5936-475e-a73b-7a3c926bb5f0
title: 'Idxtjpeg:: get_BorderWidth-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_BorderWidth
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 28405c08d5666c8f182e0ffdb6ed1aa7bac599d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359682"
---
# <a name="idxtjpegget_borderwidth-method"></a><span data-ttu-id="ba4c7-103">Idxtjpeg:: get \_ BorderWidth-Methode</span><span class="sxs-lookup"><span data-stu-id="ba4c7-103">IDxtJpeg::get\_BorderWidth method</span></span>

> [!Note]  
> <span data-ttu-id="ba4c7-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="ba4c7-104">\[Deprecated.</span></span> <span data-ttu-id="ba4c7-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="ba4c7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ba4c7-106">Die- `get_BorderWidth` Methode ruft die Breite des vollständigen Rahmens entlang der Ränder des-Abbild Musters ab.</span><span class="sxs-lookup"><span data-stu-id="ba4c7-106">The `get_BorderWidth` method retrieves the width of the solid border along the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba4c7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba4c7-107">Syntax</span></span>


```C++
HRESULT get_BorderWidth(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="ba4c7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba4c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba4c7-109">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="ba4c7-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ba4c7-110">Empfängt die Breite des Rahmens in Pixel.</span><span class="sxs-lookup"><span data-stu-id="ba4c7-110">Receives the width of the border, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba4c7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba4c7-111">Return value</span></span>

<span data-ttu-id="ba4c7-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="ba4c7-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ba4c7-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ba4c7-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba4c7-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba4c7-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ba4c7-115">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="ba4c7-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ba4c7-116">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="ba4c7-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ba4c7-117">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ba4c7-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ba4c7-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba4c7-118">Requirements</span></span>



| <span data-ttu-id="ba4c7-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba4c7-119">Requirement</span></span> | <span data-ttu-id="ba4c7-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ba4c7-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba4c7-121">Header</span><span class="sxs-lookup"><span data-stu-id="ba4c7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ba4c7-122"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="ba4c7-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ba4c7-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ba4c7-123">Library</span></span><br/> | <dl> <span data-ttu-id="ba4c7-124"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="ba4c7-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba4c7-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba4c7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba4c7-126">**Idxtjpeg-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ba4c7-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




