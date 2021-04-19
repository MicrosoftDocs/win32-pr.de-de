---
description: Die isnormalrate-Methode gibt an, ob der Clip mit der normalen Wiedergabe Rate wiedergegeben wird. Das heißt, die Wiedergabe Rate der ursprünglichen Datei.
ms.assetid: 4a8fe415-f9eb-450d-9a75-e528577050d9
title: 'Iamtimelinesrc:: isnormalrate-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.IsNormalRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e368efcf29d836cc23fa60ed34dae1a172978f77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373982"
---
# <a name="iamtimelinesrcisnormalrate-method"></a><span data-ttu-id="21b26-103">Iamtimelinesrc:: isnormalrate-Methode</span><span class="sxs-lookup"><span data-stu-id="21b26-103">IAMTimelineSrc::IsNormalRate method</span></span>

> [!Note]  
> <span data-ttu-id="21b26-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="21b26-104">\[Deprecated.</span></span> <span data-ttu-id="21b26-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="21b26-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="21b26-106">Die- `IsNormalRate` Methode gibt an, ob der Clip mit der normalen Wiedergabe Rate abgespielt wird, d. h. die Wiedergabe Rate der ursprünglichen Datei.</span><span class="sxs-lookup"><span data-stu-id="21b26-106">The `IsNormalRate` method indicates whether the clip will play at the normal playback rate; that is, the playback rate of the original file.</span></span>

## <a name="syntax"></a><span data-ttu-id="21b26-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="21b26-107">Syntax</span></span>


```C++
HRESULT IsNormalRate(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="21b26-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="21b26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21b26-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="21b26-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="21b26-110">Empfängt einen booleschen Wert, der angibt, wie der Ausschnitt dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="21b26-110">Receives a Boolean value indicating how the clip will render.</span></span> <span data-ttu-id="21b26-111">Wenn der Wert **true** ist, wird der Clip mit dem normalen Satz wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="21b26-111">If the value is **TRUE**, the clip will play at the normal rate.</span></span> <span data-ttu-id="21b26-112">Andernfalls wird die Wiedergabe schneller oder langsamer als normal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21b26-112">Otherwise, it will play faster or slower than normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21b26-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21b26-113">Return value</span></span>

<span data-ttu-id="21b26-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="21b26-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="21b26-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="21b26-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="21b26-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21b26-116">Remarks</span></span>

<span data-ttu-id="21b26-117">Die Wiedergabe Rate eines Clips wird durch die Start-und Endzeit des Mediums bestimmt, relativ zu den Zeitachsen Zeiten:</span><span class="sxs-lookup"><span data-stu-id="21b26-117">A clip's playback rate is determined by its media start and stop times, relative to its timeline times:</span></span>


```C++
Playback rate = (Media Stop <entity type="mdash"/> Media Start) / (Timeline Stop <entity type="mdash"/> Timeline Start)
```



<span data-ttu-id="21b26-118">Wenn dieses Verhältnis gleich 1 ist, wird der Clip mit der erstellten Geschwindigkeit abgespielt.</span><span class="sxs-lookup"><span data-stu-id="21b26-118">If this ratio is equal to 1, the clip plays at the authored speed.</span></span> <span data-ttu-id="21b26-119">Andernfalls wird er schneller oder langsamer abgespielt.</span><span class="sxs-lookup"><span data-stu-id="21b26-119">Otherwise, it plays faster or slower.</span></span> <span data-ttu-id="21b26-120">Weitere Informationen finden Sie unter [Zeit in DirectShow-Bearbeitungs Diensten](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="21b26-120">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="21b26-121">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="21b26-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="21b26-122">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="21b26-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="21b26-123">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="21b26-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="21b26-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21b26-124">Requirements</span></span>



| <span data-ttu-id="21b26-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21b26-125">Requirement</span></span> | <span data-ttu-id="21b26-126">Wert</span><span class="sxs-lookup"><span data-stu-id="21b26-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21b26-127">Header</span><span class="sxs-lookup"><span data-stu-id="21b26-127">Header</span></span><br/>  | <dl> <span data-ttu-id="21b26-128"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="21b26-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="21b26-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="21b26-129">Library</span></span><br/> | <dl> <span data-ttu-id="21b26-130"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="21b26-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21b26-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21b26-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21b26-132">**Iamtimelinesrc-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="21b26-132">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="21b26-133">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="21b26-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




