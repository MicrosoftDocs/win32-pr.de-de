---
description: Die Put \_ Alpha-Methode gibt den Alpha-Wert für das gesamte Bild an.
ms.assetid: ba02a9ae-b722-4771-89c6-e76369d39ed7
title: Idxtalphasetter::p ut_Alpha-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 54bd69993a0dc0880f351f3e9ba7a79c9d926194
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372133"
---
# <a name="idxtalphasetterput_alpha-method"></a><span data-ttu-id="fb2b1-103">Idxtalphasetter::p UT \_ Alpha-Methode</span><span class="sxs-lookup"><span data-stu-id="fb2b1-103">IDxtAlphaSetter::put\_Alpha method</span></span>

> [!Note]  
> <span data-ttu-id="fb2b1-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="fb2b1-104">\[Deprecated.</span></span> <span data-ttu-id="fb2b1-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="fb2b1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fb2b1-106">Die- `put_Alpha` Methode gibt den Alpha-Wert für das gesamte Bild an.</span><span class="sxs-lookup"><span data-stu-id="fb2b1-106">The `put_Alpha` method specifies the alpha value for the entire image.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb2b1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb2b1-107">Syntax</span></span>


```C++
HRESULT put_Alpha(
  [in] long Alpha
);
```



## <a name="parameters"></a><span data-ttu-id="fb2b1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb2b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb2b1-109">*Alpha* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb2b1-109">*Alpha* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb2b1-110">Der Alphawert.</span><span class="sxs-lookup"><span data-stu-id="fb2b1-110">The alpha value.</span></span> <span data-ttu-id="fb2b1-111">Dieser Wert wird auf das gesamte Zielbild angewendet.</span><span class="sxs-lookup"><span data-stu-id="fb2b1-111">This value will be applied to the entire target image.</span></span> <span data-ttu-id="fb2b1-112">Legen Sie zum Deaktivieren dieser Eigenschaft einen negativen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="fb2b1-112">To disable this property, set a negative value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb2b1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb2b1-113">Return value</span></span>

<span data-ttu-id="fb2b1-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="fb2b1-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fb2b1-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fb2b1-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb2b1-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb2b1-116">Remarks</span></span>

<span data-ttu-id="fb2b1-117">Wenn Sie diese Eigenschaft auf einen nicht negativen Wert festlegen, müssen Sie auch die Eigenschaft Alpha-Rampe deaktivieren, indem Sie **Put \_ alpharamp** mit einem negativen Wert aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fb2b1-117">If you set this property to a non-negative value, you must also disable the alpha ramp property, by calling **put\_AlphaRamp** with a negative value.</span></span> <span data-ttu-id="fb2b1-118">Andernfalls wird der Effekt nicht korrekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="fb2b1-118">Otherwise the effect will not render correctly.</span></span>

> [!Note]  
> <span data-ttu-id="fb2b1-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="fb2b1-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fb2b1-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="fb2b1-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fb2b1-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fb2b1-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fb2b1-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb2b1-122">Requirements</span></span>



| <span data-ttu-id="fb2b1-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb2b1-123">Requirement</span></span> | <span data-ttu-id="fb2b1-124">Wert</span><span class="sxs-lookup"><span data-stu-id="fb2b1-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb2b1-125">Header</span><span class="sxs-lookup"><span data-stu-id="fb2b1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="fb2b1-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="fb2b1-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fb2b1-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fb2b1-127">Library</span></span><br/> | <dl> <span data-ttu-id="fb2b1-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="fb2b1-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb2b1-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb2b1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb2b1-130">**Idxtalphasetter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="fb2b1-130">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> <dt>

[<span data-ttu-id="fb2b1-131">**Idxtalphasetter::p UT \_ alpharamp**</span><span class="sxs-lookup"><span data-stu-id="fb2b1-131">**IDxtAlphaSetter::put\_AlphaRamp**</span></span>](idxtalphasetter-put-alpharamp.md)
</dt> </dl>

 

 




