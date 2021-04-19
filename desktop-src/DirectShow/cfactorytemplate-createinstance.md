---
description: Die Methode "kreateinstance" Ruft die Objekt Erstellungs Funktion für die-Klasse auf.
ms.assetid: 8a7d5c56-867d-432d-a0c2-97b8e3cf8a69
title: Cfactorytemplate. kreateinstance-Methode (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0f67ba528943bc2a468419fc84db44359745d4a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355954"
---
# <a name="cfactorytemplatecreateinstance-method"></a><span data-ttu-id="ca667-103">Cfactorytemplate. kreateinstance-Methode</span><span class="sxs-lookup"><span data-stu-id="ca667-103">CFactoryTemplate.CreateInstance method</span></span>

<span data-ttu-id="ca667-104">Die `CreateInstance` -Methode ruft die Objekt Erstellungs Funktion für die-Klasse auf.</span><span class="sxs-lookup"><span data-stu-id="ca667-104">The `CreateInstance` method calls the object-creation function for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca667-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca667-105">Syntax</span></span>


```C++
CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="ca667-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca667-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca667-107">*Kro*</span><span class="sxs-lookup"><span data-stu-id="ca667-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="ca667-108">Zeiger auf die Aggregations- **IUnknown** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ca667-108">Pointer to the aggregating **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="ca667-109">*PHR*</span><span class="sxs-lookup"><span data-stu-id="ca667-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="ca667-110">Ein Zeiger auf eine Variable, die einen **HRESULT** -Wert empfängt, der angibt, ob die Methode erfolgreich war oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="ca667-110">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca667-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca667-111">Return value</span></span>

<span data-ttu-id="ca667-112">Gibt eine Instanz des-Klassen Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="ca667-112">Returns an instance of the class object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca667-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca667-113">Remarks</span></span>

<span data-ttu-id="ca667-114">Die **IClassFactory:: deateinstance** -Methode ruft diese Klassenmethode auf.</span><span class="sxs-lookup"><span data-stu-id="ca667-114">The **IClassFactory::CreateInstance** method calls this class method.</span></span> <span data-ttu-id="ca667-115">Diese Methode ruft die-Funktion auf, auf die von der [**cfactorytemplate:: m \_ lpfnnew**](cfactorytemplate-m-lpfnnew.md) -Member-Variable verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ca667-115">This method calls the function pointed to by the [**CFactoryTemplate::m\_lpfnNew**](cfactorytemplate-m-lpfnnew.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca667-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca667-116">Requirements</span></span>



| <span data-ttu-id="ca667-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca667-117">Requirement</span></span> | <span data-ttu-id="ca667-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ca667-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca667-119">Header</span><span class="sxs-lookup"><span data-stu-id="ca667-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ca667-120"><dt>ComBase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca667-120"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ca667-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ca667-121">Library</span></span><br/> | <dl> <span data-ttu-id="ca667-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ca667-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca667-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca667-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca667-124">**Cfactorytemplate-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ca667-124">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




