---
description: Erfahren Sie mehr über die cmediatype. cmediatype-Konstruktormethode (mtype. h). Diese Methode verwendet den Parameter "majortype".
ms.assetid: 89356578-0509-46c1-abd4-421688017f1d
title: Cmediatype. cmediatype-Konstruktor (mtype. h)-majortype-Parameter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a99717e41424a99b3c1e79674426fb14c5b57b9d
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2021
ms.locfileid: "106353409"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---majortype-parameter"></a><span data-ttu-id="2fb67-104">Cmediatype. cmediatype-Konstruktor (mtype. h)-majortype-Parameter</span><span class="sxs-lookup"><span data-stu-id="2fb67-104">CMediaType.CMediaType constructor (Mtype.h) - majortype parameter</span></span>

<span data-ttu-id="2fb67-105">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="2fb67-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fb67-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fb67-106">Syntax</span></span>


```C++
CMediaType(
   const GUID *majortype
);
```



## <a name="parameters"></a><span data-ttu-id="2fb67-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fb67-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fb67-108">*majortype*</span><span class="sxs-lookup"><span data-stu-id="2fb67-108">*majortype*</span></span> 
</dt> <dd>

<span data-ttu-id="2fb67-109">Zeiger auf eine **GUID** des Haupt Typs.</span><span class="sxs-lookup"><span data-stu-id="2fb67-109">Pointer to a major type **GUID**.</span></span> <span data-ttu-id="2fb67-110">Der Konstruktor initialisiert die GUID des Haupt Typs mit diesem Wert.</span><span class="sxs-lookup"><span data-stu-id="2fb67-110">The constructor initializes the major type GUID to this value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2fb67-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2fb67-111">Remarks</span></span>

<span data-ttu-id="2fb67-112">Der Konstruktor ruft die [**cmediatype:: initmediatype**](cmediatype-initmediatype.md) -Methode auf, um den Medientyp zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="2fb67-112">The constructor calls the [**CMediaType::InitMediaType**](cmediatype-initmediatype.md) method to initialize the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fb67-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2fb67-113">Requirements</span></span>

| <span data-ttu-id="2fb67-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2fb67-114">Requirement</span></span>                   | <span data-ttu-id="2fb67-115">Wert</span><span class="sxs-lookup"><span data-stu-id="2fb67-115">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fb67-116">Header</span><span class="sxs-lookup"><span data-stu-id="2fb67-116">Header</span></span>  | <span data-ttu-id="2fb67-117">Mtype. h (Include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="2fb67-117">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="2fb67-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2fb67-118">Library</span></span> | <span data-ttu-id="2fb67-119">"Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds)</span><span class="sxs-lookup"><span data-stu-id="2fb67-119">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="2fb67-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2fb67-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fb67-121">**Cmediatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2fb67-121">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




