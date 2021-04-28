---
description: 'CBaseDispatch.GetTypeInfoCount-Methode: Die GetTypeInfoCount-Methode ruft die Anzahl der Typinformationsschnittstellen ab, die das Objekt bereitstellt.'
ms.assetid: e09e6f6c-6ac8-4ce1-8ce1-ee5374d54183
title: CBaseDispatch.GetTypeInfoCount-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 81e68c94420b3d7715845f8d6bd14e26b770b44f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099888"
---
# <a name="cbasedispatchgettypeinfocount-method"></a><span data-ttu-id="3c0d5-103">CBaseDispatch.GetTypeInfoCount-Methode</span><span class="sxs-lookup"><span data-stu-id="3c0d5-103">CBaseDispatch.GetTypeInfoCount method</span></span>

<span data-ttu-id="3c0d5-104">Die `GetTypeInfoCount` -Methode ruft die Anzahl der Typinformationsschnittstellen ab, die das -Objekt bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="3c0d5-104">The `GetTypeInfoCount` method retrieves the number of type information interfaces the object provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c0d5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c0d5-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="3c0d5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c0d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c0d5-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="3c0d5-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="3c0d5-108">Zeiger auf eine Variable, die die Anzahl der vom -Objekt bereitgestellten Typinformationsschnittstellen empfängt.</span><span class="sxs-lookup"><span data-stu-id="3c0d5-108">Pointer to a variable that receives the number of type-information interfaces provided by the object.</span></span> <span data-ttu-id="3c0d5-109">Wenn die Methode zurückgegeben wird, ist der Wert 1.</span><span class="sxs-lookup"><span data-stu-id="3c0d5-109">When the method returns, the value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c0d5-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c0d5-110">Return value</span></span>

<span data-ttu-id="3c0d5-111">Gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="3c0d5-111">Returns one of the following values.</span></span>



| <span data-ttu-id="3c0d5-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3c0d5-112">Return code</span></span>                                                                               | <span data-ttu-id="3c0d5-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c0d5-113">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="3c0d5-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3c0d5-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="3c0d5-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="3c0d5-115">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="3c0d5-116"><dt>**E \_ POINTER**</dt></span><span class="sxs-lookup"><span data-stu-id="3c0d5-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="3c0d5-117">**NULL-Zeigerargument.**</span><span class="sxs-lookup"><span data-stu-id="3c0d5-117">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3c0d5-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c0d5-118">Requirements</span></span>



| <span data-ttu-id="3c0d5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c0d5-119">Requirement</span></span> | <span data-ttu-id="3c0d5-120">Wert</span><span class="sxs-lookup"><span data-stu-id="3c0d5-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c0d5-121">Header</span><span class="sxs-lookup"><span data-stu-id="3c0d5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3c0d5-122"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c0d5-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3c0d5-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3c0d5-123">Library</span></span><br/> | <dl> <span data-ttu-id="3c0d5-124"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3c0d5-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c0d5-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3c0d5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c0d5-126">**CBaseDispatch-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3c0d5-126">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




