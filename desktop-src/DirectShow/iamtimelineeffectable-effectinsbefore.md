---
description: Die effectinsbefore-Methode fügt einen Effekt auf der angegebenen Prioritäts Ebene in das-Objekt ein.
ms.assetid: 6c98e24a-5bac-4273-ae3c-2ab3c9d9465b
title: 'Iamtimelineeffectable:: effectinsbefore-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eeca130f90cee5985f697a4efa042e3b4cb065b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369295"
---
# <a name="iamtimelineeffectableeffectinsbefore-method"></a><span data-ttu-id="64ea5-103">Iamtimelineeffectable:: effectinsbefore-Methode</span><span class="sxs-lookup"><span data-stu-id="64ea5-103">IAMTimelineEffectable::EffectInsBefore method</span></span>

> [!Note]  
> <span data-ttu-id="64ea5-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="64ea5-104">\[Deprecated.</span></span> <span data-ttu-id="64ea5-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="64ea5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="64ea5-106">Die- `EffectInsBefore` Methode fügt einen Effekt auf der angegebenen Prioritäts Ebene in das-Objekt ein.</span><span class="sxs-lookup"><span data-stu-id="64ea5-106">The `EffectInsBefore` method inserts an effect into the object at the specified priority level.</span></span>

## <a name="syntax"></a><span data-ttu-id="64ea5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="64ea5-107">Syntax</span></span>


```C++
HRESULT EffectInsBefore(
   IAMTimelineObj *pFX,
   long           Priority
);
```



## <a name="parameters"></a><span data-ttu-id="64ea5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="64ea5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64ea5-109">*PFX*</span><span class="sxs-lookup"><span data-stu-id="64ea5-109">*pFX*</span></span> 
</dt> <dd>

<span data-ttu-id="64ea5-110">Ein Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des Effekts.</span><span class="sxs-lookup"><span data-stu-id="64ea5-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the effect.</span></span>

</dd> <dt>

<span data-ttu-id="64ea5-111">*Priority*</span><span class="sxs-lookup"><span data-stu-id="64ea5-111">*Priority*</span></span> 
</dt> <dd>

<span data-ttu-id="64ea5-112">Prioritätsstufe, bei der der Effekt eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64ea5-112">Priority level at which to insert the effect.</span></span> <span data-ttu-id="64ea5-113">Verwenden Sie den Wert – 1, um den Effekt am Ende der Prioritäts Liste einzufügen.</span><span class="sxs-lookup"><span data-stu-id="64ea5-113">Use the value –1 to insert the effect at the end of the priority list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64ea5-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64ea5-114">Return value</span></span>

<span data-ttu-id="64ea5-115">Gibt \_ bei Erfolg S OK zurück, oder E benachrichtigt, \_ Wenn das Objekt nicht wirksam ist.</span><span class="sxs-lookup"><span data-stu-id="64ea5-115">Returns S\_OK if successful or E\_NOTIMPL if the object is not an effect.</span></span> <span data-ttu-id="64ea5-116">Andernfalls wird ein anderer **HRESULT** -Wert zurückgegeben, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="64ea5-116">Otherwise, returns another **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="64ea5-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64ea5-117">Remarks</span></span>

<span data-ttu-id="64ea5-118">Die Start-und Endzeiten des Effekts werden bei Bedarf innerhalb der Grenzen des-Zeit Bereichs des Objekts abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="64ea5-118">The start and stop times of the effect are clipped within the bounds of the object's time range, if necessary.</span></span> <span data-ttu-id="64ea5-119">Wenn bereits ein Effekt auf der angegebenen Prioritätsstufe vorliegt, werden alle Effekte von diesem Punkt auf der Prioritäts Liste nach unten verschoben, um Platz für den neuen Effekt zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="64ea5-119">If there is already an effect at the specified priority level, all the effects from that point on move down the priority list to make room for the new effect.</span></span>

> [!Note]  
> <span data-ttu-id="64ea5-120">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="64ea5-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="64ea5-121">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="64ea5-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="64ea5-122">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="64ea5-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="64ea5-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64ea5-123">Requirements</span></span>



| <span data-ttu-id="64ea5-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64ea5-124">Requirement</span></span> | <span data-ttu-id="64ea5-125">Wert</span><span class="sxs-lookup"><span data-stu-id="64ea5-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64ea5-126">Header</span><span class="sxs-lookup"><span data-stu-id="64ea5-126">Header</span></span><br/>  | <dl> <span data-ttu-id="64ea5-127"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="64ea5-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="64ea5-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="64ea5-128">Library</span></span><br/> | <dl> <span data-ttu-id="64ea5-129"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="64ea5-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64ea5-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64ea5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64ea5-131">**Iamtimelineeffectable-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="64ea5-131">**IAMTimelineEffectable Interface**</span></span>](iamtimelineeffectable.md)
</dt> <dt>

[<span data-ttu-id="64ea5-132">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="64ea5-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




