---
description: Ein Zeiger auf eine Funktion, die eine Instanz des-Objekts erstellt.
ms.assetid: 8c9dab82-a080-4733-8c62-d090b28306e0
title: Lpfnnewcomobject-Funktionszeiger (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNNewCOMObject
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: 07c0f8ab961c872c9dc0f92d2fff519b94cd049e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367701"
---
# <a name="lpfnnewcomobject-function-pointer"></a><span data-ttu-id="17272-103">Lpfnnewcomobject-Funktionszeiger</span><span class="sxs-lookup"><span data-stu-id="17272-103">LPFNNewCOMObject function pointer</span></span>

<span data-ttu-id="17272-104">Ein Zeiger auf eine Funktion, die eine Instanz des-Objekts erstellt.</span><span class="sxs-lookup"><span data-stu-id="17272-104">Pointer to a function that creates an instance of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="17272-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="17272-105">Syntax</span></span>


```C++
typedef CUnknown* ( CALLBACK *LPFNNewCOMObject)(
   LPUNKNOWN pUnkOuter,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="17272-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="17272-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17272-107">*pUnkOuter*</span><span class="sxs-lookup"><span data-stu-id="17272-107">*pUnkOuter*</span></span> 
</dt> <dd>

<span data-ttu-id="17272-108">Ein Zeiger auf die **IUnknown** -Schnittstelle des Objekts, das das neue Objekt aggregiert, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="17272-108">Pointer to the **IUnknown** interface of the object that aggregates the new object, if any.</span></span> <span data-ttu-id="17272-109">Dieser Zeiger kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="17272-109">This pointer can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="17272-110">*PHR*</span><span class="sxs-lookup"><span data-stu-id="17272-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="17272-111">Zeiger auf einen **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="17272-111">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="17272-112">Wenn der Konstruktor ausfällt, empfängt dieser Parameter einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="17272-112">If the constructor fails, this parameter receives an error code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17272-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17272-113">Return value</span></span>

<span data-ttu-id="17272-114">Gibt einen Zeiger auf eine neue Instanz des-Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="17272-114">Returns a pointer to a new instance of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="17272-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17272-115">Requirements</span></span>



| <span data-ttu-id="17272-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17272-116">Requirement</span></span> | <span data-ttu-id="17272-117">Wert</span><span class="sxs-lookup"><span data-stu-id="17272-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17272-118">Header</span><span class="sxs-lookup"><span data-stu-id="17272-118">Header</span></span><br/> | <dl> <span data-ttu-id="17272-119"><dt>ComBase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="17272-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17272-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17272-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17272-121">**Cfactorytemplate-Klasse**</span><span class="sxs-lookup"><span data-stu-id="17272-121">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




