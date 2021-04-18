---
description: Die propertyinstex-Struktur definiert eine frei Form erweiterte Eigenschafts Instanz.
ms.assetid: a2316baf-07e2-4617-bb35-e20cfb11fbcb
title: Propertyinstex-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINSTEX
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f7b196d30e96f9d047f7f923d969d65a918aa4f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345040"
---
# <a name="propertyinstex-structure"></a><span data-ttu-id="75e94-103">Propertyinstex-Struktur</span><span class="sxs-lookup"><span data-stu-id="75e94-103">PROPERTYINSTEX structure</span></span>

<span data-ttu-id="75e94-104">Die **propertyinstex** -Struktur definiert eine frei Form erweiterte Eigenschafts Instanz.</span><span class="sxs-lookup"><span data-stu-id="75e94-104">The **PROPERTYINSTEX** structure defines a freeform, extended property instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="75e94-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="75e94-105">Syntax</span></span>


```C++
typedef struct _PROPERTYINSTEX {
  WORD    Length;
  WORD    LengthEx;
  ULPVOID lpData;
  union {
    BYTE          Byte[];
    WORD          Word[];
    DWORD         Dword[];
    LARGE_INTEGER LargeInt[];
    SYSTEMTIME    SysTime[];
    TYPED_STRING  TypedString;
  };
} PROPERTYINSTEX;
```



## <a name="members"></a><span data-ttu-id="75e94-106">Member</span><span class="sxs-lookup"><span data-stu-id="75e94-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="75e94-107">**Länge**</span><span class="sxs-lookup"><span data-stu-id="75e94-107">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="75e94-108">Länge der Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="75e94-108">Length of the data in Bytes.</span></span>

</dd> <dt>

<span data-ttu-id="75e94-109">**Verlängert**</span><span class="sxs-lookup"><span data-stu-id="75e94-109">**LengthEx**</span></span>
</dt> <dd>

<span data-ttu-id="75e94-110">Länge der erweiterten Daten.</span><span class="sxs-lookup"><span data-stu-id="75e94-110">Length of the extended data.</span></span>

</dd> <dt>

<span data-ttu-id="75e94-111">**lpdata**</span><span class="sxs-lookup"><span data-stu-id="75e94-111">**lpData**</span></span>
</dt> <dd>

<span data-ttu-id="75e94-112">Zeiger auf die erweiterten Daten.</span><span class="sxs-lookup"><span data-stu-id="75e94-112">Pointer to the extended data.</span></span>

</dd> <dt>

<span data-ttu-id="75e94-113">**Byte**</span><span class="sxs-lookup"><span data-stu-id="75e94-113">**Byte**</span></span>
</dt> <dd>

<span data-ttu-id="75e94-114">Zeiger auf die **Bytedaten** .</span><span class="sxs-lookup"><span data-stu-id="75e94-114">Pointer to the **BYTE** data.</span></span>

</dd> <dt>

<span data-ttu-id="75e94-115">**Word**</span><span class="sxs-lookup"><span data-stu-id="75e94-115">**Word**</span></span>
</dt> <dd>

<span data-ttu-id="75e94-116">Zeiger auf das **Word** -Daten.</span><span class="sxs-lookup"><span data-stu-id="75e94-116">Pointer to the **WORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="75e94-117">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="75e94-117">**Dword**</span></span>
</dt> <dd>

<span data-ttu-id="75e94-118">Zeiger auf die **DWORD** -Daten.</span><span class="sxs-lookup"><span data-stu-id="75e94-118">Pointer to the **DWORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="75e94-119">**' Largeint**</span><span class="sxs-lookup"><span data-stu-id="75e94-119">**LargeInt**</span></span>
</dt> <dd>

<span data-ttu-id="75e94-120">Zeiger auf die **largeint** -Daten.</span><span class="sxs-lookup"><span data-stu-id="75e94-120">Pointer to the **LARGEINT** data.</span></span>

</dd> <dt>

<span data-ttu-id="75e94-121">**SysTime**</span><span class="sxs-lookup"><span data-stu-id="75e94-121">**SysTime**</span></span>
</dt> <dd>

<span data-ttu-id="75e94-122">Zeiger auf die **SYSTEMTIME** -Daten.</span><span class="sxs-lookup"><span data-stu-id="75e94-122">Pointer to the **SYSTEMTIME** data.</span></span>

</dd> <dt>

<span data-ttu-id="75e94-123">**Typedstring**</span><span class="sxs-lookup"><span data-stu-id="75e94-123">**TypedString**</span></span>
</dt> <dd>

<span data-ttu-id="75e94-124">Eine typisierte Zeichenfolge, die möglicherweise über erweiterte Daten verfügt.</span><span class="sxs-lookup"><span data-stu-id="75e94-124">A typed string that may have extended data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="75e94-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75e94-125">Requirements</span></span>



| <span data-ttu-id="75e94-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75e94-126">Requirement</span></span> | <span data-ttu-id="75e94-127">Wert</span><span class="sxs-lookup"><span data-stu-id="75e94-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="75e94-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="75e94-128">Minimum supported client</span></span><br/> | <span data-ttu-id="75e94-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75e94-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="75e94-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="75e94-130">Minimum supported server</span></span><br/> | <span data-ttu-id="75e94-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75e94-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="75e94-132">Header</span><span class="sxs-lookup"><span data-stu-id="75e94-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="75e94-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="75e94-133"><dt>Netmon.h</dt></span></span> </dl> |



 

 




