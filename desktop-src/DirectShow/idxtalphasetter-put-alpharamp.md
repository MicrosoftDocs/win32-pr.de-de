---
description: Die Put \_ alpharamp-Methode gibt die Eigenschaft für die Alpha-Eigenschaft an. Die Alpha-Rampe ist der Prozentsatz, um den die Alpha Werte im ursprünglichen Bild angepasst werden. Wenn die Alpha-Rampe z. b. 0,5 ist, werden die Alpha-Werte im Bild um 50% reduziert.
ms.assetid: 19ea5828-54fc-43a1-be7c-f6c12cf84648
title: Idxtalphasetter::p ut_AlphaRamp-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc6c0eb4d5286081de9abe0c7c6d58092d111573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371791"
---
# <a name="idxtalphasetterput_alpharamp-method"></a><span data-ttu-id="5570a-105">Idxtalphasetter::p UT \_ alpharamp-Methode</span><span class="sxs-lookup"><span data-stu-id="5570a-105">IDxtAlphaSetter::put\_AlphaRamp method</span></span>

> [!Note]  
> <span data-ttu-id="5570a-106">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="5570a-106">\[Deprecated.</span></span> <span data-ttu-id="5570a-107">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="5570a-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5570a-108">Die- `put_AlphaRamp` Methode gibt die Eigenschaft der Alpha-Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="5570a-108">The `put_AlphaRamp` method specifies the alpha ramp property.</span></span> <span data-ttu-id="5570a-109">Die Alpha-Rampe ist der Prozentsatz, um den die Alpha Werte im ursprünglichen Bild angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="5570a-109">The alpha ramp is the percentage by which the alpha values in the original image are adjusted.</span></span> <span data-ttu-id="5570a-110">Wenn die Alpha-Rampe z. b. 0,5 ist, werden die Alpha-Werte im Bild um 50% reduziert.</span><span class="sxs-lookup"><span data-stu-id="5570a-110">For example, if the alpha ramp is 0.5, the alpha values in the image are reduced 50%.</span></span>

## <a name="syntax"></a><span data-ttu-id="5570a-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="5570a-111">Syntax</span></span>


```C++
HRESULT put_AlphaRamp(
  [in] double Alpha
);
```



## <a name="parameters"></a><span data-ttu-id="5570a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5570a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5570a-113">*Alpha* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5570a-113">*Alpha* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5570a-114">Die Alpha-Rampe als Prozentsatz.</span><span class="sxs-lookup"><span data-stu-id="5570a-114">The alpha ramp as a percentage.</span></span> <span data-ttu-id="5570a-115">1,0 ist beispielsweise 100%.</span><span class="sxs-lookup"><span data-stu-id="5570a-115">For example, 1.0 is 100%.</span></span> <span data-ttu-id="5570a-116">Legen Sie zum Deaktivieren dieser Eigenschaft einen negativen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="5570a-116">To disable this property, set a negative value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5570a-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5570a-117">Return value</span></span>

<span data-ttu-id="5570a-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="5570a-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5570a-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5570a-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5570a-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5570a-120">Remarks</span></span>

<span data-ttu-id="5570a-121">Wenn Sie diese Eigenschaft auf einen nicht negativen Wert festlegen, müssen Sie auch die Alpha-Eigenschaft deaktivieren, indem Sie **Put \_ Alpha** mit einem negativen Wert aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5570a-121">If you set this property to a non-negative value, you must also disable the alpha property, by calling **put\_Alpha** with a negative value.</span></span> <span data-ttu-id="5570a-122">Andernfalls wird der Effekt nicht korrekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5570a-122">Otherwise the effect will not render correctly.</span></span>

> [!Note]  
> <span data-ttu-id="5570a-123">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="5570a-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5570a-124">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="5570a-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5570a-125">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5570a-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5570a-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5570a-126">Requirements</span></span>



| <span data-ttu-id="5570a-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5570a-127">Requirement</span></span> | <span data-ttu-id="5570a-128">Wert</span><span class="sxs-lookup"><span data-stu-id="5570a-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5570a-129">Header</span><span class="sxs-lookup"><span data-stu-id="5570a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="5570a-130"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="5570a-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5570a-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5570a-131">Library</span></span><br/> | <dl> <span data-ttu-id="5570a-132"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="5570a-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5570a-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5570a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5570a-134">**Idxtalphasetter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5570a-134">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> <dt>

[<span data-ttu-id="5570a-135">**Idxtalphasetter::p UT \_ Alpha**</span><span class="sxs-lookup"><span data-stu-id="5570a-135">**IDxtAlphaSetter::put\_Alpha**</span></span>](idxtalphasetter-put-alpha.md)
</dt> </dl>

 

 




