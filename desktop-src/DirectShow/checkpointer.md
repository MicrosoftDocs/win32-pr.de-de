---
description: Überprüft, ob ein Zeiger NULL ist. Wenn der Zeiger NULL ist, gibt die Funktion oder Methode, in der das Makro angezeigt wird, den angegebenen Wert zurück.
ms.assetid: eca73fbf-5fd8-4b76-af06-ca0c22510b55
title: Check Pointer-Makro (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckPointer
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 04f442303e520ef758a3576d21c2df810ef26fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372135"
---
# <a name="checkpointer-macro"></a><span data-ttu-id="c06b1-104">Check Pointer-Makro</span><span class="sxs-lookup"><span data-stu-id="c06b1-104">CheckPointer macro</span></span>

<span data-ttu-id="c06b1-105">Überprüft, ob ein Zeiger **null** ist.</span><span class="sxs-lookup"><span data-stu-id="c06b1-105">Checks whether a pointer is **NULL**.</span></span> <span data-ttu-id="c06b1-106">Wenn der Zeiger **null** ist, gibt die Funktion oder Methode, in der das Makro angezeigt wird, den angegebenen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c06b1-106">If the pointer is **NULL**, the function or method in which the macro appears returns the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c06b1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c06b1-107">Syntax</span></span>


```C++
HRESULT CheckPointer(
    p,
    ret
);
```



## <a name="parameters"></a><span data-ttu-id="c06b1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c06b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c06b1-109">*cker*</span><span class="sxs-lookup"><span data-stu-id="c06b1-109">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="c06b1-110">Der zu Überprüfung Ende Zeiger.</span><span class="sxs-lookup"><span data-stu-id="c06b1-110">Pointer to check.</span></span>

</dd> <dt>

<span data-ttu-id="c06b1-111">*TZI*</span><span class="sxs-lookup"><span data-stu-id="c06b1-111">*ret*</span></span> 
</dt> <dd>

<span data-ttu-id="c06b1-112">Der Wert, den die Funktion oder Methode zurückgibt, wenn *p* **null** ist.</span><span class="sxs-lookup"><span data-stu-id="c06b1-112">Value that the function or method returns if *p* is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c06b1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c06b1-113">Return value</span></span>

<span data-ttu-id="c06b1-114">Die umgebende Funktion gibt *ret* zurück, wenn *p* **null** ist.</span><span class="sxs-lookup"><span data-stu-id="c06b1-114">The surrounding function returns *ret* if *p* is **NULL**.</span></span> <span data-ttu-id="c06b1-115">Andernfalls bewirkt das Makro nicht, dass die umgebende Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c06b1-115">Otherwise, the macro does not cause the surrounding function to return.</span></span>

## <a name="examples"></a><span data-ttu-id="c06b1-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c06b1-116">Examples</span></span>


```
HRESULT MyFunction(VOID *pSomeParameter)
{
    // Return E_INVALIDARG if pSomeParameter is NULL.
    CheckPointer(pSomeParameter, E_INVALIDARG)

    // Rest of the function (not shown).
}
```



## <a name="requirements"></a><span data-ttu-id="c06b1-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c06b1-117">Requirements</span></span>



| <span data-ttu-id="c06b1-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c06b1-118">Requirement</span></span> | <span data-ttu-id="c06b1-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c06b1-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c06b1-120">Header</span><span class="sxs-lookup"><span data-stu-id="c06b1-120">Header</span></span><br/> | <dl> <span data-ttu-id="c06b1-121"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c06b1-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c06b1-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c06b1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c06b1-123">Zeiger Validierungs Makros</span><span class="sxs-lookup"><span data-stu-id="c06b1-123">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




