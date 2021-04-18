---
description: Die dbginitialise-Funktion initialisiert die Debug-Bibliothek. Wird in Einzelhandels Builds ignoriert.
ms.assetid: d4ca739e-cd39-4692-81da-c5a88a09d546
title: Dbginitialise-Funktion (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgInitialise
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33a62c8dad7ef6e15b9b11461303b1bced977a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351300"
---
# <a name="dbginitialise-function"></a><span data-ttu-id="aa54d-104">Dbginitialise-Funktion</span><span class="sxs-lookup"><span data-stu-id="aa54d-104">DbgInitialise function</span></span>

<span data-ttu-id="aa54d-105">Die **dbginitialise** -Funktion initialisiert die Debug-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="aa54d-105">The **DbgInitialise** function initializes the debug library.</span></span> <span data-ttu-id="aa54d-106">Wird in Einzelhandels Builds ignoriert.</span><span class="sxs-lookup"><span data-stu-id="aa54d-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa54d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa54d-107">Syntax</span></span>


```C++
void DbgInitialise(
   HINSTANCE hInst
);
```



## <a name="parameters"></a><span data-ttu-id="aa54d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa54d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa54d-109">*hinst*</span><span class="sxs-lookup"><span data-stu-id="aa54d-109">*hInst*</span></span> 
</dt> <dd>

<span data-ttu-id="aa54d-110">Handle für die Modul Instanz.</span><span class="sxs-lookup"><span data-stu-id="aa54d-110">Handle to the module instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa54d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa54d-111">Return value</span></span>

<span data-ttu-id="aa54d-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="aa54d-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa54d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa54d-113">Remarks</span></span>

<span data-ttu-id="aa54d-114">In einer ausführbaren Datei wird diese Methode aufgerufen, bevor die DirectShow-Debugfunktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aa54d-114">In an executable, call this method before using the DirectShow debug facilities.</span></span> <span data-ttu-id="aa54d-115">Bevor die ausführbare Datei beendet wird, müssen Sie die [**dbgend**](dbgterminate.md) -Funktion zum Bereinigen der Debugbibliothek aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="aa54d-115">Before the executable quits, call the [**DbgTerminate**](dbgterminate.md) function to clean up the debug library.</span></span>

<span data-ttu-id="aa54d-116">In einer DLL, die mit der Basisklassen Bibliothek verknüpft ist ("straumbase. lib"), ist es nicht erforderlich, diese Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="aa54d-116">In a DLL that links to the base-class library (Strmbase.lib), it is not necessary to call this function.</span></span> <span data-ttu-id="aa54d-117">Die-Funktion wird automatisch aufgerufen, wenn die dll geladen wird.</span><span class="sxs-lookup"><span data-stu-id="aa54d-117">The function is called automatically when the DLL is loaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa54d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa54d-118">Requirements</span></span>



| <span data-ttu-id="aa54d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa54d-119">Requirement</span></span> | <span data-ttu-id="aa54d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="aa54d-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa54d-121">Header</span><span class="sxs-lookup"><span data-stu-id="aa54d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="aa54d-122"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa54d-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="aa54d-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="aa54d-123">Library</span></span><br/> | <dl> <span data-ttu-id="aa54d-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="aa54d-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa54d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa54d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa54d-126">Debug-Ausgabefunktionen</span><span class="sxs-lookup"><span data-stu-id="aa54d-126">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




