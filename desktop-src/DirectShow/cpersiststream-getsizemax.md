---
description: Ruft die maximale Bytegröße ab, die für den aktuellen Stream benötigt wird, einschließlich der Versionsnummer.
ms.assetid: 55ea4568-5ca4-4139-8def-bef20071835d
title: Cpersiststream. GetSizeMax-Methode (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ef9fcd176463aa8b0bc69fabbd74d78d4ca17cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359401"
---
# <a name="cpersiststreamgetsizemax-method"></a><span data-ttu-id="5fb08-103">Cpersiststream. GetSizeMax-Methode</span><span class="sxs-lookup"><span data-stu-id="5fb08-103">CPersistStream.GetSizeMax method</span></span>

<span data-ttu-id="5fb08-104">Ruft die maximale Bytegröße ab, die für den aktuellen Stream benötigt wird, einschließlich der Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="5fb08-104">Retrieves the maximum byte size needed for the current stream, including the version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fb08-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5fb08-105">Syntax</span></span>


```C++
HRESULT GetSizeMax(
   ULARGE_INTEGER *pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="5fb08-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5fb08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fb08-107">*pcbSize*</span><span class="sxs-lookup"><span data-stu-id="5fb08-107">*pcbSize*</span></span> 
</dt> <dd>

<span data-ttu-id="5fb08-108">Ein Zeiger auf die Größe in Bytes, die zum Speichern dieses Streams benötigt wird, einschließlich der Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="5fb08-108">Pointer to the size in bytes needed to save this stream, including the version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fb08-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5fb08-109">Return value</span></span>

<span data-ttu-id="5fb08-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5fb08-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fb08-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5fb08-111">Remarks</span></span>

<span data-ttu-id="5fb08-112">Diese Member-Funktion implementiert die **IPersistStream:: GetSizeMax** -Methode.</span><span class="sxs-lookup"><span data-stu-id="5fb08-112">This member function implements the **IPersistStream::GetSizeMax** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fb08-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5fb08-113">Requirements</span></span>



| <span data-ttu-id="5fb08-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5fb08-114">Requirement</span></span> | <span data-ttu-id="5fb08-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5fb08-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fb08-116">Header</span><span class="sxs-lookup"><span data-stu-id="5fb08-116">Header</span></span><br/>  | <dl> <span data-ttu-id="5fb08-117"><dt>PStream. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5fb08-117"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5fb08-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5fb08-118">Library</span></span><br/> | <dl> <span data-ttu-id="5fb08-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5fb08-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fb08-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fb08-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fb08-121">**Cpersiststream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5fb08-121">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




