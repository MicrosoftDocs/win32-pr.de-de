---
description: Die LockIT-Klasse ist eine interne Klasse, die den DMO sperrt und entsperrt.
ms.assetid: f516ce22-17ad-488e-a768-3f3849c56087
title: 'Imediaobjectimpl:: LockIT-Klasse (dmuimpl. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24fe896ea293ec5e60b038f908cab794274d26e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356390"
---
# <a name="imediaobjectimpllockit-class"></a><span data-ttu-id="58d12-103">Imediaobjectimpl:: LockIT-Klasse</span><span class="sxs-lookup"><span data-stu-id="58d12-103">IMediaObjectImpl::LockIt Class</span></span>

<span data-ttu-id="58d12-104">Bei der `LockIt` -Klasse handelt es sich um eine interne Klasse, die den DMO sperrt und entsperrt.</span><span class="sxs-lookup"><span data-stu-id="58d12-104">The `LockIt` class is an internal class that locks and unlocks the DMO.</span></span>

``` syntax
LockIt(
    _DERIVED_ *p
);
```

## <a name="parameters"></a><span data-ttu-id="58d12-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="58d12-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58d12-106"><span id="p"></span><span id="P"></span>*cker*</span><span class="sxs-lookup"><span data-stu-id="58d12-106"><span id="p"></span><span id="P"></span>*p*</span></span>
</dt> <dd>

<span data-ttu-id="58d12-107">Zeiger auf das abgeleitete Objekt.</span><span class="sxs-lookup"><span data-stu-id="58d12-107">Pointer to the derived object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58d12-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58d12-108">Remarks</span></span>

<span data-ttu-id="58d12-109">Der `LockIt` Konstruktor sperrt den DMO, und der Dekonstruktor entsperrt den DMO.</span><span class="sxs-lookup"><span data-stu-id="58d12-109">The `LockIt` constructor locks the DMO, and the destructor unlocks the DMO.</span></span> <span data-ttu-id="58d12-110">Um das Objekt in der abgeleiteten Klasse zu sperren, deklarieren Sie eine lokale Variable vom Typ `LockIt` .</span><span class="sxs-lookup"><span data-stu-id="58d12-110">To lock the object from inside your derived class, declare a local variable of type `LockIt`.</span></span> <span data-ttu-id="58d12-111">Der DMO ist gesperrt, während das `LockIt` Objekt im Gültigkeitsbereich bleibt:</span><span class="sxs-lookup"><span data-stu-id="58d12-111">The DMO is locked while the `LockIt` object remains in scope:</span></span>


```C++
void SomeMethod()
{
    // The DMO is not locked.
    {
        LockIt dmoLock(this); // Locks the DMO.
        /* ... */
    } 
    // dmoLock goes out of scope, DMO is unlocked.
}
```



<span data-ttu-id="58d12-112">Die Methoden in **imediaobjectimpl** sperren den DMO automatisch.</span><span class="sxs-lookup"><span data-stu-id="58d12-112">The methods in **IMediaObjectImpl** automatically lock the DMO.</span></span>

## <a name="requirements"></a><span data-ttu-id="58d12-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58d12-113">Requirements</span></span>



| <span data-ttu-id="58d12-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58d12-114">Requirement</span></span> | <span data-ttu-id="58d12-115">Wert</span><span class="sxs-lookup"><span data-stu-id="58d12-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58d12-116">Header</span><span class="sxs-lookup"><span data-stu-id="58d12-116">Header</span></span><br/>  | <dl> <span data-ttu-id="58d12-117"><dt>Dmuimpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="58d12-117"><dt>Dmoimpl.h</dt></span></span> </dl>                                                                     |
| <span data-ttu-id="58d12-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="58d12-118">Library</span></span><br/> | <dl> <span data-ttu-id="58d12-119"><dt>Dmuguids. lib; </dt> <dt>Msdmo. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58d12-119"><dt>Dmoguids.lib; </dt> <dt>Msdmo.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58d12-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58d12-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58d12-121">**Imediaobjectimpl-Klassen Vorlage**</span><span class="sxs-lookup"><span data-stu-id="58d12-121">**IMediaObjectImpl Class Template**</span></span>](imediaobjectimpl-class-template.md)
</dt> </dl>

 

 




