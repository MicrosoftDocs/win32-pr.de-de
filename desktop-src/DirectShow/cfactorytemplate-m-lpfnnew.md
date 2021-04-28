---
description: 'CFactoryTemplate::m_lpfnNew Member : Zeiger auf eine Funktion, die eine Instanz des -Objekts erstellt.'
ms.assetid: 86859bf9-e16a-4494-bf1b-1d8ddbc1c805
title: CFactoryTemplate::m_lpfnNew Member (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnNew
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee4ec8e1503d3b260e025d154624b2d7c09bb49b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095648"
---
# <a name="cfactorytemplatem_lpfnnew-member"></a><span data-ttu-id="13beb-103">CFactoryTemplate::m \_ lpfnNew-Member</span><span class="sxs-lookup"><span data-stu-id="13beb-103">CFactoryTemplate::m\_lpfnNew member</span></span>

<span data-ttu-id="13beb-104">Zeiger auf eine Funktion, die eine Instanz des -Objekts erstellt.</span><span class="sxs-lookup"><span data-stu-id="13beb-104">Pointer to a function that creates an instance of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="13beb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="13beb-105">Syntax</span></span>


```C++
LPFNNewCOMObject m_lpfnNew;
```



## <a name="remarks"></a><span data-ttu-id="13beb-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13beb-106">Remarks</span></span>

<span data-ttu-id="13beb-107">Deklarieren Sie in Ihrer DLL eine statische Funktion, die einen Zeiger auf eine neue Instanz des -Objekts zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="13beb-107">In your DLL, declare a static function that returns a pointer to a new instance of the object.</span></span> <span data-ttu-id="13beb-108">Legen Sie in der Factoryvorlage die **Membervariable m \_ lpfnNew** auf die Adresse dieser statischen Funktion fest.</span><span class="sxs-lookup"><span data-stu-id="13beb-108">In the factory template, set the **m\_lpfnNew** member variable to the address of this static function.</span></span>

<span data-ttu-id="13beb-109">Der Funktionszeigertyp ist [**LPFNNewCOMObject.**](lpfnnewcomobject.md)</span><span class="sxs-lookup"><span data-stu-id="13beb-109">The function pointer type is [**LPFNNewCOMObject**](lpfnnewcomobject.md).</span></span>

<span data-ttu-id="13beb-110">Das folgende Beispiel zeigt eine typische Funktion für **m \_ lpfnNew:**</span><span class="sxs-lookup"><span data-stu-id="13beb-110">The following example shows a typical function for **m\_lpfnNew**:</span></span>


```C++
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = 
        new CMyComponent(NAME("My Component"), pUnk, pHr );

    if (pNewObject == NULL)  
    {
        *phr = E_OUTOFMEMORY;
    }
    return pNewObject;
}
```



## <a name="requirements"></a><span data-ttu-id="13beb-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13beb-111">Requirements</span></span>



| <span data-ttu-id="13beb-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13beb-112">Requirement</span></span> | <span data-ttu-id="13beb-113">Wert</span><span class="sxs-lookup"><span data-stu-id="13beb-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13beb-114">Header</span><span class="sxs-lookup"><span data-stu-id="13beb-114">Header</span></span><br/>  | <dl> <span data-ttu-id="13beb-115"><dt>Combase.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="13beb-115"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="13beb-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="13beb-116">Library</span></span><br/> | <dl> <span data-ttu-id="13beb-117"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="13beb-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13beb-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="13beb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13beb-119">**CFactoryTemplate-Klasse**</span><span class="sxs-lookup"><span data-stu-id="13beb-119">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




