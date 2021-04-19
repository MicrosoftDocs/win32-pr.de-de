---
description: Lädt die Filterdaten aus einem angegebenen Datenstrom.
ms.assetid: c2bfd379-2916-4698-bc41-653161723706
title: Cpersiststream. Load-Methode (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Load
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83b16c3fe7bf905d1ade6b7f38cf27c61b44e4d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367066"
---
# <a name="cpersiststreamload-method"></a><span data-ttu-id="50c92-103">Cpersiststream. Load-Methode</span><span class="sxs-lookup"><span data-stu-id="50c92-103">CPersistStream.Load method</span></span>

<span data-ttu-id="50c92-104">Lädt die Filterdaten aus einem angegebenen Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="50c92-104">Loads the filter's data from a given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="50c92-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="50c92-105">Syntax</span></span>


```C++
HRESULT Load(
   LPSTREAM pStm
);
```



## <a name="parameters"></a><span data-ttu-id="50c92-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="50c92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50c92-107">*pstm*</span><span class="sxs-lookup"><span data-stu-id="50c92-107">*pStm*</span></span> 
</dt> <dd>

<span data-ttu-id="50c92-108">Zeiger auf den Stream, aus dem geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="50c92-108">Pointer to the stream from which to be loaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50c92-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50c92-109">Return value</span></span>

<span data-ttu-id="50c92-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="50c92-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50c92-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50c92-111">Remarks</span></span>

<span data-ttu-id="50c92-112">Diese Member-Funktion implementiert die **IPersistStream:: Load** -Methode.</span><span class="sxs-lookup"><span data-stu-id="50c92-112">This member function implements the **IPersistStream::Load** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="50c92-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50c92-113">Requirements</span></span>



| <span data-ttu-id="50c92-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50c92-114">Requirement</span></span> | <span data-ttu-id="50c92-115">Wert</span><span class="sxs-lookup"><span data-stu-id="50c92-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50c92-116">Header</span><span class="sxs-lookup"><span data-stu-id="50c92-116">Header</span></span><br/>  | <dl> <span data-ttu-id="50c92-117"><dt>PStream. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="50c92-117"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="50c92-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="50c92-118">Library</span></span><br/> | <dl> <span data-ttu-id="50c92-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="50c92-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50c92-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50c92-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50c92-121">**Cpersiststream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="50c92-121">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




