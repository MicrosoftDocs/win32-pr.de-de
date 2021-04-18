---
description: Die gezwapinputs-Methode ruft einen Wert ab, der angibt, ob die Übergangs Eingaben ausgetauscht werden.
ms.assetid: 84cb5c3d-7c3a-4c35-aac7-97d812d99a38
title: 'Iamtimelinetrans:: gezwapinputs-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a2acdff1007bd26773ce495d024676632eee1767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364538"
---
# <a name="iamtimelinetransgetswapinputs-method"></a><span data-ttu-id="38e54-103">Iamtimelinetrans:: gezwapinputs-Methode</span><span class="sxs-lookup"><span data-stu-id="38e54-103">IAMTimelineTrans::GetSwapInputs method</span></span>

> [!Note]  
> <span data-ttu-id="38e54-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="38e54-104">\[Deprecated.</span></span> <span data-ttu-id="38e54-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="38e54-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="38e54-106">Die- `GetSwapInputs` Methode ruft einen Wert ab, der angibt, ob die Übergangs Eingaben ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="38e54-106">The `GetSwapInputs` method retrieves a value that indicates whether the transition inputs are swapped.</span></span>

<span data-ttu-id="38e54-107">Standardmäßig wird ein Übergang von der zusammengesetzten aller Ebenen mit niedrigerer Priorität zu der Ebene, auf der sich der Übergang befindet, durchläuft.</span><span class="sxs-lookup"><span data-stu-id="38e54-107">By default, a transition goes from the composite of all lower-priority layers to the layer where the transition resides.</span></span> <span data-ttu-id="38e54-108">Sie können diesen Fortschritt umkehren, sodass der Übergang von der Ebene, in der er sich wieder auf die Zusammensetzung der Ebenen mit niedrigerer Priorität befindet, erfolgt.</span><span class="sxs-lookup"><span data-stu-id="38e54-108">You can reverse this progression, so the transition goes from the layer where it resides back to the composite of lower-priority layers.</span></span>

## <a name="syntax"></a><span data-ttu-id="38e54-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="38e54-109">Syntax</span></span>


```C++
HRESULT GetSwapInputs(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="38e54-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="38e54-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38e54-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="38e54-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="38e54-112">Empfängt einen booleschen Wert.</span><span class="sxs-lookup"><span data-stu-id="38e54-112">Receives a Boolean value.</span></span> <span data-ttu-id="38e54-113">Wenn der Wert **false** ist, wird der Übergang von der zusammengesetzten aller Ebenen mit niedrigerer Priorität zur Übergangs Schicht geleitet.</span><span class="sxs-lookup"><span data-stu-id="38e54-113">If the value is **FALSE**, the transition goes from the composite of all lower-priority layers to the transition layer.</span></span> <span data-ttu-id="38e54-114">Wenn der Wert **true** ist, wird der Übergang in die entgegengesetzte Richtung geleitet.</span><span class="sxs-lookup"><span data-stu-id="38e54-114">If the value is **TRUE**, the transition goes in the opposite direction.</span></span> <span data-ttu-id="38e54-115">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="38e54-115">The default value is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38e54-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38e54-116">Return value</span></span>

<span data-ttu-id="38e54-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="38e54-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="38e54-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="38e54-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="38e54-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38e54-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="38e54-120">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="38e54-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="38e54-121">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="38e54-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="38e54-122">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="38e54-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="38e54-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38e54-123">Requirements</span></span>



| <span data-ttu-id="38e54-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="38e54-124">Requirement</span></span> | <span data-ttu-id="38e54-125">Wert</span><span class="sxs-lookup"><span data-stu-id="38e54-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38e54-126">Header</span><span class="sxs-lookup"><span data-stu-id="38e54-126">Header</span></span><br/>  | <dl> <span data-ttu-id="38e54-127"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="38e54-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="38e54-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="38e54-128">Library</span></span><br/> | <dl> <span data-ttu-id="38e54-129"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="38e54-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38e54-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38e54-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38e54-131">**Iamtimelinetrans-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="38e54-131">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="38e54-132">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="38e54-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




