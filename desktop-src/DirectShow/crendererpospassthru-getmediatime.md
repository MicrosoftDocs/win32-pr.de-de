---
description: 'CRendererPosPassThru.GetMediaTime-Methode: Die GetMediaTime-Methode ruft die Zeitstempel im aktuellen Beispiel ab.'
ms.assetid: 13710373-04fd-4c1d-ba97-78be5cf27e7d
title: CRendererPosPassThru.GetMediaTime-Methode (Ctlutil.h)
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
ms.openlocfilehash: 588c92faec6b68cfa51392d4df00567c4e881460
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085368"
---
# <a name="crendererpospassthrugetmediatime-method"></a><span data-ttu-id="bb3e1-103">CRendererPosPassThru.GetMediaTime-Methode</span><span class="sxs-lookup"><span data-stu-id="bb3e1-103">CRendererPosPassThru.GetMediaTime method</span></span>

<span data-ttu-id="bb3e1-104">Die `GetMediaTime` -Methode ruft die Zeitstempel für das aktuelle Beispiel ab.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-104">The `GetMediaTime` method retrieves the time stamps on the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb3e1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb3e1-105">Syntax</span></span>


```C++
HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="bb3e1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb3e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb3e1-107">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="bb3e1-107">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="bb3e1-108">Zeiger auf eine Variable, die die Startzeit in Einheiten des aktuellen Zeitformats empfängt.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-108">Pointer to a variable that receives the start time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="bb3e1-109">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="bb3e1-109">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="bb3e1-110">Zeiger auf eine Variable, die die Endzeit in Einheiten des aktuellen Zeitformats empfängt.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-110">Pointer to a variable that receives the end time, in units of the current time format.</span></span> <span data-ttu-id="bb3e1-111">Kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-111">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb3e1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb3e1-112">Return value</span></span>

<span data-ttu-id="bb3e1-113">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="bb3e1-114">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="bb3e1-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="bb3e1-115">Return code</span></span>                                                                                  | <span data-ttu-id="bb3e1-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb3e1-116">Description</span></span>                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="bb3e1-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bb3e1-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="bb3e1-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-118">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="bb3e1-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="bb3e1-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="bb3e1-120">Die Konvertierung in dieses Format wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-120">Conversion to this format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="bb3e1-121"><dt>**E \_ POINTER**</dt></span><span class="sxs-lookup"><span data-stu-id="bb3e1-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="bb3e1-122">**NULL-Zeigerargument.**</span><span class="sxs-lookup"><span data-stu-id="bb3e1-122">**NULL** pointer argument.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="bb3e1-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb3e1-123">Remarks</span></span>

<span data-ttu-id="bb3e1-124">Diese Methode überschreibt die [**CPosPassThru::GetMediaTime-Methode.**](cpospassthru-getmediatime.md)</span><span class="sxs-lookup"><span data-stu-id="bb3e1-124">This method overrides the [**CPosPassThru::GetMediaTime**](cpospassthru-getmediatime.md) method.</span></span> <span data-ttu-id="bb3e1-125">Die Zeitstempelwerte werden in das aktuelle Zeitformat konvertiert, indem die [**CPosPassThru::ConvertTimeFormat-Methode**](cpospassthru-converttimeformat.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-125">The time-stamp values are converted to the current time format by calling the [**CPosPassThru::ConvertTimeFormat**](cpospassthru-converttimeformat.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb3e1-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb3e1-126">Requirements</span></span>



| <span data-ttu-id="bb3e1-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb3e1-127">Requirement</span></span> | <span data-ttu-id="bb3e1-128">Wert</span><span class="sxs-lookup"><span data-stu-id="bb3e1-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb3e1-129">Header</span><span class="sxs-lookup"><span data-stu-id="bb3e1-129">Header</span></span><br/>  | <dl> <span data-ttu-id="bb3e1-130"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb3e1-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bb3e1-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bb3e1-131">Library</span></span><br/> | <dl> <span data-ttu-id="bb3e1-132"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="bb3e1-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




