---
description: Die Put \_ Invert-Methode gibt an, ob der Schlüssel Vorgang invertiert wird. Diese Eigenschaft gilt für alle Schlüsseltypen außer dxtkey \_ alpha.
ms.assetid: 06acdd9f-eb3a-49bd-961d-00966df2ccb4
title: Idxtkey::p ut_Invert-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3e4b807770d0eeb985c982b61b8390695cc42327
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369485"
---
# <a name="idxtkeyput_invert-method"></a><span data-ttu-id="ba7e7-104">Idxtkey::p UT \_ Invert-Methode</span><span class="sxs-lookup"><span data-stu-id="ba7e7-104">IDxtKey::put\_Invert method</span></span>

> [!Note]  
> <span data-ttu-id="ba7e7-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="ba7e7-105">\[Deprecated.</span></span> <span data-ttu-id="ba7e7-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="ba7e7-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ba7e7-107">Die- `put_Invert` Methode gibt an, ob der Schlüssel Vorgang invertiert wird.</span><span class="sxs-lookup"><span data-stu-id="ba7e7-107">The `put_Invert` method specifies whether the key operation is inverted.</span></span> <span data-ttu-id="ba7e7-108">Diese Eigenschaft gilt für alle Schlüsseltypen außer dxtkey \_ alpha.</span><span class="sxs-lookup"><span data-stu-id="ba7e7-108">This property applies to all key types except DXTKEY\_ALPHA.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba7e7-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba7e7-109">Syntax</span></span>


```C++
HRESULT put_Invert(
  [in] BOOL newVal
);
```



## <a name="parameters"></a><span data-ttu-id="ba7e7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba7e7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba7e7-111">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba7e7-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba7e7-112">Gibt einen booleschen Wert an.</span><span class="sxs-lookup"><span data-stu-id="ba7e7-112">Specifies a Boolean value.</span></span> <span data-ttu-id="ba7e7-113">**True** gibt an, dass Pixel im überliegenden Bild in Bezug auf den Standard Vorgang invertiert werden.</span><span class="sxs-lookup"><span data-stu-id="ba7e7-113">If **TRUE**, pixels in the overlying image are inverted with respect to the default operation.</span></span> <span data-ttu-id="ba7e7-114">Wenn der Wert **false** ist, werden die Pixel im überliegenden Bild standardmäßig transparent gemacht.</span><span class="sxs-lookup"><span data-stu-id="ba7e7-114">If **FALSE**, pixels in the overlying image are made transparent in the default manner.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba7e7-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba7e7-115">Return value</span></span>

<span data-ttu-id="ba7e7-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="ba7e7-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ba7e7-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ba7e7-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba7e7-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba7e7-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ba7e7-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="ba7e7-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ba7e7-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="ba7e7-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ba7e7-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ba7e7-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ba7e7-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba7e7-122">Requirements</span></span>



| <span data-ttu-id="ba7e7-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba7e7-123">Requirement</span></span> | <span data-ttu-id="ba7e7-124">Wert</span><span class="sxs-lookup"><span data-stu-id="ba7e7-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba7e7-125">Header</span><span class="sxs-lookup"><span data-stu-id="ba7e7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ba7e7-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="ba7e7-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ba7e7-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ba7e7-127">Library</span></span><br/> | <dl> <span data-ttu-id="ba7e7-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="ba7e7-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba7e7-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba7e7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba7e7-130">**Idxtkey-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ba7e7-130">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="ba7e7-131">**Idxtkey::p UT- \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="ba7e7-131">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




