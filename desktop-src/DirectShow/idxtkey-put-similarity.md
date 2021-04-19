---
description: Die Put- \_ Ähnlichkeits Methode gibt den Bereich der Farbdaten an, der transparent wird. Bei höheren Werten ist eine größere Anzahl ähnlicher Farben transparent. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp dxtkey \_ RGB oder dxtkey \_ nicht rot ist.
ms.assetid: f033b226-f36d-4288-b17e-e173546caee1
title: Idxtkey::p ut_Similarity-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f2aec52b987a1d4f146f2261d44a289ddac59f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366759"
---
# <a name="idxtkeyput_similarity-method"></a><span data-ttu-id="4f655-105">Idxtkey::p UT- \_ Ähnlichkeits Methode</span><span class="sxs-lookup"><span data-stu-id="4f655-105">IDxtKey::put\_Similarity method</span></span>

> [!Note]  
> <span data-ttu-id="4f655-106">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="4f655-106">\[Deprecated.</span></span> <span data-ttu-id="4f655-107">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="4f655-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4f655-108">Die- `put_Similarity` Methode gibt den Bereich der Farbdaten an, der transparent wird.</span><span class="sxs-lookup"><span data-stu-id="4f655-108">The `put_Similarity` method specifies the range of color data that becomes transparent.</span></span> <span data-ttu-id="4f655-109">Bei höheren Werten ist eine größere Anzahl ähnlicher Farben transparent.</span><span class="sxs-lookup"><span data-stu-id="4f655-109">At higher values, a wider range of similar colors is transparent.</span></span> <span data-ttu-id="4f655-110">Diese Eigenschaft gilt nur, wenn der Schlüsseltyp dxtkey \_ RGB oder dxtkey \_ nicht rot ist.</span><span class="sxs-lookup"><span data-stu-id="4f655-110">This property applies only when the key type is DXTKEY\_RGB or DXTKEY\_NONRED.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f655-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f655-111">Syntax</span></span>


```C++
HRESULT put_Similarity(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="4f655-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f655-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f655-113">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f655-113">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f655-114">Gibt den Ähnlichkeits Wert an.</span><span class="sxs-lookup"><span data-stu-id="4f655-114">Specifies the similarity value.</span></span> <span data-ttu-id="4f655-115">Der gültige Bereich liegt zwischen 0 und 100.</span><span class="sxs-lookup"><span data-stu-id="4f655-115">The valid range is from 0 to 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f655-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f655-116">Return value</span></span>

<span data-ttu-id="4f655-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="4f655-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4f655-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4f655-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f655-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f655-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4f655-120">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="4f655-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4f655-121">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="4f655-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4f655-122">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4f655-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4f655-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f655-123">Requirements</span></span>



| <span data-ttu-id="4f655-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f655-124">Requirement</span></span> | <span data-ttu-id="4f655-125">Wert</span><span class="sxs-lookup"><span data-stu-id="4f655-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f655-126">Header</span><span class="sxs-lookup"><span data-stu-id="4f655-126">Header</span></span><br/>  | <dl> <span data-ttu-id="4f655-127"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="4f655-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4f655-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4f655-128">Library</span></span><br/> | <dl> <span data-ttu-id="4f655-129"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="4f655-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f655-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f655-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f655-131">**Idxtkey-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="4f655-131">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="4f655-132">**Idxtkey::p UT- \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="4f655-132">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




