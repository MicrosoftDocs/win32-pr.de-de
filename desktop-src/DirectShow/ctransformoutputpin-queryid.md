---
description: 'Die QueryId-Methode ruft einen Bezeichner für die PIN ab. Diese Methode implementiert die IPin:: QueryId-Methode.'
ms.assetid: 3d83db3a-b919-454d-a91a-91f33a952a22
title: Ctransformoutputpin. QueryId-Methode (Transfrm. h)
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
ms.openlocfilehash: 3e8e5fbc4b4da7b38853df5b4dcf3580a8c198d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354697"
---
# <a name="ctransformoutputpinqueryid-method"></a><span data-ttu-id="55f23-104">Ctransformoutputpin. QueryId-Methode</span><span class="sxs-lookup"><span data-stu-id="55f23-104">CTransformOutputPin.QueryId method</span></span>

<span data-ttu-id="55f23-105">Die- `QueryId` Methode ruft einen Bezeichner für die PIN ab.</span><span class="sxs-lookup"><span data-stu-id="55f23-105">The `QueryId` method retrieves an identifier for the pin.</span></span> <span data-ttu-id="55f23-106">Diese Methode implementiert die [**IPin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) -Methode.</span><span class="sxs-lookup"><span data-stu-id="55f23-106">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="55f23-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="55f23-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="55f23-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="55f23-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55f23-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="55f23-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="55f23-110">Empfängt eine Zeichenfolge mit dem PIN-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="55f23-110">Receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55f23-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55f23-111">Return value</span></span>

<span data-ttu-id="55f23-112">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="55f23-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="55f23-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="55f23-113">Return code</span></span>                                                                                   | <span data-ttu-id="55f23-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="55f23-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="55f23-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="55f23-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="55f23-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="55f23-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="55f23-117"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="55f23-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="55f23-118">Nicht genügend Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="55f23-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="55f23-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="55f23-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="55f23-120">**Null** -Zeigerargument</span><span class="sxs-lookup"><span data-stu-id="55f23-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="55f23-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55f23-121">Remarks</span></span>

<span data-ttu-id="55f23-122">Der PIN-Bezeichner wird für die Diagramm Persistenz verwendet.</span><span class="sxs-lookup"><span data-stu-id="55f23-122">The pin identifier is used for graph persistence.</span></span> <span data-ttu-id="55f23-123">Der PIN-Bezeichner für diese Klasse ist out. Diese Klasse überschreibt das Verhalten der [**cbasepin**](cbasepin.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="55f23-123">The pin identifier for this class is Out. This class overrides the behavior of the [**CBasePin**](cbasepin.md) class.</span></span> <span data-ttu-id="55f23-124">In der **cbasepin** -Klasse ist der PIN-Bezeichner mit dem PIN-Namen identisch, der im-Klassenkonstruktor angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="55f23-124">In the **CBasePin** class, the pin identifier is the same as the pin name, specified in the class constructor.</span></span> <span data-ttu-id="55f23-125">In der **ctransforminputpin** -Klasse sind der PIN-Bezeichner und der PIN-Name nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="55f23-125">In the **CTransformInputPin** class, the pin identifier and the pin name are not the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="55f23-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55f23-126">Requirements</span></span>



| <span data-ttu-id="55f23-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55f23-127">Requirement</span></span> | <span data-ttu-id="55f23-128">Wert</span><span class="sxs-lookup"><span data-stu-id="55f23-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55f23-129">Header</span><span class="sxs-lookup"><span data-stu-id="55f23-129">Header</span></span><br/>  | <dl> <span data-ttu-id="55f23-130"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="55f23-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="55f23-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="55f23-131">Library</span></span><br/> | <dl> <span data-ttu-id="55f23-132">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="55f23-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




