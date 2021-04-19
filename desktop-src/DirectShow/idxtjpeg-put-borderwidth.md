---
description: Die Put \_ BorderWidth-Methode gibt die Breite des vollständigen Rahmens entlang der Kanten des Abbild Musters an.
ms.assetid: a618926a-efa4-47a2-9ce9-ae298ed41083
title: Idxtjpeg::p ut_BorderWidth-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_BorderWidth
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: df7435b8a516b818b6d7c86e907ba75cce86f6c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361454"
---
# <a name="idxtjpegput_borderwidth-method"></a><span data-ttu-id="fa5c5-103">Idxtjpeg::p UT \_ BorderWidth-Methode</span><span class="sxs-lookup"><span data-stu-id="fa5c5-103">IDxtJpeg::put\_BorderWidth method</span></span>

> [!Note]  
> <span data-ttu-id="fa5c5-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="fa5c5-104">\[Deprecated.</span></span> <span data-ttu-id="fa5c5-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="fa5c5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fa5c5-106">Die- `put_BorderWidth` Methode gibt die Breite des vollständigen Rahmens entlang der Kanten des-Abbild Musters an.</span><span class="sxs-lookup"><span data-stu-id="fa5c5-106">The `put_BorderWidth` method specifies the width of the solid border along the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa5c5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa5c5-107">Syntax</span></span>


```C++
HRESULT put_BorderWidth(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="fa5c5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa5c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa5c5-109">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa5c5-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa5c5-110">Die Breite des Rahmens in Pixel.</span><span class="sxs-lookup"><span data-stu-id="fa5c5-110">The width of the border, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa5c5-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fa5c5-111">Return value</span></span>

<span data-ttu-id="fa5c5-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="fa5c5-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fa5c5-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fa5c5-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa5c5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa5c5-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fa5c5-115">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="fa5c5-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fa5c5-116">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="fa5c5-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fa5c5-117">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fa5c5-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fa5c5-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa5c5-118">Requirements</span></span>



| <span data-ttu-id="fa5c5-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa5c5-119">Requirement</span></span> | <span data-ttu-id="fa5c5-120">Wert</span><span class="sxs-lookup"><span data-stu-id="fa5c5-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa5c5-121">Header</span><span class="sxs-lookup"><span data-stu-id="fa5c5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fa5c5-122"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="fa5c5-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fa5c5-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fa5c5-123">Library</span></span><br/> | <dl> <span data-ttu-id="fa5c5-124"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="fa5c5-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa5c5-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa5c5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa5c5-126">**Idxtjpeg-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="fa5c5-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




