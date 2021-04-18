---
description: Die GetEffect-Methode ruft den Effekt auf der angegebenen Prioritäts Ebene ab.
ms.assetid: 8606c457-1c4d-4a20-b674-aaf82abeb451
title: 'Iamtimelineeffectable:: GetEffect-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.GetEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b7a769fca28ea1f8f698b23de7df6b7c15f05234
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365841"
---
# <a name="iamtimelineeffectablegeteffect-method"></a><span data-ttu-id="194e9-103">Iamtimelineeffectable:: GetEffect-Methode</span><span class="sxs-lookup"><span data-stu-id="194e9-103">IAMTimelineEffectable::GetEffect method</span></span>

> [!Note]  
> <span data-ttu-id="194e9-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="194e9-104">\[Deprecated.</span></span> <span data-ttu-id="194e9-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="194e9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="194e9-106">Die **GetEffect** -Methode ruft den Effekt auf der angegebenen Prioritäts Ebene ab.</span><span class="sxs-lookup"><span data-stu-id="194e9-106">The **GetEffect** method retrieves the effect at the specified priority level.</span></span>

## <a name="syntax"></a><span data-ttu-id="194e9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="194e9-107">Syntax</span></span>


```C++
HRESULT GetEffect(
  [out] IAMTimelineObj **ppFX,
        long           Which
);
```



## <a name="parameters"></a><span data-ttu-id="194e9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="194e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="194e9-109">*ppfx* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="194e9-109">*ppFX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="194e9-110">Empfängt die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des Effekts.</span><span class="sxs-lookup"><span data-stu-id="194e9-110">Receives the effect's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="194e9-111">*,*</span><span class="sxs-lookup"><span data-stu-id="194e9-111">*Which*</span></span> 
</dt> <dd>

<span data-ttu-id="194e9-112">Prioritätsstufe des abzurufenden Effekts.</span><span class="sxs-lookup"><span data-stu-id="194e9-112">Priority level of the effect to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="194e9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="194e9-113">Return value</span></span>

<span data-ttu-id="194e9-114">Gibt einen HRESULT-Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="194e9-114">Returns an HRESULT value.</span></span> <span data-ttu-id="194e9-115">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="194e9-115">Possible values include the following:</span></span>



| <span data-ttu-id="194e9-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="194e9-116">Return code</span></span>                                                                               | <span data-ttu-id="194e9-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="194e9-117">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="194e9-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="194e9-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="194e9-119">Keine Auswirkung mit der angegebenen Priorität,</span><span class="sxs-lookup"><span data-stu-id="194e9-119">No effect at the specified priority,</span></span><br/> |
| <dl> <span data-ttu-id="194e9-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="194e9-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="194e9-121">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="194e9-121">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="194e9-122"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="194e9-122"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="194e9-123">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="194e9-123">**NULL** pointer argument.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="194e9-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="194e9-124">Remarks</span></span>

<span data-ttu-id="194e9-125">Wenn die Methode S OK zurückgibt \_ , weist die zurückgegebene **iamtimelineobj** -Schnittstelle einen ausstehenden Verweis Zähler auf.</span><span class="sxs-lookup"><span data-stu-id="194e9-125">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="194e9-126">Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="194e9-126">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="194e9-127">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="194e9-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="194e9-128">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="194e9-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="194e9-129">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="194e9-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="194e9-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="194e9-130">Requirements</span></span>



| <span data-ttu-id="194e9-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="194e9-131">Requirement</span></span> | <span data-ttu-id="194e9-132">Wert</span><span class="sxs-lookup"><span data-stu-id="194e9-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="194e9-133">Header</span><span class="sxs-lookup"><span data-stu-id="194e9-133">Header</span></span><br/>  | <dl> <span data-ttu-id="194e9-134"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="194e9-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="194e9-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="194e9-135">Library</span></span><br/> | <dl> <span data-ttu-id="194e9-136"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="194e9-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="194e9-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="194e9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="194e9-138">**Iamtimelineeffectable-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="194e9-138">**IAMTimelineEffectable Interface**</span></span>](iamtimelineeffectable.md)
</dt> <dt>

[<span data-ttu-id="194e9-139">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="194e9-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




