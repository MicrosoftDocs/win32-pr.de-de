---
description: Die get \_ alpharamp-Methode ruft die Eigenschaft für die Alpha-Eigenschaft ab. Die Alpha-Rampe ist der Prozentsatz, um den die Alpha Werte im ursprünglichen Bild angepasst werden. Wenn die Alpha-Rampe z. b. 0,5 ist, werden die Alpha-Werte im Bild um 50% reduziert.
ms.assetid: e142a562-2e78-4418-94e9-b41320d4af57
title: 'Idxtalphasetter:: get_AlphaRamp-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 335c227b0ac35ccd730d8ce7014b9a5c7ebc3213
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351270"
---
# <a name="idxtalphasetterget_alpharamp-method"></a><span data-ttu-id="b1a29-105">Idxtalphasetter:: get \_ alpharamp-Methode</span><span class="sxs-lookup"><span data-stu-id="b1a29-105">IDxtAlphaSetter::get\_AlphaRamp method</span></span>

> [!Note]  
> <span data-ttu-id="b1a29-106">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="b1a29-106">\[Deprecated.</span></span> <span data-ttu-id="b1a29-107">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="b1a29-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b1a29-108">Die- `get_AlphaRamp` Methode ruft die Eigenschaft für die Alpha-Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="b1a29-108">The `get_AlphaRamp` method retrieves the alpha ramp property.</span></span> <span data-ttu-id="b1a29-109">Die Alpha-Rampe ist der Prozentsatz, um den die Alpha Werte im ursprünglichen Bild angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="b1a29-109">The alpha ramp is the percentage by which the alpha values in the original image are adjusted.</span></span> <span data-ttu-id="b1a29-110">Wenn die Alpha-Rampe z. b. 0,5 ist, werden die Alpha-Werte im Bild um 50% reduziert.</span><span class="sxs-lookup"><span data-stu-id="b1a29-110">For example, if the alpha ramp is 0.5, the alpha values in the image are reduced 50%.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1a29-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1a29-111">Syntax</span></span>


```C++
HRESULT get_AlphaRamp(
  [out, retval] double *pAlpha
);
```



## <a name="parameters"></a><span data-ttu-id="b1a29-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1a29-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1a29-113">*Palpha* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b1a29-113">*pAlpha* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b1a29-114">Empfängt die Alpha-Rampe.</span><span class="sxs-lookup"><span data-stu-id="b1a29-114">Receives the alpha ramp.</span></span> <span data-ttu-id="b1a29-115">Ein negativer Wert gibt an, dass keine Alpha-Rampe festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b1a29-115">A negative value indicates that no alpha ramp is set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1a29-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b1a29-116">Return value</span></span>

<span data-ttu-id="b1a29-117">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b1a29-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b1a29-118">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="b1a29-118">Possible values include the following.</span></span>



| <span data-ttu-id="b1a29-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b1a29-119">Return code</span></span>                                                                               | <span data-ttu-id="b1a29-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1a29-120">Description</span></span>                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="b1a29-121"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="b1a29-121"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="b1a29-122">**Null** -Zeigerargument</span><span class="sxs-lookup"><span data-stu-id="b1a29-122">**NULL** pointer argument</span></span><br/> |
| <dl> <span data-ttu-id="b1a29-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b1a29-123"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="b1a29-124">Erfolg</span><span class="sxs-lookup"><span data-stu-id="b1a29-124">Success</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="b1a29-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1a29-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b1a29-126">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="b1a29-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b1a29-127">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="b1a29-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b1a29-128">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b1a29-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b1a29-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1a29-129">Requirements</span></span>



| <span data-ttu-id="b1a29-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1a29-130">Requirement</span></span> | <span data-ttu-id="b1a29-131">Wert</span><span class="sxs-lookup"><span data-stu-id="b1a29-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1a29-132">Header</span><span class="sxs-lookup"><span data-stu-id="b1a29-132">Header</span></span><br/>  | <dl> <span data-ttu-id="b1a29-133"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="b1a29-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b1a29-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b1a29-134">Library</span></span><br/> | <dl> <span data-ttu-id="b1a29-135"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="b1a29-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1a29-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1a29-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1a29-137">**Idxtalphasetter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b1a29-137">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> </dl>

 

 




