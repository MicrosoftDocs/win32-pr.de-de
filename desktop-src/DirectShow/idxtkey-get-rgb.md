---
description: Die get \_ RGB-Methode ruft die RGB-Farbe ab, nach der der Schlüssel abgerufen werden soll. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp dxtkey \_ RGB ist.
ms.assetid: 7b1b22ff-457a-48c8-9221-ca38601874a9
title: 'Idxtkey:: get_RGB-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ef521b28c232f8247ef38858931ae56be6bf2d25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368373"
---
# <a name="idxtkeyget_rgb-method"></a><span data-ttu-id="5aa73-104">Idxtkey:: get \_ RGB-Methode</span><span class="sxs-lookup"><span data-stu-id="5aa73-104">IDxtKey::get\_RGB method</span></span>

> [!Note]  
> <span data-ttu-id="5aa73-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="5aa73-105">\[Deprecated.</span></span> <span data-ttu-id="5aa73-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="5aa73-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5aa73-107">Die- `get_RGB` Methode ruft die RGB-Farbe ab, für die der Schlüssel abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5aa73-107">The `get_RGB` method retrieves the RGB color on which to key.</span></span> <span data-ttu-id="5aa73-108">Diese Eigenschaft gilt nur, wenn der Schlüsseltyp dxtkey \_ RGB ist.</span><span class="sxs-lookup"><span data-stu-id="5aa73-108">This property applies only when the key type is DXTKEY\_RGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aa73-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5aa73-109">Syntax</span></span>


```C++
HRESULT get_RGB(
  [out, retval] DWORD *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="5aa73-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5aa73-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aa73-111">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5aa73-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5aa73-112">Empfängt die Farbe.</span><span class="sxs-lookup"><span data-stu-id="5aa73-112">Receives the color.</span></span> <span data-ttu-id="5aa73-113">Der zurückgegebene Wert ist eine hexadezimale Zahl im Format 0xRRGGBB, wobei RR der rote Wert, GG der grüne Wert und BB der blaue Wert ist.</span><span class="sxs-lookup"><span data-stu-id="5aa73-113">The returned value is a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aa73-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5aa73-114">Return value</span></span>

<span data-ttu-id="5aa73-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="5aa73-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5aa73-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5aa73-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5aa73-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5aa73-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5aa73-118">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="5aa73-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5aa73-119">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="5aa73-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5aa73-120">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5aa73-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5aa73-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5aa73-121">Requirements</span></span>



| <span data-ttu-id="5aa73-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5aa73-122">Requirement</span></span> | <span data-ttu-id="5aa73-123">Wert</span><span class="sxs-lookup"><span data-stu-id="5aa73-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa73-124">Header</span><span class="sxs-lookup"><span data-stu-id="5aa73-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5aa73-125"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="5aa73-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5aa73-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5aa73-126">Library</span></span><br/> | <dl> <span data-ttu-id="5aa73-127"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="5aa73-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5aa73-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5aa73-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aa73-129">**Idxtkey-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5aa73-129">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="5aa73-130">**Idxtkey:: get \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="5aa73-130">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




