---
description: CBasePropertyPage.CBasePropertyPage-Konstruktor – Konstruktormethode.
ms.assetid: 5d9863e7-fdd9-4df2-a603-34a240a2286c
title: CBasePropertyPage.CBasePropertyPage-Konstruktor (Cprop.h)
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
ms.openlocfilehash: 95821062b6b1199ea98a5329934d76e2197901d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119948"
---
# <a name="cbasepropertypagecbasepropertypage-constructor"></a><span data-ttu-id="eb2a4-103">CBasePropertyPage.CBasePropertyPage-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="eb2a4-103">CBasePropertyPage.CBasePropertyPage constructor</span></span>

<span data-ttu-id="eb2a4-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb2a4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb2a4-105">Syntax</span></span>


```C++
CBasePropertyPage(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   int       DialogId,
   int       TitleId
);
```



## <a name="parameters"></a><span data-ttu-id="eb2a4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb2a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb2a4-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="eb2a4-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="eb2a4-108">Zeichenfolge, die den Namen des Objekts zu Debugzwecken enthält.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-108">String that contains the name of the object, for debugging purposes.</span></span> <span data-ttu-id="eb2a4-109">Weitere Informationen finden Sie unter [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="eb2a4-109">For more information, see [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb2a4-110">*Punk*</span><span class="sxs-lookup"><span data-stu-id="eb2a4-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="eb2a4-111">Zeiger auf die aggregierende **IUnknown-Schnittstelle.**</span><span class="sxs-lookup"><span data-stu-id="eb2a4-111">Pointer to the aggregating **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="eb2a4-112">*DialogId*</span><span class="sxs-lookup"><span data-stu-id="eb2a4-112">*DialogId*</span></span> 
</dt> <dd>

<span data-ttu-id="eb2a4-113">Ressourcen-ID für das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-113">Resource ID for the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="eb2a4-114">*TitleId*</span><span class="sxs-lookup"><span data-stu-id="eb2a4-114">*TitleId*</span></span> 
</dt> <dd>

<span data-ttu-id="eb2a4-115">Ressourcen-ID für die Zeichenfolge, die den Titel des Dialogfelds enthält.</span><span class="sxs-lookup"><span data-stu-id="eb2a4-115">Resource ID for the string that contains the dialog box title.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="eb2a4-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb2a4-116">Examples</span></span>


```C++
CMyProp::CMyProp(IUnknown *pUnk) : 
    CBasePropertyPage(NAME("MyPropPage"), pUnk, IDD_PROPPAGE, IDS_TITLE),
```



## <a name="requirements"></a><span data-ttu-id="eb2a4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb2a4-117">Requirements</span></span>



| <span data-ttu-id="eb2a4-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb2a4-118">Requirement</span></span> | <span data-ttu-id="eb2a4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="eb2a4-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb2a4-120">Header</span><span class="sxs-lookup"><span data-stu-id="eb2a4-120">Header</span></span><br/>  | <dl> <span data-ttu-id="eb2a4-121"><dt>Cprop.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb2a4-121"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="eb2a4-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eb2a4-122">Library</span></span><br/> | <dl> <span data-ttu-id="eb2a4-123"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="eb2a4-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb2a4-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="eb2a4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb2a4-125">**CBasePropertyPage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="eb2a4-125">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




