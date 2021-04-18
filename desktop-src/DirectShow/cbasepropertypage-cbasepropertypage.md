---
description: Konstruktormethode.
ms.assetid: 5d9863e7-fdd9-4df2-a603-34a240a2286c
title: Cbasepropertypage. cbasepropertypage-Konstruktor (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 915bc42cfb7f152cc061dab76caede6c998edf8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359224"
---
# <a name="cbasepropertypagecbasepropertypage-constructor"></a><span data-ttu-id="aff29-103">Cbasepropertypage. cbasepropertypage-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="aff29-103">CBasePropertyPage.CBasePropertyPage constructor</span></span>

<span data-ttu-id="aff29-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="aff29-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="aff29-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aff29-105">Syntax</span></span>


```C++
CBasePropertyPage(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   int       DialogId,
   int       TitleId
);
```



## <a name="parameters"></a><span data-ttu-id="aff29-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aff29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aff29-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="aff29-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="aff29-108">Eine Zeichenfolge, die den Namen des Objekts zu Debuggingzwecken enthält.</span><span class="sxs-lookup"><span data-stu-id="aff29-108">String that contains the name of the object, for debugging purposes.</span></span> <span data-ttu-id="aff29-109">Weitere Informationen finden Sie unter [**cbaseobject:: cbaseobject**](cbaseobject-cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="aff29-109">For more information, see [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="aff29-110">*Kro*</span><span class="sxs-lookup"><span data-stu-id="aff29-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="aff29-111">Zeiger auf die Aggregations- **IUnknown** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="aff29-111">Pointer to the aggregating **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="aff29-112">*DialogID*</span><span class="sxs-lookup"><span data-stu-id="aff29-112">*DialogId*</span></span> 
</dt> <dd>

<span data-ttu-id="aff29-113">Die Ressourcen-ID für das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="aff29-113">Resource ID for the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="aff29-114">*TitleId*</span><span class="sxs-lookup"><span data-stu-id="aff29-114">*TitleId*</span></span> 
</dt> <dd>

<span data-ttu-id="aff29-115">Die Ressourcen-ID für die Zeichenfolge, die den Dialogfeld Titel enthält.</span><span class="sxs-lookup"><span data-stu-id="aff29-115">Resource ID for the string that contains the dialog box title.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="aff29-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aff29-116">Examples</span></span>


```C++
CMyProp::CMyProp(IUnknown *pUnk) : 
    CBasePropertyPage(NAME("MyPropPage"), pUnk, IDD_PROPPAGE, IDS_TITLE),
```



## <a name="requirements"></a><span data-ttu-id="aff29-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aff29-117">Requirements</span></span>



| <span data-ttu-id="aff29-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aff29-118">Requirement</span></span> | <span data-ttu-id="aff29-119">Wert</span><span class="sxs-lookup"><span data-stu-id="aff29-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aff29-120">Header</span><span class="sxs-lookup"><span data-stu-id="aff29-120">Header</span></span><br/>  | <dl> <span data-ttu-id="aff29-121"><dt>Cprop. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aff29-121"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="aff29-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="aff29-122">Library</span></span><br/> | <dl> <span data-ttu-id="aff29-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="aff29-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aff29-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aff29-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aff29-125">**Cbasepropertypage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="aff29-125">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




