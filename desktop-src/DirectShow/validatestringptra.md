---
description: Überprüft, ob der aufrufende Prozess über Lesezugriff auf eine ANSI-Zeichenfolge verfügt. Andernfalls ruft das Makro das dbgbreak-Makro auf.
ms.assetid: 44be67f8-9896-4360-82de-083a5f28a3d0
title: Validatestringptra-Makro (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateStringPtrA
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 94ce34393ec494f34cce621afc168a4d6bbe4325
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364479"
---
# <a name="validatestringptra-macro"></a><span data-ttu-id="41cf0-104">Validatestringptra-Makro</span><span class="sxs-lookup"><span data-stu-id="41cf0-104">ValidateStringPtrA macro</span></span>

<span data-ttu-id="41cf0-105">Überprüft, ob der aufrufende Prozess über Lesezugriff auf eine ANSI-Zeichenfolge verfügt.</span><span class="sxs-lookup"><span data-stu-id="41cf0-105">Verifies that the calling process has read access to an ANSI string.</span></span> <span data-ttu-id="41cf0-106">Andernfalls ruft das Makro das [**dbgbreak**](dbgbreak.md) -Makro auf.</span><span class="sxs-lookup"><span data-stu-id="41cf0-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="41cf0-107">Dieses Makro ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="41cf0-107">This macro is deprecated.</span></span> <span data-ttu-id="41cf0-108">Im Windows SDK für Windows Vista (und höher) führt dieses Makro nichts aus.</span><span class="sxs-lookup"><span data-stu-id="41cf0-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="41cf0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="41cf0-109">Syntax</span></span>


```C++
void ValidateStringPtrA(
   LPCSTR p
);
```



## <a name="parameters"></a><span data-ttu-id="41cf0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="41cf0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41cf0-111">*cker*</span><span class="sxs-lookup"><span data-stu-id="41cf0-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="41cf0-112">Zeiger auf eine mit NULL endende ANSI-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="41cf0-112">Pointer to a NULL-terminated ANSI string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41cf0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41cf0-113">Return value</span></span>

<span data-ttu-id="41cf0-114">Dieses Makro gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="41cf0-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="41cf0-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41cf0-115">Remarks</span></span>

<span data-ttu-id="41cf0-116">Dieses Makro wird ignoriert, es sei denn, Debug, \_ Debug oder vfwrobust wird definiert, wenn die DirectShow-Basisklassen-Header Datei eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="41cf0-116">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span>

## <a name="requirements"></a><span data-ttu-id="41cf0-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41cf0-117">Requirements</span></span>



| <span data-ttu-id="41cf0-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41cf0-118">Requirement</span></span> | <span data-ttu-id="41cf0-119">Wert</span><span class="sxs-lookup"><span data-stu-id="41cf0-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41cf0-120">Header</span><span class="sxs-lookup"><span data-stu-id="41cf0-120">Header</span></span><br/> | <dl> <span data-ttu-id="41cf0-121"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="41cf0-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41cf0-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41cf0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41cf0-123">Zeiger Validierungs Makros</span><span class="sxs-lookup"><span data-stu-id="41cf0-123">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




