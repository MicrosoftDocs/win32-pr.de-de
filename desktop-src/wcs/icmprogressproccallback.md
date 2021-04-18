---
title: ICMProgressProcCallback-Rückruffunktion
description: Die icmprogressproccallback-Funktion ist eine von der Anwendung bereitgestellte Rückruffunktion, die den Fortschritt meldet und es der Anwendung ermöglicht, die Farbverarbeitung abzubrechen.
ms.assetid: 4e0bfa4c-f0eb-4776-98d6-90d9adf71bee
keywords:
- Icmprogressproccallback-Rückruffunktion Windows Color System
topic_type:
- apiref
api_name:
- ICMProgressProcCallback
api_location:
- Icm.h
api_type:
- UserDefined
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8acf790a135a41e4eabb4a67c2498f1ed914c4c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371972"
---
# <a name="icmprogressproccallback-callback-function"></a><span data-ttu-id="16421-104">ICMProgressProcCallback-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="16421-104">ICMProgressProcCallback callback function</span></span>

<span data-ttu-id="16421-105">Die **icmprogressproccallback** -Funktion ist eine von der Anwendung bereitgestellte Rückruffunktion, die den Fortschritt meldet und es der Anwendung ermöglicht, die Farbverarbeitung abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="16421-105">The **ICMProgressProcCallback** function is an application-supplied callback function that reports progress and permits the application to cancel color processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="16421-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="16421-106">Syntax</span></span>


```C++
BOOL WINAPI ICMProgressProcCallback(
   ULONG  ulMax,
   ULONG  ulCurrent,
   LPARAM ulCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="16421-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="16421-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16421-108">*ulmax*</span><span class="sxs-lookup"><span data-stu-id="16421-108">*ulMax*</span></span> 
</dt> <dd>

<span data-ttu-id="16421-109">Gibt den maximalen Wert des Fortschritts Zählers an (der zum Schätzen der Vervollständigung der bitmapverarbeitung verwendet wird).</span><span class="sxs-lookup"><span data-stu-id="16421-109">Specifies the maximum value of the progress counter (used to estimate completion of the bitmap processing).</span></span>

</dd> <dt>

<span data-ttu-id="16421-110">*ulcurrent*</span><span class="sxs-lookup"><span data-stu-id="16421-110">*ulCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="16421-111">Gibt den aktuellen Wert des Status Zählers an (Wenn dividiert durch den maximalen Wert ist, wird eine grobe Schätzung des Abschlusses in Prozent angegeben).</span><span class="sxs-lookup"><span data-stu-id="16421-111">Specifies the current value of the progress counter (when divided by the maximum value, provides a rough estimate of percentage of completion).</span></span>

</dd> <dt>

<span data-ttu-id="16421-112">*ulcallbackdata*</span><span class="sxs-lookup"><span data-stu-id="16421-112">*ulCallbackData*</span></span> 
</dt> <dd>

<span data-ttu-id="16421-113">Gibt die Daten an, die von der Anwendung an eine ICM2-Funktion weitergegeben werden, die Sie dann an die Rückruffunktion übergibt.</span><span class="sxs-lookup"><span data-stu-id="16421-113">Specifies the data which is passed by the application to an ICM2 function, which then passes it on to the callback function.</span></span> <span data-ttu-id="16421-114">Diese Daten können z. b. verwendet werden, um die Bitmap und den Prozess zu identifizieren, über den der Fortschritt berichtet wird.</span><span class="sxs-lookup"><span data-stu-id="16421-114">Such data can be used, for example, to identify the bitmap and process about which progress is being reported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16421-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="16421-115">Return value</span></span>

<span data-ttu-id="16421-116">Diese Funktion gibt **true** zurück, um die bitmapverarbeitung fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="16421-116">This function returns **TRUE** to continue bitmap processing.</span></span> <span data-ttu-id="16421-117">Der Rückgabewert ist " **false** ", um die Verarbeitung abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="16421-117">The return value is **FALSE** to cancel processing.</span></span> <span data-ttu-id="16421-118">Wenn die Verarbeitung abgebrochen wird, gibt die aufrufende Funktion NULL zurück, um einen Fehler anzugeben, obwohl der Ausgabepuffer möglicherweise teilweise ausgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="16421-118">If processing is canceled, the calling function returns zero to indicate failure, although its output buffer may be partially filled.</span></span>

## <a name="remarks"></a><span data-ttu-id="16421-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16421-119">Remarks</span></span>

<span data-ttu-id="16421-120">Der Name dieser Rückruffunktion wird von der Anwendung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="16421-120">The name of this callback function is supplied by the application.</span></span> <span data-ttu-id="16421-121">Eine Reihe von WCS-Funktionen, einschließlich [**translatebitmapbits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) und [**checkbitmapbits**](/windows/win32/api/icm/nf-icm-checkbitmapbits), wird diese Funktion in regelmäßigen Abständen aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="16421-121">A number of WCS functions, including [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) and [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits), call this function periodically.</span></span>

## <a name="requirements"></a><span data-ttu-id="16421-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16421-122">Requirements</span></span>



| <span data-ttu-id="16421-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16421-123">Requirement</span></span> | <span data-ttu-id="16421-124">Wert</span><span class="sxs-lookup"><span data-stu-id="16421-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="16421-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="16421-125">Minimum supported client</span></span><br/> | <span data-ttu-id="16421-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16421-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="16421-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="16421-127">Minimum supported server</span></span><br/> | <span data-ttu-id="16421-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16421-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="16421-129">Header</span><span class="sxs-lookup"><span data-stu-id="16421-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="16421-130"><dt>ICM. h</dt></span><span class="sxs-lookup"><span data-stu-id="16421-130"><dt>Icm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16421-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16421-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16421-132">Konzepte der grundlegenden Farbverwaltung</span><span class="sxs-lookup"><span data-stu-id="16421-132">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="16421-133">Funktionen</span><span class="sxs-lookup"><span data-stu-id="16421-133">Functions</span></span>](functions.md)
</dt> <dt>

[<span data-ttu-id="16421-134">**Translatebitmapbits**</span><span class="sxs-lookup"><span data-stu-id="16421-134">**TranslateBitmapBits**</span></span>](/windows/win32/api/icm/nf-icm-translatebitmapbits)
</dt> <dt>

[<span data-ttu-id="16421-135">**Checkbitmapbits**</span><span class="sxs-lookup"><span data-stu-id="16421-135">**CheckBitmapBits**</span></span>](/windows/win32/api/icm/nf-icm-checkbitmapbits)
</dt> </dl>
