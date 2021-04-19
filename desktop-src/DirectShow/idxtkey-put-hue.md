---
description: Die Put \_ Hue-Methode gibt den Hue-Wert an, für den der Schlüssel bestimmt wird. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp dxtkey \_ Hue ist.
ms.assetid: 90c8c610-7ceb-479b-bb0e-d8753d0d7dac
title: Idxtkey::p ut_Hue-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Hue
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9d2b08f3e805edc8b8860495fc105f0cfdf6768f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369644"
---
# <a name="idxtkeyput_hue-method"></a><span data-ttu-id="90820-104">Idxtkey::p UT \_ Hue-Methode</span><span class="sxs-lookup"><span data-stu-id="90820-104">IDxtKey::put\_Hue method</span></span>

> [!Note]  
> <span data-ttu-id="90820-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="90820-105">\[Deprecated.</span></span> <span data-ttu-id="90820-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="90820-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="90820-107">Die- `put_Hue` Methode gibt den Farbton Wert an, auf den der Schlüssel festgelegt wird</span><span class="sxs-lookup"><span data-stu-id="90820-107">The `put_Hue` method specifies the hue value on which to key.</span></span> <span data-ttu-id="90820-108">Diese Eigenschaft gilt nur, wenn der Schlüsseltyp dxtkey \_ Hue ist.</span><span class="sxs-lookup"><span data-stu-id="90820-108">This property applies only when the key type is DXTKEY\_HUE.</span></span>

## <a name="syntax"></a><span data-ttu-id="90820-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="90820-109">Syntax</span></span>


```C++
HRESULT put_Hue(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="90820-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="90820-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90820-111">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90820-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90820-112">Der Farbton Wert, für den der Schlüssel angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="90820-112">The hue value on which to key.</span></span> <span data-ttu-id="90820-113">Der gültige Bereich liegt zwischen 0 und 360.</span><span class="sxs-lookup"><span data-stu-id="90820-113">The valid range is from 0 to 360.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90820-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90820-114">Return value</span></span>

<span data-ttu-id="90820-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="90820-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="90820-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="90820-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="90820-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90820-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="90820-118">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="90820-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="90820-119">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="90820-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="90820-120">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="90820-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="90820-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90820-121">Requirements</span></span>



| <span data-ttu-id="90820-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90820-122">Requirement</span></span> | <span data-ttu-id="90820-123">Wert</span><span class="sxs-lookup"><span data-stu-id="90820-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90820-124">Header</span><span class="sxs-lookup"><span data-stu-id="90820-124">Header</span></span><br/>  | <dl> <span data-ttu-id="90820-125"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="90820-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="90820-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="90820-126">Library</span></span><br/> | <dl> <span data-ttu-id="90820-127"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="90820-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90820-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90820-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90820-129">**Idxtkey-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="90820-129">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="90820-130">**Idxtkey::p UT- \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="90820-130">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




