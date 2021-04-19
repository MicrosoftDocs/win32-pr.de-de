---
description: Die Put \_ masknum-Methode gibt den SMPTE-Code zum Löschen der Löschung an.
ms.assetid: d2d2382c-d920-49e7-b9b7-6897356a78de
title: Idxtjpeg::p ut_MaskNum-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_MaskNum
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0f814fab2654a5585567273301dab285c32a1019
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356439"
---
# <a name="idxtjpegput_masknum-method"></a><span data-ttu-id="9a5f0-103">Idxtjpeg::p UT \_ masknum-Methode</span><span class="sxs-lookup"><span data-stu-id="9a5f0-103">IDxtJpeg::put\_MaskNum method</span></span>

> [!Note]  
> <span data-ttu-id="9a5f0-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="9a5f0-104">\[Deprecated.</span></span> <span data-ttu-id="9a5f0-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="9a5f0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9a5f0-106">Die- `put_MaskNum` Methode gibt den SMPTE-Code zum Löschen der Löschung an.</span><span class="sxs-lookup"><span data-stu-id="9a5f0-106">The `put_MaskNum` method specifies the SMPTE wipe code of the wipe.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a5f0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a5f0-107">Syntax</span></span>


```C++
HRESULT put_MaskNum(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="9a5f0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a5f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a5f0-109">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a5f0-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a5f0-110">Gibt den SMPTE-Code zum Löschen an.</span><span class="sxs-lookup"><span data-stu-id="9a5f0-110">Specifies the SMPTE wipe code.</span></span> <span data-ttu-id="9a5f0-111">Eine Liste der unterstützten SMPTE-Wipes finden Sie unter [SMPTE](smpte-wipe-transition.md)-Zurücksetzungs Übergang.</span><span class="sxs-lookup"><span data-stu-id="9a5f0-111">For a list of supported SMPTE wipes, see [SMPTE Wipe Transition](smpte-wipe-transition.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a5f0-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a5f0-112">Return value</span></span>

<span data-ttu-id="9a5f0-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="9a5f0-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9a5f0-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9a5f0-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a5f0-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a5f0-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9a5f0-116">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="9a5f0-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9a5f0-117">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="9a5f0-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9a5f0-118">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9a5f0-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9a5f0-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a5f0-119">Requirements</span></span>



| <span data-ttu-id="9a5f0-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a5f0-120">Requirement</span></span> | <span data-ttu-id="9a5f0-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9a5f0-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a5f0-122">Header</span><span class="sxs-lookup"><span data-stu-id="9a5f0-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9a5f0-123"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="9a5f0-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9a5f0-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9a5f0-124">Library</span></span><br/> | <dl> <span data-ttu-id="9a5f0-125"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="9a5f0-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a5f0-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a5f0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a5f0-127">**Idxtjpeg-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="9a5f0-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




