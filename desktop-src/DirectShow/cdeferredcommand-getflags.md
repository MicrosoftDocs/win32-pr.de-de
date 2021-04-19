---
description: Die GetFlags-Methode ruft die dem verzögerten Befehl zugeordneten kontextflags ab.
ms.assetid: 3a96299a-b157-419b-a23e-86241e10566f
title: Cdeferredcommand. GetFlags-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetFlags
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aec9b97e42534d34c5033b3b86edb9c33366d639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367205"
---
# <a name="cdeferredcommandgetflags-method"></a><span data-ttu-id="c50ac-103">Cdeferredcommand. GetFlags-Methode</span><span class="sxs-lookup"><span data-stu-id="c50ac-103">CDeferredCommand.GetFlags method</span></span>

<span data-ttu-id="c50ac-104">Die- `GetFlags` Methode ruft die dem verzögerten Befehl zugeordneten kontexflags ab.</span><span class="sxs-lookup"><span data-stu-id="c50ac-104">The `GetFlags` method retrieves the context flags associated with the deferred command.</span></span>

## <a name="syntax"></a><span data-ttu-id="c50ac-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c50ac-105">Syntax</span></span>


```C++
short GetFlags();
```



## <a name="parameters"></a><span data-ttu-id="c50ac-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c50ac-106">Parameters</span></span>

<span data-ttu-id="c50ac-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c50ac-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c50ac-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c50ac-108">Return value</span></span>

<span data-ttu-id="c50ac-109">Gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="c50ac-109">Returns one of the following:</span></span>



| <span data-ttu-id="c50ac-110">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c50ac-110">Return code</span></span>                                                                                             | <span data-ttu-id="c50ac-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c50ac-111">Description</span></span>                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c50ac-112"><dt>**Dispatch- \_ Methode**</dt></span><span class="sxs-lookup"><span data-stu-id="c50ac-112"><dt>**DISPATCH\_METHOD**</dt></span></span> </dl>         | <span data-ttu-id="c50ac-113">Führen Sie den Member als Methode aus.</span><span class="sxs-lookup"><span data-stu-id="c50ac-113">Run the member as a method.</span></span> <span data-ttu-id="c50ac-114">Wenn eine Eigenschaft denselben Namen hat, können sowohl dieses als auch das Dispatch \_ PropertyGet-Flag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c50ac-114">If a property has the same name, both this and the DISPATCH\_PROPERTYGET flag can be set.</span></span><br/>                                               |
| <dl> <span data-ttu-id="c50ac-115"><dt>**Dispatch- \_ PropertyGet**</dt></span><span class="sxs-lookup"><span data-stu-id="c50ac-115"><dt>**DISPATCH\_PROPERTYGET**</dt></span></span> </dl>    | <span data-ttu-id="c50ac-116">Der Member wird als Eigenschaft oder Datenmember abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c50ac-116">The member is being retrieved as a property or data member.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="c50ac-117"><dt>**Dispatch- \_ PropertyPut**</dt></span><span class="sxs-lookup"><span data-stu-id="c50ac-117"><dt>**DISPATCH\_PROPERTYPUT**</dt></span></span> </dl>    | <span data-ttu-id="c50ac-118">Der Member wird als Eigenschaft oder Datenmember geändert.</span><span class="sxs-lookup"><span data-stu-id="c50ac-118">The member is being changed as a property or data member.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="c50ac-119"><dt>**Dispatch \_ propertyputref**</dt></span><span class="sxs-lookup"><span data-stu-id="c50ac-119"><dt>**DISPATCH\_PROPERTYPUTREF**</dt></span></span> </dl> | <span data-ttu-id="c50ac-120">Der Member wird über eine Verweis Zuweisung und nicht über eine Wert Zuweisung geändert.</span><span class="sxs-lookup"><span data-stu-id="c50ac-120">The member is being changed via a reference assignment, rather than a value assignment.</span></span> <span data-ttu-id="c50ac-121">Dieses Flag ist nur gültig, wenn die-Eigenschaft einen Verweis auf ein-Objekt akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="c50ac-121">This flag is valid only when the property accepts a reference to an object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c50ac-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c50ac-122">Requirements</span></span>



| <span data-ttu-id="c50ac-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c50ac-123">Requirement</span></span> | <span data-ttu-id="c50ac-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c50ac-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c50ac-125">Header</span><span class="sxs-lookup"><span data-stu-id="c50ac-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c50ac-126"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c50ac-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c50ac-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c50ac-127">Library</span></span><br/> | <dl> <span data-ttu-id="c50ac-128">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c50ac-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c50ac-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c50ac-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c50ac-130">**Cdeferredcommand-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c50ac-130">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




