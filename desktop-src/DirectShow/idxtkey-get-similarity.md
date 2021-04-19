---
description: Die \_ Methode Get Ähnlichkeits Methode ruft den Bereich der Farbdaten ab, der transparent wird. Bei höheren Werten ist eine größere Anzahl ähnlicher Farben transparent. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp dxtkey \_ RGB oder dxtkey \_ nicht rot ist.
ms.assetid: ddf82759-fe71-4e06-b73c-c450b7cce43d
title: 'Idxtkey:: get_Similarity-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e53898a1f9c5175fdf7a42ba6de68e3173f02afe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366975"
---
# <a name="idxtkeyget_similarity-method"></a><span data-ttu-id="45e0e-105">Idxtkey:: get- \_ Ähnlichkeits Methode</span><span class="sxs-lookup"><span data-stu-id="45e0e-105">IDxtKey::get\_Similarity method</span></span>

> [!Note]  
> <span data-ttu-id="45e0e-106">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="45e0e-106">\[Deprecated.</span></span> <span data-ttu-id="45e0e-107">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="45e0e-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="45e0e-108">Die- `get_Similarity` Methode ruft den Bereich der Farbdaten ab, der transparent wird.</span><span class="sxs-lookup"><span data-stu-id="45e0e-108">The `get_Similarity` method retrieves the range of color data that becomes transparent.</span></span> <span data-ttu-id="45e0e-109">Bei höheren Werten ist eine größere Anzahl ähnlicher Farben transparent.</span><span class="sxs-lookup"><span data-stu-id="45e0e-109">At higher values, a wider range of similar colors is transparent.</span></span> <span data-ttu-id="45e0e-110">Diese Eigenschaft gilt nur, wenn der Schlüsseltyp dxtkey \_ RGB oder dxtkey \_ nicht rot ist.</span><span class="sxs-lookup"><span data-stu-id="45e0e-110">This property applies only when the key type is DXTKEY\_RGB or DXTKEY\_NONRED.</span></span>

## <a name="syntax"></a><span data-ttu-id="45e0e-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="45e0e-111">Syntax</span></span>


```C++
HRESULT get_Similarity(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="45e0e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="45e0e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45e0e-113">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="45e0e-113">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="45e0e-114">Empfängt den Ähnlichkeits Wert.</span><span class="sxs-lookup"><span data-stu-id="45e0e-114">Receives the similarity value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45e0e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="45e0e-115">Return value</span></span>

<span data-ttu-id="45e0e-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="45e0e-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="45e0e-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="45e0e-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="45e0e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45e0e-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="45e0e-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="45e0e-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="45e0e-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="45e0e-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="45e0e-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="45e0e-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="45e0e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45e0e-122">Requirements</span></span>



| <span data-ttu-id="45e0e-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45e0e-123">Requirement</span></span> | <span data-ttu-id="45e0e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="45e0e-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45e0e-125">Header</span><span class="sxs-lookup"><span data-stu-id="45e0e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="45e0e-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="45e0e-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="45e0e-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="45e0e-127">Library</span></span><br/> | <dl> <span data-ttu-id="45e0e-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="45e0e-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45e0e-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45e0e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45e0e-130">**Idxtkey-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="45e0e-130">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="45e0e-131">**Idxtkey:: get \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="45e0e-131">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




