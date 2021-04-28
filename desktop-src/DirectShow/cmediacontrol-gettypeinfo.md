---
description: 'CMediaControl.GetTypeInfo-Methode: Ruft ein Typinformationsobjekt ab, das die Typinformationen für eine Schnittstelle abrufen kann.'
ms.assetid: 2014485f-d937-415d-a2fc-0c69269b5237
title: CMediaControl.GetTypeInfo-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 857dbdeee9a2add9ab77cae0ff97d69699d2dd2e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099128"
---
# <a name="cmediacontrolgettypeinfo-method"></a><span data-ttu-id="abfd5-103">CMediaControl.GetTypeInfo-Methode</span><span class="sxs-lookup"><span data-stu-id="abfd5-103">CMediaControl.GetTypeInfo method</span></span>

<span data-ttu-id="abfd5-104">Ruft ein Typinformationsobjekt ab, das die Typinformationen für eine Schnittstelle abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="abfd5-104">Retrieves a type-information object, which can retrieve the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="abfd5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="abfd5-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="abfd5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="abfd5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abfd5-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="abfd5-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="abfd5-108">Geben Sie informationen ein, die sie zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="abfd5-108">Type information to return.</span></span> <span data-ttu-id="abfd5-109">Übergeben Sie 0 (null), um Typinformationen für die **IDispatch-Implementierung** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="abfd5-109">Pass zero to retrieve type information for the **IDispatch** implementation.</span></span>

</dd> <dt>

<span data-ttu-id="abfd5-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="abfd5-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="abfd5-111">Die Locale ID für die Typinformationen.</span><span class="sxs-lookup"><span data-stu-id="abfd5-111">Locale ID for the type information.</span></span> <span data-ttu-id="abfd5-112">Für Klassen, die lokalisierte Membernamen unterstützen, kann ein Objekt möglicherweise unterschiedliche Typinformationen für verschiedene Sprachen zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="abfd5-112">For classes that support localized member names, an object might be able to return different type information for different languages.</span></span> <span data-ttu-id="abfd5-113">Für Klassen, die lokalisierte Membernamen nicht unterstützen, kann dieser Parameter ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="abfd5-113">For classes that do not support localized member names, this parameter can be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="abfd5-114">*pptinfo*</span><span class="sxs-lookup"><span data-stu-id="abfd5-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="abfd5-115">Adresse eines Zeigers auf das angeforderte Typinformationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="abfd5-115">Address of a pointer to the type-information object requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abfd5-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="abfd5-116">Return value</span></span>

<span data-ttu-id="abfd5-117">Gibt einen \_ E-ZEIGER zurück, *wenn pptinfo* ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="abfd5-117">Returns an E\_POINTER if *pptinfo* is invalid.</span></span> <span data-ttu-id="abfd5-118">Gibt TYPE \_ E \_ ELEMENTNOTFOUND zurück, *wenn itinfo* nicht 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="abfd5-118">Returns TYPE\_E\_ELEMENTNOTFOUND if *itinfo* is not zero.</span></span> <span data-ttu-id="abfd5-119">Gibt S \_ OK zurück, wenn erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="abfd5-119">Returns S\_OK if is successful.</span></span> <span data-ttu-id="abfd5-120">Andernfalls gibt ein **HRESULT aus** einem der Aufrufe zurück, um den Typ abzurufen.</span><span class="sxs-lookup"><span data-stu-id="abfd5-120">Otherwise, returns an **HRESULT** from one of the calls to retrieve the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="abfd5-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abfd5-121">Requirements</span></span>



| <span data-ttu-id="abfd5-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abfd5-122">Requirement</span></span> | <span data-ttu-id="abfd5-123">Wert</span><span class="sxs-lookup"><span data-stu-id="abfd5-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abfd5-124">Header</span><span class="sxs-lookup"><span data-stu-id="abfd5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="abfd5-125"><dt>Ctlutil.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="abfd5-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="abfd5-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="abfd5-126">Library</span></span><br/> | <dl> <span data-ttu-id="abfd5-127"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="abfd5-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abfd5-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="abfd5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abfd5-129">**CMediaControl-Klasse**</span><span class="sxs-lookup"><span data-stu-id="abfd5-129">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




