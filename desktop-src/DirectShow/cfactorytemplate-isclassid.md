---
description: Die isclassid-Methode bestimmt, ob eine CLSID mit dieser Klassen Vorlage übereinstimmt.
ms.assetid: de560f7a-2ccb-44e2-ac32-3b0fea0d80b8
title: Cfactorytemplate. isclassid-Methode (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.IsClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94564d7e9db52f8be22717a10f73fffb7fb6fa14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367678"
---
# <a name="cfactorytemplateisclassid-method"></a><span data-ttu-id="2277b-103">Cfactorytemplate. isclassid-Methode</span><span class="sxs-lookup"><span data-stu-id="2277b-103">CFactoryTemplate.IsClassID method</span></span>

<span data-ttu-id="2277b-104">Die- `IsClassID` Methode bestimmt, ob eine CLSID mit dieser Klassen Vorlage übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="2277b-104">The `IsClassID` method determines whether a CLSID matches this class template.</span></span>

## <a name="syntax"></a><span data-ttu-id="2277b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2277b-105">Syntax</span></span>


```C++
BOOL IsClassID(
   REFCLSID rclsid
);
```



## <a name="parameters"></a><span data-ttu-id="2277b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2277b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2277b-107">*rclsid*</span><span class="sxs-lookup"><span data-stu-id="2277b-107">*rclsid*</span></span> 
</dt> <dd>

<span data-ttu-id="2277b-108">Verweis auf eine CLSID.</span><span class="sxs-lookup"><span data-stu-id="2277b-108">Reference to a CLSID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2277b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2277b-109">Return value</span></span>

<span data-ttu-id="2277b-110">Gibt " **true** " zurück, wenn der *rclsid* -Parameter dieselbe CLSID wie die CLSID-Element Variable " [**\_ cfactorytemplate:: m**](cfactorytemplate-m-clsid.md) " ist, andernfalls wird " **false**" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2277b-110">Returns **TRUE** if the *rclsid* parameter is the same CLSID as the [**CFactoryTemplate::m\_ClsID**](cfactorytemplate-m-clsid.md) member variable, or else returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2277b-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2277b-111">Requirements</span></span>



| <span data-ttu-id="2277b-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2277b-112">Requirement</span></span> | <span data-ttu-id="2277b-113">Wert</span><span class="sxs-lookup"><span data-stu-id="2277b-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2277b-114">Header</span><span class="sxs-lookup"><span data-stu-id="2277b-114">Header</span></span><br/>  | <dl> <span data-ttu-id="2277b-115"><dt>ComBase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2277b-115"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2277b-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2277b-116">Library</span></span><br/> | <dl> <span data-ttu-id="2277b-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2277b-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2277b-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2277b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2277b-119">**Cfactorytemplate-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2277b-119">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




