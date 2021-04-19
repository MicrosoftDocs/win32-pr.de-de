---
description: Mit der Put- \_ Methode für die Leuchtkraft wird der Wert für die Leuchtkraft festgelegt. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp dxtkey- \_ Beleuchtung ist.
ms.assetid: 3e255423-1724-49fe-b1a1-49bc1d5fa6ae
title: Idxtkey::p ut_Luminance-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Luminance
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 100f2352b88e9aae2f31ce969302f4bee0905f27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369156"
---
# <a name="idxtkeyput_luminance-method"></a><span data-ttu-id="1ed6c-104">Idxtkey::p UT-Methode "Leuchtkraft" \_</span><span class="sxs-lookup"><span data-stu-id="1ed6c-104">IDxtKey::put\_Luminance method</span></span>

> [!Note]  
> <span data-ttu-id="1ed6c-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="1ed6c-105">\[Deprecated.</span></span> <span data-ttu-id="1ed6c-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="1ed6c-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1ed6c-107">Die- `put_Luminance` Methode gibt den Wert der Leuchtkraft an, für den der Schlüssel bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="1ed6c-107">The `put_Luminance` method specifies the luminance value on which to key.</span></span> <span data-ttu-id="1ed6c-108">Diese Eigenschaft gilt nur, wenn der Schlüsseltyp dxtkey- \_ Beleuchtung ist.</span><span class="sxs-lookup"><span data-stu-id="1ed6c-108">This property applies only when the key type is DXTKEY\_LUMINANCE.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ed6c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ed6c-109">Syntax</span></span>


```C++
HRESULT put_Luminance(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="1ed6c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ed6c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ed6c-111">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ed6c-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ed6c-112">Der Wert für die Leuchtkraft, auf den der Schlüssel fest.</span><span class="sxs-lookup"><span data-stu-id="1ed6c-112">The luminance value on which to key.</span></span> <span data-ttu-id="1ed6c-113">Der gültige Bereich liegt zwischen 0 und 100.</span><span class="sxs-lookup"><span data-stu-id="1ed6c-113">The valid range is from 0 to 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ed6c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ed6c-114">Return value</span></span>

<span data-ttu-id="1ed6c-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="1ed6c-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1ed6c-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1ed6c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ed6c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ed6c-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1ed6c-118">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="1ed6c-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1ed6c-119">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="1ed6c-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1ed6c-120">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1ed6c-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1ed6c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ed6c-121">Requirements</span></span>



| <span data-ttu-id="1ed6c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ed6c-122">Requirement</span></span> | <span data-ttu-id="1ed6c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="1ed6c-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ed6c-124">Header</span><span class="sxs-lookup"><span data-stu-id="1ed6c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1ed6c-125"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="1ed6c-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1ed6c-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1ed6c-126">Library</span></span><br/> | <dl> <span data-ttu-id="1ed6c-127"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="1ed6c-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ed6c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ed6c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ed6c-129">**Idxtkey-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="1ed6c-129">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="1ed6c-130">**Idxtkey::p UT- \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="1ed6c-130">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




