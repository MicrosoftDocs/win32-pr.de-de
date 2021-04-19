---
description: Die keysvc \_ \_ -Unicode-Zeichen folgen Struktur definiert eine Unicode-Zeichenfolge und eine maximale Länge für die Zeichenfolge. Diese Struktur wird von der Funktion rkeypfxinstall verwendet.
ms.assetid: 12142543-5c53-4638-9fd7-f523594142c8
title: KEYSVC_UNICODE_STRING Struktur (rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_UNICODE_STRING
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 5424fa103b2bbbadd735dbda0bb92f9dea21787b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351583"
---
# <a name="keysvc_unicode_string-structure"></a><span data-ttu-id="9848f-104">Keysvc- \_ Unicode- \_ Zeichen folgen Struktur</span><span class="sxs-lookup"><span data-stu-id="9848f-104">KEYSVC\_UNICODE\_STRING structure</span></span>

<span data-ttu-id="9848f-105">Die **keysvc- \_ Unicode- \_ Zeichen** folgen Struktur definiert eine [*Unicode*](../secgloss/u-gly.md) -Zeichenfolge und eine maximale Länge für die Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9848f-105">The **KEYSVC\_UNICODE\_STRING** structure defines a [*Unicode*](../secgloss/u-gly.md) string and a maximum length for the string.</span></span> <span data-ttu-id="9848f-106">Diese Struktur wird von der Funktion [**rkeypfxinstall**](rkeypfxinstall.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="9848f-106">This structure is used by the [**RKeyPFXInstall**](rkeypfxinstall.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="9848f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9848f-107">Syntax</span></span>


```C++
typedef struct _KEYSVC_UNICODE_STRING {
  USHORT Length;
  USHORT MaximumLength;
  USHORT *Buffer;
} KEYSVC_UNICODE_STRING, *PKEYSVC_UNICODE_STRING;
```



## <a name="members"></a><span data-ttu-id="9848f-108">Member</span><span class="sxs-lookup"><span data-stu-id="9848f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="9848f-109">**Länge**</span><span class="sxs-lookup"><span data-stu-id="9848f-109">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="9848f-110">Ein **UShort** -Wert, der die Länge in Bytes angibt, die für den **Puffer** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9848f-110">A **USHORT** value that specifies the length, in bytes, used for **Buffer**.</span></span>

</dd> <dt>

<span data-ttu-id="9848f-111">**MaximumLength**</span><span class="sxs-lookup"><span data-stu-id="9848f-111">**MaximumLength**</span></span>
</dt> <dd>

<span data-ttu-id="9848f-112">Ein **UShort** -Wert, der die maximale Länge (in Byte) angibt, die für den **Puffer** zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="9848f-112">A **USHORT** value that specifies the maximum length, in bytes, allowed for **Buffer**.</span></span>

</dd> <dt>

<span data-ttu-id="9848f-113">**Buffer**</span><span class="sxs-lookup"><span data-stu-id="9848f-113">**Buffer**</span></span>
</dt> <dd>

<span data-ttu-id="9848f-114">Ein Zeiger auf einen **UShort** , der die Unicode-Zeichenfolge darstellt.</span><span class="sxs-lookup"><span data-stu-id="9848f-114">A pointer to a **USHORT** that represents the Unicode string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9848f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9848f-115">Requirements</span></span>



| <span data-ttu-id="9848f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9848f-116">Requirement</span></span> | <span data-ttu-id="9848f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="9848f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9848f-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9848f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9848f-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9848f-119">None supported</span></span><br/>                                                             |
| <span data-ttu-id="9848f-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9848f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9848f-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9848f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9848f-122">Header</span><span class="sxs-lookup"><span data-stu-id="9848f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9848f-123"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="9848f-123"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9848f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9848f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9848f-125">**Rkeypfxinstall**</span><span class="sxs-lookup"><span data-stu-id="9848f-125">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> <dt>

[<span data-ttu-id="9848f-126">**keysvc- \_ BLOB**</span><span class="sxs-lookup"><span data-stu-id="9848f-126">**KEYSVC\_BLOB**</span></span>](keysvc-blob.md)
</dt> </dl>

 

 
