---
description: Die effectgetcount-Methode ruft die Anzahl der Effekte für dieses Objekt ab.
ms.assetid: 6cf3b5b1-f38f-4ee1-8567-3c55f4f89cbb
title: 'Iamtimelineeffectable:: effectgetcount-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectGetCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 247af794c2336c80e251d1a970e1d90925d4c53c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371567"
---
# <a name="iamtimelineeffectableeffectgetcount-method"></a><span data-ttu-id="e6fec-103">Iamtimelineeffectable:: effectgetcount-Methode</span><span class="sxs-lookup"><span data-stu-id="e6fec-103">IAMTimelineEffectable::EffectGetCount method</span></span>

> [!Note]  
> <span data-ttu-id="e6fec-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="e6fec-104">\[Deprecated.</span></span> <span data-ttu-id="e6fec-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="e6fec-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e6fec-106">Die- `EffectGetCount` Methode ruft die Anzahl der Effekte für dieses-Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="e6fec-106">The `EffectGetCount` method retrieves the number of effects on this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6fec-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6fec-107">Syntax</span></span>


```C++
HRESULT EffectGetCount(
   long *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="e6fec-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6fec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6fec-109">*pCount*</span><span class="sxs-lookup"><span data-stu-id="e6fec-109">*pCount*</span></span> 
</dt> <dd>

<span data-ttu-id="e6fec-110">Empfängt die Anzahl der Effekte.</span><span class="sxs-lookup"><span data-stu-id="e6fec-110">Receives the number of effects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6fec-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6fec-111">Return value</span></span>

<span data-ttu-id="e6fec-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="e6fec-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e6fec-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e6fec-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6fec-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6fec-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e6fec-115">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="e6fec-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e6fec-116">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="e6fec-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e6fec-117">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e6fec-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e6fec-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6fec-118">Requirements</span></span>



| <span data-ttu-id="e6fec-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6fec-119">Requirement</span></span> | <span data-ttu-id="e6fec-120">Wert</span><span class="sxs-lookup"><span data-stu-id="e6fec-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6fec-121">Header</span><span class="sxs-lookup"><span data-stu-id="e6fec-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e6fec-122"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="e6fec-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e6fec-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e6fec-123">Library</span></span><br/> | <dl> <span data-ttu-id="e6fec-124"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="e6fec-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6fec-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6fec-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6fec-126">**Iamtimelineeffectable-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e6fec-126">**IAMTimelineEffectable Interface**</span></span>](iamtimelineeffectable.md)
</dt> <dt>

[<span data-ttu-id="e6fec-127">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="e6fec-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




