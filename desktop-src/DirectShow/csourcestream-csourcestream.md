---
description: 'CSourceStream.CSourceStream-Konstruktor : Konstruktormethode.'
ms.assetid: 9078b2f5-b11e-4780-8143-6738e9df4f4b
title: CSourceStream.CSourceStream-Konstruktor (Source.h)
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
ms.openlocfilehash: 75d94bb89ca109c2a7974c294153d46235f92f23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085188"
---
# <a name="csourcestreamcsourcestream-constructor"></a><span data-ttu-id="55ea2-103">CSourceStream.CSourceStream-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="55ea2-103">CSourceStream.CSourceStream constructor</span></span>

<span data-ttu-id="55ea2-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="55ea2-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="55ea2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="55ea2-105">Syntax</span></span>


```C++
CSourceStream(
   TCHAR   *pObjectName,
   HRESULT *phr,
   CSource *pms,
   LPCWSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="55ea2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="55ea2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55ea2-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="55ea2-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="55ea2-108">Zeiger auf eine Zeichenfolge, die den Debugnamen des Pins enthält.</span><span class="sxs-lookup"><span data-stu-id="55ea2-108">Pointer to a string containing the debug name of the pin.</span></span>

</dd> <dt>

<span data-ttu-id="55ea2-109">*Phr*</span><span class="sxs-lookup"><span data-stu-id="55ea2-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="55ea2-110">Zeiger auf eine Variable, die einen **HRESULT-Wert** empfängt, der den Erfolg oder Fehler der Methode angibt.</span><span class="sxs-lookup"><span data-stu-id="55ea2-110">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="55ea2-111">Initialisieren Sie den Wert vor dem Erstellen des -Objekts mit S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="55ea2-111">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="55ea2-112">Der Wert wird nur geändert, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="55ea2-112">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="55ea2-113">*Pms*</span><span class="sxs-lookup"><span data-stu-id="55ea2-113">*pms*</span></span> 
</dt> <dd>

<span data-ttu-id="55ea2-114">Zeiger auf den [**CSource-Filter,**](csource.md) der diese Stecknadel erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="55ea2-114">Pointer to the [**CSource**](csource.md) filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="55ea2-115">*pName*</span><span class="sxs-lookup"><span data-stu-id="55ea2-115">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="55ea2-116">Zeiger auf eine Zeichenfolge, die den Namen der Stecknadel enthält.</span><span class="sxs-lookup"><span data-stu-id="55ea2-116">Pointer to a string that contains the name of the pin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55ea2-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55ea2-117">Remarks</span></span>

<span data-ttu-id="55ea2-118">Die im *pObjectName-Parameter* angegebene Zeichenfolge wird nur zu Debugzwecken verwendet.</span><span class="sxs-lookup"><span data-stu-id="55ea2-118">The string given in the *pObjectName* parameter is used only for debugging purposes.</span></span> <span data-ttu-id="55ea2-119">Weitere Informationen finden Sie unter [**CBaseObject.**](cbaseobject.md)</span><span class="sxs-lookup"><span data-stu-id="55ea2-119">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

<span data-ttu-id="55ea2-120">Die im *pName-Parameter* angegebene Zeichenfolge ist der Name, der von der [**IPin::QueryPinInfo-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="55ea2-120">The string given in the *pName* parameter is the name returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="55ea2-121">Die `CSourceStream` -Klasse verwendet diesen Namen nicht für den pin-Bezeichner, der von der [**CSourceStream::QueryId-Methode**](csourcestream-queryid.md) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="55ea2-121">The `CSourceStream` class does not use this name for the pin identifier returned by the [**CSourceStream::QueryId**](csourcestream-queryid.md) method.</span></span> <span data-ttu-id="55ea2-122">Stattdessen berechnet **QueryId** einen Pinbezeichner basierend auf der Pinnummer.</span><span class="sxs-lookup"><span data-stu-id="55ea2-122">Instead, **QueryId** calculates a pin identifier based on the pin number.</span></span> <span data-ttu-id="55ea2-123">(Stecknadelbezeichner unterstützen die Graphpersistenz.</span><span class="sxs-lookup"><span data-stu-id="55ea2-123">(Pin identifiers support graph persistence.</span></span> <span data-ttu-id="55ea2-124">Weitere Informationen finden Sie unter [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).)</span><span class="sxs-lookup"><span data-stu-id="55ea2-124">For more information, see [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).)</span></span>

<span data-ttu-id="55ea2-125">Der Konstruktor fügt den Pin automatisch dem besitzenden Filter hinzu, indem er [**CSource::AddPin aufruft.**](csource-addpin.md)</span><span class="sxs-lookup"><span data-stu-id="55ea2-125">The constructor automatically adds the pin to the owning filter, by calling [**CSource::AddPin**](csource-addpin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55ea2-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55ea2-126">Requirements</span></span>



| <span data-ttu-id="55ea2-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55ea2-127">Requirement</span></span> | <span data-ttu-id="55ea2-128">Wert</span><span class="sxs-lookup"><span data-stu-id="55ea2-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55ea2-129">Header</span><span class="sxs-lookup"><span data-stu-id="55ea2-129">Header</span></span><br/>  | <dl> <span data-ttu-id="55ea2-130"><dt>Source.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="55ea2-130"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="55ea2-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="55ea2-131">Library</span></span><br/> | <dl> <span data-ttu-id="55ea2-132"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="55ea2-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55ea2-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="55ea2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55ea2-134">**CSourceStream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="55ea2-134">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




