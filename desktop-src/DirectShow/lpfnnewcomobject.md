---
description: 'LPFNNewCOMObject-Funktionszeiger: Zeiger auf eine Funktion, die eine Instanz des -Objekts erstellt.'
ms.assetid: 8c9dab82-a080-4733-8c62-d090b28306e0
title: LPFNNewCOMObject-Funktionszeiger (Combase.h)
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
ms.openlocfilehash: f3ea5bc172bc22f7aa9dce1f348bba552520565f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116528"
---
# <a name="lpfnnewcomobject-function-pointer"></a><span data-ttu-id="14938-103">LPFNNewCOMObject-Funktionszeiger</span><span class="sxs-lookup"><span data-stu-id="14938-103">LPFNNewCOMObject function pointer</span></span>

<span data-ttu-id="14938-104">Zeiger auf eine Funktion, die eine Instanz des -Objekts erstellt.</span><span class="sxs-lookup"><span data-stu-id="14938-104">Pointer to a function that creates an instance of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="14938-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="14938-105">Syntax</span></span>


```C++
typedef CUnknown* ( CALLBACK *LPFNNewCOMObject)(
   LPUNKNOWN pUnkOuter,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="14938-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="14938-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14938-107">*pUnkOuter*</span><span class="sxs-lookup"><span data-stu-id="14938-107">*pUnkOuter*</span></span> 
</dt> <dd>

<span data-ttu-id="14938-108">Zeiger auf die **IUnknown-Schnittstelle** des Objekts, das das neue Objekt aggregiert, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="14938-108">Pointer to the **IUnknown** interface of the object that aggregates the new object, if any.</span></span> <span data-ttu-id="14938-109">Dieser Zeiger kann NULL **sein.**</span><span class="sxs-lookup"><span data-stu-id="14938-109">This pointer can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="14938-110">*Phr*</span><span class="sxs-lookup"><span data-stu-id="14938-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="14938-111">Zeiger auf einen **HRESULT-Wert.**</span><span class="sxs-lookup"><span data-stu-id="14938-111">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="14938-112">Wenn der Konstruktor fehlschlägt, empfängt dieser Parameter einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="14938-112">If the constructor fails, this parameter receives an error code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14938-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14938-113">Return value</span></span>

<span data-ttu-id="14938-114">Gibt einen Zeiger auf eine neue Instanz des -Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="14938-114">Returns a pointer to a new instance of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="14938-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14938-115">Requirements</span></span>



| <span data-ttu-id="14938-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14938-116">Requirement</span></span> | <span data-ttu-id="14938-117">Wert</span><span class="sxs-lookup"><span data-stu-id="14938-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14938-118">Header</span><span class="sxs-lookup"><span data-stu-id="14938-118">Header</span></span><br/> | <dl> <span data-ttu-id="14938-119"><dt>Combase.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="14938-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14938-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="14938-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14938-121">**CFactoryTemplate-Klasse**</span><span class="sxs-lookup"><span data-stu-id="14938-121">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




