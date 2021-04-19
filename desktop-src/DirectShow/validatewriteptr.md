---
description: Überprüft, ob der aufrufende Prozess über Schreibzugriff auf einen Speicherblock verfügt. Andernfalls ruft das Makro das dbgbreak-Makro auf.
ms.assetid: efbb5ca6-0289-487d-b55a-f85b38d0515a
title: Validatewrite-PTR-Makro (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateWritePtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: e7c955f31cf9e0bf1050c52b680dfc9b32741bb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359822"
---
# <a name="validatewriteptr-macro"></a><span data-ttu-id="bd829-104">Validatewrite-PTR-Makro</span><span class="sxs-lookup"><span data-stu-id="bd829-104">ValidateWritePtr macro</span></span>

<span data-ttu-id="bd829-105">Überprüft, ob der aufrufende Prozess über Schreibzugriff auf einen Speicherblock verfügt.</span><span class="sxs-lookup"><span data-stu-id="bd829-105">Verifies that the calling process has write access to a memory block.</span></span> <span data-ttu-id="bd829-106">Andernfalls ruft das Makro das [**dbgbreak**](dbgbreak.md) -Makro auf.</span><span class="sxs-lookup"><span data-stu-id="bd829-106">If not, the macro calls the [**DbgBreak**](dbgbreak.md) macro.</span></span>

> [!Note]  
> <span data-ttu-id="bd829-107">Dieses Makro ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="bd829-107">This macro is deprecated.</span></span> <span data-ttu-id="bd829-108">Im Windows SDK für Windows Vista (und höher) führt dieses Makro nichts aus.</span><span class="sxs-lookup"><span data-stu-id="bd829-108">In the Windows SDK for Windows Vista (and later) this macro does not do anything.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="bd829-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd829-109">Syntax</span></span>


```C++
void ValidateWritePtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a><span data-ttu-id="bd829-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd829-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd829-111">*cker*</span><span class="sxs-lookup"><span data-stu-id="bd829-111">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="bd829-112">Zeiger auf einen Speicherblock.</span><span class="sxs-lookup"><span data-stu-id="bd829-112">Pointer to a memory block.</span></span>

</dd> <dt>

<span data-ttu-id="bd829-113">*betrieben*</span><span class="sxs-lookup"><span data-stu-id="bd829-113">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="bd829-114">Größe des Speicherblocks in Bytes.</span><span class="sxs-lookup"><span data-stu-id="bd829-114">Size of the memory block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd829-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd829-115">Return value</span></span>

<span data-ttu-id="bd829-116">Dieses Makro gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bd829-116">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd829-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd829-117">Remarks</span></span>

<span data-ttu-id="bd829-118">Dieses Makro wird ignoriert, es sei denn, Debug, \_ Debug oder vfwrobust wird definiert, wenn die DirectShow-Basisklassen-Header Datei eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="bd829-118">This macro is ignored unless DEBUG, \_DEBUG, or VFWROBUST is defined when the DirectShow base-class header file is included.</span></span> <span data-ttu-id="bd829-119">Dieses Makro kann einen erheblichen Leistungs Aufwand verursachen.</span><span class="sxs-lookup"><span data-stu-id="bd829-119">This macro can have a significant performance cost.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd829-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd829-120">Requirements</span></span>



| <span data-ttu-id="bd829-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd829-121">Requirement</span></span> | <span data-ttu-id="bd829-122">Wert</span><span class="sxs-lookup"><span data-stu-id="bd829-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd829-123">Header</span><span class="sxs-lookup"><span data-stu-id="bd829-123">Header</span></span><br/> | <dl> <span data-ttu-id="bd829-124"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bd829-124"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd829-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd829-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd829-126">Zeiger Validierungs Makros</span><span class="sxs-lookup"><span data-stu-id="bd829-126">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




