---
description: Die Put \_ RGB-Methode gibt die RGB-Farbe für den Schlüssel an. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp dxtkey \_ RGB ist.
ms.assetid: 7a0b794e-bea6-4061-98a0-3f70521e89a3
title: Idxtkey::p ut_RGB-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0b7d282ceb4a693d5a390b8df9b935f0e415d150
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369128"
---
# <a name="idxtkeyput_rgb-method"></a><span data-ttu-id="81dc5-104">Idxtkey::p UT \_ RGB-Methode</span><span class="sxs-lookup"><span data-stu-id="81dc5-104">IDxtKey::put\_RGB method</span></span>

> [!Note]  
> <span data-ttu-id="81dc5-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="81dc5-105">\[Deprecated.</span></span> <span data-ttu-id="81dc5-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="81dc5-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="81dc5-107">Die- `put_RGB` Methode gibt die RGB-Farbe für den Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="81dc5-107">The `put_RGB` method specifies the RGB color on which to key.</span></span> <span data-ttu-id="81dc5-108">Diese Eigenschaft gilt nur, wenn der Schlüsseltyp dxtkey \_ RGB ist.</span><span class="sxs-lookup"><span data-stu-id="81dc5-108">This property applies only when the key type is DXTKEY\_RGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="81dc5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="81dc5-109">Syntax</span></span>


```C++
HRESULT put_RGB(
  [in] DWORD newVal
);
```



## <a name="parameters"></a><span data-ttu-id="81dc5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="81dc5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81dc5-111">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81dc5-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81dc5-112">Gibt die Farbe als hexadezimale Zahl mit dem Format 0xRRGGBB an, wobei RR der rote Wert, GG der grüne Wert und BB der blaue Wert ist.</span><span class="sxs-lookup"><span data-stu-id="81dc5-112">Specifies the color as a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81dc5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81dc5-113">Return value</span></span>

<span data-ttu-id="81dc5-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="81dc5-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="81dc5-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="81dc5-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="81dc5-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81dc5-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="81dc5-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="81dc5-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="81dc5-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="81dc5-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="81dc5-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="81dc5-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="81dc5-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81dc5-120">Requirements</span></span>



| <span data-ttu-id="81dc5-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81dc5-121">Requirement</span></span> | <span data-ttu-id="81dc5-122">Wert</span><span class="sxs-lookup"><span data-stu-id="81dc5-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81dc5-123">Header</span><span class="sxs-lookup"><span data-stu-id="81dc5-123">Header</span></span><br/>  | <dl> <span data-ttu-id="81dc5-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="81dc5-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="81dc5-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="81dc5-125">Library</span></span><br/> | <dl> <span data-ttu-id="81dc5-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="81dc5-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81dc5-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81dc5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81dc5-128">**Idxtkey-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="81dc5-128">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="81dc5-129">**Idxtkey::p UT- \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="81dc5-129">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




