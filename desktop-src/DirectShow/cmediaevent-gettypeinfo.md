---
description: 'CMediaEvent.GetTypeInfo-Methode: Ruft ein Typinformationsobjekt ab, das die Typinformationen für eine Schnittstelle abrufen kann.'
ms.assetid: d54042d5-e9d3-415c-b90d-1fe7d38164f5
title: CMediaEvent.GetTypeInfo-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f93e3227051729f9d16e1f9ef8de464a14cca33b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095568"
---
# <a name="cmediaeventgettypeinfo-method"></a><span data-ttu-id="38595-103">CMediaEvent.GetTypeInfo-Methode</span><span class="sxs-lookup"><span data-stu-id="38595-103">CMediaEvent.GetTypeInfo method</span></span>

<span data-ttu-id="38595-104">Ruft ein Typinformationsobjekt ab, das die Typinformationen für eine Schnittstelle abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="38595-104">Retrieves a type-information object, which can retrieve the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="38595-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="38595-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="38595-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="38595-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38595-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="38595-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="38595-108">Geben Sie die zurückzugebende Information ein.</span><span class="sxs-lookup"><span data-stu-id="38595-108">Type information to return.</span></span> <span data-ttu-id="38595-109">Übergeben Sie 0 (null), um Typinformationen für die **IDispatch-Implementierung** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="38595-109">Pass zero to retrieve type information for the **IDispatch** implementation.</span></span>

</dd> <dt>

<span data-ttu-id="38595-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="38595-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="38595-111">Gebietsschema-ID für die Typinformationen.</span><span class="sxs-lookup"><span data-stu-id="38595-111">Locale ID for the type information.</span></span> <span data-ttu-id="38595-112">Für Klassen, die lokalisierte Membernamen unterstützen, kann ein Objekt möglicherweise unterschiedliche Typinformationen für verschiedene Sprachen zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="38595-112">For classes that support localized member names, an object might be able to return different type information for different languages.</span></span> <span data-ttu-id="38595-113">Für Klassen, die lokalisierte Membernamen nicht unterstützen, kann dieser Parameter ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="38595-113">For classes that do not support localized member names, this parameter can be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="38595-114">*pptinfo*</span><span class="sxs-lookup"><span data-stu-id="38595-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="38595-115">Adresse eines Zeigers auf das angeforderte Typinformationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="38595-115">Address of a pointer to the type-information object requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38595-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38595-116">Return value</span></span>

<span data-ttu-id="38595-117">Gibt einen E \_ POINTER zurück, wenn *pptinfo* ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="38595-117">Returns an E\_POINTER if *pptinfo* is invalid.</span></span> <span data-ttu-id="38595-118">Gibt TYPE \_ E \_ ELEMENTNOTFOUND zurück, wenn *itinfo* nicht 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="38595-118">Returns TYPE\_E\_ELEMENTNOTFOUND if *itinfo* is not zero.</span></span> <span data-ttu-id="38595-119">Gibt S \_ OK zurück, wenn erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="38595-119">Returns S\_OK if is successful.</span></span> <span data-ttu-id="38595-120">Andernfalls gibt ein **HRESULT** aus einem der Aufrufe zurück, um den Typ abzurufen.</span><span class="sxs-lookup"><span data-stu-id="38595-120">Otherwise, returns an **HRESULT** from one of the calls to retrieve the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="38595-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38595-121">Requirements</span></span>



| <span data-ttu-id="38595-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38595-122">Requirement</span></span> | <span data-ttu-id="38595-123">Wert</span><span class="sxs-lookup"><span data-stu-id="38595-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38595-124">Header</span><span class="sxs-lookup"><span data-stu-id="38595-124">Header</span></span><br/>  | <dl> <span data-ttu-id="38595-125"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="38595-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="38595-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="38595-126">Library</span></span><br/> | <dl> <span data-ttu-id="38595-127"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="38595-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38595-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="38595-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38595-129">**CMediaEvent-Klasse**</span><span class="sxs-lookup"><span data-stu-id="38595-129">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




