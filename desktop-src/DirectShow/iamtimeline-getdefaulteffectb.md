---
description: 'Die getdefaulteffectb-Methode ruft den Standardeffekt ab. Diese Methode entspricht iamtimeline:: getdefaulteffect, empfängt aber einen BSTR-Wert anstelle einer GUID.'
ms.assetid: 62c37a61-9875-4140-8552-83d82c060715
title: 'Iamtimeline:: getdefaulteffectb-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultEffectB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 01b82c42c34e3146bbad5560d516aef55225a3d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365570"
---
# <a name="iamtimelinegetdefaulteffectb-method"></a><span data-ttu-id="f82f1-104">Iamtimeline:: getdefaulteffectb-Methode</span><span class="sxs-lookup"><span data-stu-id="f82f1-104">IAMTimeline::GetDefaultEffectB method</span></span>

> [!Note]  
> <span data-ttu-id="f82f1-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="f82f1-105">\[Deprecated.</span></span> <span data-ttu-id="f82f1-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="f82f1-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f82f1-107">Die- `GetDefaultEffectB` Methode ruft den Standardeffekt ab.</span><span class="sxs-lookup"><span data-stu-id="f82f1-107">The `GetDefaultEffectB` method retrieves the default effect.</span></span> <span data-ttu-id="f82f1-108">Diese Methode entspricht [**iamtimeline:: getdefaulteffect**](iamtimeline-getdefaulteffect.md), empfängt aber einen **BSTR** -Wert anstelle einer GUID.</span><span class="sxs-lookup"><span data-stu-id="f82f1-108">This method is equivalent to [**IAMTimeline::GetDefaultEffect**](iamtimeline-getdefaulteffect.md), but receives a **BSTR** value rather than a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="f82f1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f82f1-109">Syntax</span></span>


```C++
HRESULT GetDefaultEffectB(
  [out, retval] BSTR *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="f82f1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f82f1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f82f1-111">*pguid* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f82f1-111">*pGuid* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f82f1-112">Empfängt einen **BSTR** -Wert, der die GUID des Standard Effekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="f82f1-112">Receives a **BSTR** value representing the GUID of the default effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f82f1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f82f1-113">Return value</span></span>

<span data-ttu-id="f82f1-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f82f1-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f82f1-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f82f1-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f82f1-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f82f1-116">Remarks</span></span>

<span data-ttu-id="f82f1-117">Die-Methode ordnet Speicher für die Zeichenfolge zu.</span><span class="sxs-lookup"><span data-stu-id="f82f1-117">The method allocates memory for the string.</span></span> <span data-ttu-id="f82f1-118">Die Anwendung muss **SysFreeString** aufzurufen, um den Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="f82f1-118">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="f82f1-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="f82f1-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f82f1-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="f82f1-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f82f1-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f82f1-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f82f1-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f82f1-122">Requirements</span></span>



| <span data-ttu-id="f82f1-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f82f1-123">Requirement</span></span> | <span data-ttu-id="f82f1-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f82f1-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f82f1-125">Header</span><span class="sxs-lookup"><span data-stu-id="f82f1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f82f1-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="f82f1-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f82f1-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f82f1-127">Library</span></span><br/> | <dl> <span data-ttu-id="f82f1-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="f82f1-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f82f1-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f82f1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f82f1-130">**Iamtimeline-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f82f1-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="f82f1-131">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="f82f1-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




