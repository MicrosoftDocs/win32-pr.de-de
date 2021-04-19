---
description: Die SetFormat-Methode initialisiert den Format Block.
ms.assetid: 71f1c3d4-9c45-4124-8560-378c8f66e710
title: Cmediatype. SetFormat-Methode (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08dd05faf514581a3325f4922076ba2053cd0c95
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359624"
---
# <a name="cmediatypesetformat-method"></a><span data-ttu-id="3ddea-103">Cmediatype. SetFormat-Methode</span><span class="sxs-lookup"><span data-stu-id="3ddea-103">CMediaType.SetFormat method</span></span>

<span data-ttu-id="3ddea-104">Die- `SetFormat` Methode initialisiert den Format Block.</span><span class="sxs-lookup"><span data-stu-id="3ddea-104">The `SetFormat` method initializes the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ddea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ddea-105">Syntax</span></span>


```C++
BOOL SetFormat(
   BYTE  *pFormat,
   ULONG length
);
```



## <a name="parameters"></a><span data-ttu-id="3ddea-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ddea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ddea-107">*pformat*</span><span class="sxs-lookup"><span data-stu-id="3ddea-107">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="3ddea-108">Ein Zeiger auf einen Speicherblock, der den Format Block enthält.</span><span class="sxs-lookup"><span data-stu-id="3ddea-108">Pointer to a block of memory that contains the format block.</span></span>

</dd> <dt>

<span data-ttu-id="3ddea-109">*length*</span><span class="sxs-lookup"><span data-stu-id="3ddea-109">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="3ddea-110">Länge des Format Blocks in Bytes.</span><span class="sxs-lookup"><span data-stu-id="3ddea-110">Length of the format block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ddea-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3ddea-111">Return value</span></span>

<span data-ttu-id="3ddea-112">Gibt **true** zurück, wenn erfolgreich, oder **false** , wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="3ddea-112">Returns **TRUE** if successful, or **FALSE** if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ddea-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ddea-113">Remarks</span></span>

<span data-ttu-id="3ddea-114">Diese Methode ordnet Speicher für den Format Block zu und kopiert den durch *pformat* angegebenen Puffer in den neuen Format Block.</span><span class="sxs-lookup"><span data-stu-id="3ddea-114">This method allocates memory for the format block and copies the buffer specified by *pFormat* into the new format block.</span></span> <span data-ttu-id="3ddea-115">Wenn der Medientyp bereits einen Format Block enthält, wird der alte freigegeben.</span><span class="sxs-lookup"><span data-stu-id="3ddea-115">If the media type already contains a format block, the old one is released.</span></span> <span data-ttu-id="3ddea-116">Die-Methode legt auch den **cbformat** -Member **der \_ \_ Medientyp** Struktur "am" fest.</span><span class="sxs-lookup"><span data-stu-id="3ddea-116">The method also sets the **cbFormat** member of the **AM\_MEDIA\_TYPE** structure.</span></span>

<span data-ttu-id="3ddea-117">Um den Formattyp festzulegen, rufen Sie die [**cmediatype:: setformattype**](cmediatype-setformattype.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="3ddea-117">To set the format type, call the [**CMediaType::SetFormatType**](cmediatype-setformattype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ddea-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ddea-118">Requirements</span></span>



| <span data-ttu-id="3ddea-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ddea-119">Requirement</span></span> | <span data-ttu-id="3ddea-120">Wert</span><span class="sxs-lookup"><span data-stu-id="3ddea-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ddea-121">Header</span><span class="sxs-lookup"><span data-stu-id="3ddea-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3ddea-122"><dt>Mtype. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3ddea-122"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="3ddea-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3ddea-123">Library</span></span><br/> | <dl> <span data-ttu-id="3ddea-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3ddea-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ddea-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ddea-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ddea-126">**Cmediatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3ddea-126">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




