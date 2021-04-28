---
description: 'CTransformOutputPin.QueryId-Methode: Die QueryId-Methode ruft einen Bezeichner für den Pin ab. Diese Methode implementiert die IPin::QueryId-Methode.'
ms.assetid: 3d83db3a-b919-454d-a91a-91f33a952a22
title: CTransformOutputPin.QueryId-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d4c2d222ca4dd184adfe41f9f610b10f15ee9f02
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094848"
---
# <a name="ctransformoutputpinqueryid-method"></a><span data-ttu-id="d681a-104">CTransformOutputPin.QueryId-Methode</span><span class="sxs-lookup"><span data-stu-id="d681a-104">CTransformOutputPin.QueryId method</span></span>

<span data-ttu-id="d681a-105">Die `QueryId` -Methode ruft einen Bezeichner für den Pin ab.</span><span class="sxs-lookup"><span data-stu-id="d681a-105">The `QueryId` method retrieves an identifier for the pin.</span></span> <span data-ttu-id="d681a-106">Diese Methode implementiert die [**IPin::QueryId-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)</span><span class="sxs-lookup"><span data-stu-id="d681a-106">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d681a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d681a-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="d681a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d681a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d681a-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="d681a-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="d681a-110">Empfängt eine Zeichenfolge, die den Stecknadelbezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="d681a-110">Receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d681a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d681a-111">Return value</span></span>

<span data-ttu-id="d681a-112">Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.</span><span class="sxs-lookup"><span data-stu-id="d681a-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="d681a-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d681a-113">Return code</span></span>                                                                                   | <span data-ttu-id="d681a-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d681a-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="d681a-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d681a-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d681a-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="d681a-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="d681a-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d681a-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d681a-118">Nicht genügend Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="d681a-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="d681a-119"><dt>**E \_ POINTER**</dt></span><span class="sxs-lookup"><span data-stu-id="d681a-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d681a-120">**NULL-Zeigerargument**</span><span class="sxs-lookup"><span data-stu-id="d681a-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d681a-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d681a-121">Remarks</span></span>

<span data-ttu-id="d681a-122">Der Stecknadelbezeichner wird für die Graphpersistenz verwendet.</span><span class="sxs-lookup"><span data-stu-id="d681a-122">The pin identifier is used for graph persistence.</span></span> <span data-ttu-id="d681a-123">Der Stecknadelbezeichner für diese Klasse ist Out. Diese Klasse überschreibt das Verhalten der [**CBasePin-Klasse.**](cbasepin.md)</span><span class="sxs-lookup"><span data-stu-id="d681a-123">The pin identifier for this class is Out. This class overrides the behavior of the [**CBasePin**](cbasepin.md) class.</span></span> <span data-ttu-id="d681a-124">In der **CBasePin-Klasse** ist der Stecknadelbezeichner mit dem Pinnamen identisch, der im Klassenkonstruktor angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d681a-124">In the **CBasePin** class, the pin identifier is the same as the pin name, specified in the class constructor.</span></span> <span data-ttu-id="d681a-125">In der **CTransformInputPin-Klasse** sind der Stecknadelbezeichner und der Pinname nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="d681a-125">In the **CTransformInputPin** class, the pin identifier and the pin name are not the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="d681a-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d681a-126">Requirements</span></span>



| <span data-ttu-id="d681a-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d681a-127">Requirement</span></span> | <span data-ttu-id="d681a-128">Wert</span><span class="sxs-lookup"><span data-stu-id="d681a-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d681a-129">Header</span><span class="sxs-lookup"><span data-stu-id="d681a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d681a-130"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="d681a-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d681a-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d681a-131">Library</span></span><br/> | <dl> <span data-ttu-id="d681a-132"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d681a-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




