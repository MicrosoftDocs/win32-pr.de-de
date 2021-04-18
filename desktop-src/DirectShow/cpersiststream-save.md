---
description: Speichert die Filterdaten in dem angegebenen Stream.
ms.assetid: f45c8c6e-f0bb-4358-805a-da2669706d34
title: Cpersiststream. Save-Methode (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Save
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c16e4820f846d2d60382fabd6aafe3ad82880193
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361294"
---
# <a name="cpersiststreamsave-method"></a><span data-ttu-id="fb97a-103">Cpersiststream. Save-Methode</span><span class="sxs-lookup"><span data-stu-id="fb97a-103">CPersistStream.Save method</span></span>

<span data-ttu-id="fb97a-104">Speichert die Filterdaten in dem angegebenen Stream.</span><span class="sxs-lookup"><span data-stu-id="fb97a-104">Saves the filter's data to the given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb97a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb97a-105">Syntax</span></span>


```C++
HRESULT Save(
   LPSTREAM pStm,
   BOOL     fClearDirty
);
```



## <a name="parameters"></a><span data-ttu-id="fb97a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb97a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb97a-107">*pstm*</span><span class="sxs-lookup"><span data-stu-id="fb97a-107">*pStm*</span></span> 
</dt> <dd>

<span data-ttu-id="fb97a-108">Zeiger auf den Stream, in dem Daten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fb97a-108">Pointer to the stream to which data is to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="fb97a-109">*Klartext*</span><span class="sxs-lookup"><span data-stu-id="fb97a-109">*fClearDirty*</span></span> 
</dt> <dd>

<span data-ttu-id="fb97a-110">Flag, das angibt, ob das geänderte Flag des aktuellen Streams zurückgesetzt werden soll. " **True** " gibt zurück</span><span class="sxs-lookup"><span data-stu-id="fb97a-110">Flag that indicates whether to reset the current stream's dirty flag; **TRUE** means to reset it.</span></span> <span data-ttu-id="fb97a-111">(Wenn die Methode als Teil eines Speicher Vorgangs aufgerufen wird, ist der Wert normalerweise **true**; wenn er als Teil eines "Speichern unter"-Vorgangs aufgerufen wird, ist der Wert in der Regel " **false**".)</span><span class="sxs-lookup"><span data-stu-id="fb97a-111">(When the method is called as part of a Save operation, the value is typically **TRUE**; when called as part of a Save As operation, the value is typically **FALSE**.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb97a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb97a-112">Return value</span></span>

<span data-ttu-id="fb97a-113">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fb97a-113">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb97a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb97a-114">Remarks</span></span>

<span data-ttu-id="fb97a-115">Diese Member-Funktion implementiert die **IPersistStream:: Save** -Methode.</span><span class="sxs-lookup"><span data-stu-id="fb97a-115">This member function implements the **IPersistStream::Save** method.</span></span> <span data-ttu-id="fb97a-116">Er ruft den **Schreib** Vorgang mit der Softwareversion auf, ruft [**cpersiststream:: Write**](cpersiststream-writetostream.md) Team Access Stream mit dem Stream in *pstm* auf und setzt die mPS-bereinigen zurück. **\_**</span><span class="sxs-lookup"><span data-stu-id="fb97a-116">It calls **WriteInt** with the software version, calls [**CPersistStream::WriteToStream**](cpersiststream-writetostream.md) with the stream in *pStm*, and resets **mPS\_fDirty**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb97a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb97a-117">Requirements</span></span>



| <span data-ttu-id="fb97a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb97a-118">Requirement</span></span> | <span data-ttu-id="fb97a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="fb97a-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb97a-120">Header</span><span class="sxs-lookup"><span data-stu-id="fb97a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="fb97a-121"><dt>PStream. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb97a-121"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fb97a-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fb97a-122">Library</span></span><br/> | <dl> <span data-ttu-id="fb97a-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="fb97a-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb97a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb97a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb97a-125">**Cpersiststream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="fb97a-125">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




