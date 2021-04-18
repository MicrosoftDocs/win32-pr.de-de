---
description: Konstruktormethode.
ms.assetid: 9078b2f5-b11e-4780-8143-6738e9df4f4b
title: Csourcestream. csourcestream-Konstruktor (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8671e939364d1c0cd22796b1518313002b5eb33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358048"
---
# <a name="csourcestreamcsourcestream-constructor"></a><span data-ttu-id="48187-103">Csourcestream. csourcestream-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="48187-103">CSourceStream.CSourceStream constructor</span></span>

<span data-ttu-id="48187-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="48187-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="48187-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="48187-105">Syntax</span></span>


```C++
CSourceStream(
   TCHAR   *pObjectName,
   HRESULT *phr,
   CSource *pms,
   LPCWSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="48187-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="48187-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48187-107">*pobjectname*</span><span class="sxs-lookup"><span data-stu-id="48187-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="48187-108">Zeiger auf eine Zeichenfolge, die den debugnamen der PIN enthält.</span><span class="sxs-lookup"><span data-stu-id="48187-108">Pointer to a string containing the debug name of the pin.</span></span>

</dd> <dt>

<span data-ttu-id="48187-109">*PHR*</span><span class="sxs-lookup"><span data-stu-id="48187-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="48187-110">Ein Zeiger auf eine Variable, die einen **HRESULT** -Wert empfängt, der angibt, ob die Methode erfolgreich war oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="48187-110">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="48187-111">Initialisieren Sie den Wert \_ vor dem Erstellen des-Objekts auf S OK.</span><span class="sxs-lookup"><span data-stu-id="48187-111">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="48187-112">Der Wert wird nur geändert, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="48187-112">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="48187-113">*PMS*</span><span class="sxs-lookup"><span data-stu-id="48187-113">*pms*</span></span> 
</dt> <dd>

<span data-ttu-id="48187-114">Zeiger auf den [**CSource**](csource.md) -Filter, der diese Pin erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="48187-114">Pointer to the [**CSource**](csource.md) filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="48187-115">*pName*</span><span class="sxs-lookup"><span data-stu-id="48187-115">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="48187-116">Zeiger auf eine Zeichenfolge, die den Namen der PIN enthält.</span><span class="sxs-lookup"><span data-stu-id="48187-116">Pointer to a string that contains the name of the pin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48187-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48187-117">Remarks</span></span>

<span data-ttu-id="48187-118">Die im *pobjectname* -Parameter angegebene Zeichenfolge wird nur für Debugzwecke verwendet.</span><span class="sxs-lookup"><span data-stu-id="48187-118">The string given in the *pObjectName* parameter is used only for debugging purposes.</span></span> <span data-ttu-id="48187-119">Weitere Informationen finden Sie unter [**cbaseobject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="48187-119">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

<span data-ttu-id="48187-120">Die im *PName* -Parameter angegebene Zeichenfolge ist der Name, der von der [**IPin:: querypininfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) -Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="48187-120">The string given in the *pName* parameter is the name returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="48187-121">Die- `CSourceStream` Klasse verwendet diesen Namen nicht für den PIN-Bezeichner, der von der [**csourcestream:: QueryId**](csourcestream-queryid.md) -Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="48187-121">The `CSourceStream` class does not use this name for the pin identifier returned by the [**CSourceStream::QueryId**](csourcestream-queryid.md) method.</span></span> <span data-ttu-id="48187-122">Stattdessen berechnet **QueryId** einen PIN-Bezeichner basierend auf der PIN-Nummer.</span><span class="sxs-lookup"><span data-stu-id="48187-122">Instead, **QueryId** calculates a pin identifier based on the pin number.</span></span> <span data-ttu-id="48187-123">(PIN-Bezeichner unterstützen die Diagramm Persistenz.</span><span class="sxs-lookup"><span data-stu-id="48187-123">(Pin identifiers support graph persistence.</span></span> <span data-ttu-id="48187-124">Weitere Informationen finden Sie unter [**IPin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).)</span><span class="sxs-lookup"><span data-stu-id="48187-124">For more information, see [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).)</span></span>

<span data-ttu-id="48187-125">Der Konstruktor fügt die PIN automatisch dem besitzenden Filter hinzu, indem [**CSource:: addpin**](csource-addpin.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="48187-125">The constructor automatically adds the pin to the owning filter, by calling [**CSource::AddPin**](csource-addpin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="48187-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48187-126">Requirements</span></span>



| <span data-ttu-id="48187-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48187-127">Requirement</span></span> | <span data-ttu-id="48187-128">Wert</span><span class="sxs-lookup"><span data-stu-id="48187-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48187-129">Header</span><span class="sxs-lookup"><span data-stu-id="48187-129">Header</span></span><br/>  | <dl> <span data-ttu-id="48187-130"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="48187-130"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="48187-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="48187-131">Library</span></span><br/> | <dl> <span data-ttu-id="48187-132">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="48187-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48187-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48187-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48187-134">**Csourcestream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="48187-134">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




