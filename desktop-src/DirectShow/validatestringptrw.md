---
description: Überprüft, ob der aufrufenden Prozess Lesezugriff auf eine breit Zeichen-Zeichenfolge hat. Andernfalls ruft das Makro das dbgbreak-Makro auf.
ms.assetid: 526e8027-31e5-428d-856d-9fc6698693c3
title: Validatestringptrw-Makro (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateStringPtrW
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 1ece2caa0f2263c038121cd1ffd031cbe42d336a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371348"
---
# <a name="validatestringptrw-macro"></a><span data-ttu-id="a9fbe-104">Validatestringptrw-Makro</span><span class="sxs-lookup"><span data-stu-id="a9fbe-104">ValidateStringPtrW macro</span></span>

<span data-ttu-id="a9fbe-105">Überprüft, ob der aufrufenden Prozess Lesezugriff auf eine breit Zeichen-Zeichenfolge hat.</span><span class="sxs-lookup"><span data-stu-id="a9fbe-105">Verifies that the calling process has read access to a wide-character string.</span></span> <span data-ttu-id="a9fbe-106">Andernfalls ruft das Makro das [**dbgbreak**](dbgbreak.md) -Makro auf.</span><span class="sxs-lookup"><span data-stu-id="a9fbe-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="a9fbe-107">Dieses Makro ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="a9fbe-107">This macro is deprecated.</span></span> <span data-ttu-id="a9fbe-108">Im Windows SDK für Windows Vista (und höher) führt dieses Makro nichts aus.</span><span class="sxs-lookup"><span data-stu-id="a9fbe-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a9fbe-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9fbe-109">Syntax</span></span>


```C++
void ValidateStringPtrW(
   LPCWSTR p
);
```



## <a name="parameters"></a><span data-ttu-id="a9fbe-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9fbe-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9fbe-111">*cker*</span><span class="sxs-lookup"><span data-stu-id="a9fbe-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="a9fbe-112">Zeiger auf eine NULL-terminierte breit Zeichen-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a9fbe-112">Pointer to a NULL-terminated wide-character string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9fbe-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9fbe-113">Return value</span></span>

<span data-ttu-id="a9fbe-114">Dieses Makro gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a9fbe-114">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9fbe-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9fbe-115">Remarks</span></span>

<span data-ttu-id="a9fbe-116">Dieses Makro wird ignoriert, es sei denn, Debug, \_ Debug oder vfwrobust wird definiert, wenn die DirectShow-Basisklassen-Header Datei eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="a9fbe-116">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span> <span data-ttu-id="a9fbe-117">Dieses Makro kann einen erheblichen Leistungs Aufwand verursachen.</span><span class="sxs-lookup"><span data-stu-id="a9fbe-117">This macro can have a significant performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9fbe-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9fbe-118">Requirements</span></span>



| <span data-ttu-id="a9fbe-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9fbe-119">Requirement</span></span> | <span data-ttu-id="a9fbe-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a9fbe-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9fbe-121">Header</span><span class="sxs-lookup"><span data-stu-id="a9fbe-121">Header</span></span><br/> | <dl> <span data-ttu-id="a9fbe-122"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9fbe-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9fbe-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9fbe-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9fbe-124">Zeiger Validierungs Makros</span><span class="sxs-lookup"><span data-stu-id="a9fbe-124">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




