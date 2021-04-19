---
description: Ein Zeiger auf eine Funktion, die eine Instanz des-Objekts erstellt.
ms.assetid: 86859bf9-e16a-4494-bf1b-1d8ddbc1c805
title: 'Cfactoriytemplate:: m_lpfnNew Member (ComBase. h)'
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
ms.openlocfilehash: 2299f7a87f348ac8a5fa6c6d83b6a17fbf97ca28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359641"
---
# <a name="cfactorytemplatem_lpfnnew-member"></a><span data-ttu-id="8d5c3-103">Cfactor ytemplate:: m \_ lpfnnew-Member</span><span class="sxs-lookup"><span data-stu-id="8d5c3-103">CFactoryTemplate::m\_lpfnNew member</span></span>

<span data-ttu-id="8d5c3-104">Ein Zeiger auf eine Funktion, die eine Instanz des-Objekts erstellt.</span><span class="sxs-lookup"><span data-stu-id="8d5c3-104">Pointer to a function that creates an instance of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d5c3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d5c3-105">Syntax</span></span>


```C++
LPFNNewCOMObject m_lpfnNew;
```



## <a name="remarks"></a><span data-ttu-id="8d5c3-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d5c3-106">Remarks</span></span>

<span data-ttu-id="8d5c3-107">Deklarieren Sie in der DLL eine statische Funktion, die einen Zeiger auf eine neue Instanz des-Objekts zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8d5c3-107">In your DLL, declare a static function that returns a pointer to a new instance of the object.</span></span> <span data-ttu-id="8d5c3-108">Legen Sie in der Factory-Vorlage die **m \_ lpfnnew** -Member-Variable auf die Adresse dieser statischen Funktion fest.</span><span class="sxs-lookup"><span data-stu-id="8d5c3-108">In the factory template, set the **m\_lpfnNew** member variable to the address of this static function.</span></span>

<span data-ttu-id="8d5c3-109">Der Funktions Zeigertyp ist " [**lpfnnewcomobject**](lpfnnewcomobject.md)".</span><span class="sxs-lookup"><span data-stu-id="8d5c3-109">The function pointer type is [**LPFNNewCOMObject**](lpfnnewcomobject.md).</span></span>

<span data-ttu-id="8d5c3-110">Das folgende Beispiel zeigt eine typische Funktion für **m \_ lpfnnew**:</span><span class="sxs-lookup"><span data-stu-id="8d5c3-110">The following example shows a typical function for **m\_lpfnNew**:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="8d5c3-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d5c3-111">Requirements</span></span>



| <span data-ttu-id="8d5c3-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d5c3-112">Requirement</span></span> | <span data-ttu-id="8d5c3-113">Wert</span><span class="sxs-lookup"><span data-stu-id="8d5c3-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d5c3-114">Header</span><span class="sxs-lookup"><span data-stu-id="8d5c3-114">Header</span></span><br/>  | <dl> <span data-ttu-id="8d5c3-115"><dt>ComBase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8d5c3-115"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8d5c3-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8d5c3-116">Library</span></span><br/> | <dl> <span data-ttu-id="8d5c3-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8d5c3-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d5c3-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d5c3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d5c3-119">**Cfactorytemplate-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8d5c3-119">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




