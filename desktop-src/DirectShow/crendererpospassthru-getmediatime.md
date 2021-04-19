---
description: Die getmediatime-Methode ruft die Zeitstempel im aktuellen Beispiel ab.
ms.assetid: 13710373-04fd-4c1d-ba97-78be5cf27e7d
title: Crendererpospassthru. getmediatime-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 628c0f0c65dad4e00dd259edbeee97fd8f6f13ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373859"
---
# <a name="crendererpospassthrugetmediatime-method"></a><span data-ttu-id="3a66f-103">Crendererpospassthru. getmediatime-Methode</span><span class="sxs-lookup"><span data-stu-id="3a66f-103">CRendererPosPassThru.GetMediaTime method</span></span>

<span data-ttu-id="3a66f-104">Die- `GetMediaTime` Methode ruft die Zeitstempel im aktuellen Beispiel ab.</span><span class="sxs-lookup"><span data-stu-id="3a66f-104">The `GetMediaTime` method retrieves the time stamps on the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a66f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a66f-105">Syntax</span></span>


```C++
HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="3a66f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a66f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a66f-107">*pstarttime*</span><span class="sxs-lookup"><span data-stu-id="3a66f-107">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="3a66f-108">Ein Zeiger auf eine Variable, die die Startzeit in Einheiten des aktuellen Zeit Formats empfängt.</span><span class="sxs-lookup"><span data-stu-id="3a66f-108">Pointer to a variable that receives the start time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="3a66f-109">*Zeit*</span><span class="sxs-lookup"><span data-stu-id="3a66f-109">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="3a66f-110">Ein Zeiger auf eine Variable, die die Endzeit in Einheiten des aktuellen Zeit Formats empfängt.</span><span class="sxs-lookup"><span data-stu-id="3a66f-110">Pointer to a variable that receives the end time, in units of the current time format.</span></span> <span data-ttu-id="3a66f-111">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="3a66f-111">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a66f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a66f-112">Return value</span></span>

<span data-ttu-id="3a66f-113">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3a66f-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3a66f-114">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="3a66f-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="3a66f-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3a66f-115">Return code</span></span>                                                                                  | <span data-ttu-id="3a66f-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a66f-116">Description</span></span>                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="3a66f-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3a66f-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="3a66f-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="3a66f-118">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3a66f-119"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="3a66f-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="3a66f-120">Die Konvertierung in dieses Format wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3a66f-120">Conversion to this format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="3a66f-121"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="3a66f-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="3a66f-122">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="3a66f-122">**NULL** pointer argument.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="3a66f-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a66f-123">Remarks</span></span>

<span data-ttu-id="3a66f-124">Diese Methode überschreibt die [**cpospassthru:: getmediatime**](cpospassthru-getmediatime.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3a66f-124">This method overrides the [**CPosPassThru::GetMediaTime**](cpospassthru-getmediatime.md) method.</span></span> <span data-ttu-id="3a66f-125">Die Zeitstempel Werte werden in das aktuelle Zeitformat konvertiert, indem die [**cpospassthru:: converttimeformat**](cpospassthru-converttimeformat.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3a66f-125">The time-stamp values are converted to the current time format by calling the [**CPosPassThru::ConvertTimeFormat**](cpospassthru-converttimeformat.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a66f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a66f-126">Requirements</span></span>



| <span data-ttu-id="3a66f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a66f-127">Requirement</span></span> | <span data-ttu-id="3a66f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="3a66f-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a66f-129">Header</span><span class="sxs-lookup"><span data-stu-id="3a66f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3a66f-130"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a66f-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3a66f-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3a66f-131">Library</span></span><br/> | <dl> <span data-ttu-id="3a66f-132">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3a66f-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




