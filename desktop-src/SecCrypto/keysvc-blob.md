---
description: Die keysvc- \_ BLOB-Struktur definiert ein Schlüsseldienst-BLOB. Diese Struktur wird von der Funktion rkeypfxinstall verwendet.
ms.assetid: 255b5fab-6271-4d3f-9c56-a63278b8b104
title: KEYSVC_BLOB Struktur (rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_BLOB
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 801be5f5a0d431f488da6e13e1f3082d147c5974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357093"
---
# <a name="keysvc_blob-structure"></a><span data-ttu-id="63903-104">Keysvc- \_ BLOB-Struktur</span><span class="sxs-lookup"><span data-stu-id="63903-104">KEYSVC\_BLOB structure</span></span>

<span data-ttu-id="63903-105">Die **keysvc- \_ BLOB** -Struktur definiert ein Schlüsseldienst-BLOB.</span><span class="sxs-lookup"><span data-stu-id="63903-105">The **KEYSVC\_BLOB** structure defines a key service BLOB.</span></span> <span data-ttu-id="63903-106">Diese Struktur wird von der Funktion [**rkeypfxinstall**](rkeypfxinstall.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="63903-106">This structure is used by the [**RKeyPFXInstall**](rkeypfxinstall.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="63903-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="63903-107">Syntax</span></span>


```C++
typedef struct _KEYSVC_BLOB {
  ULONG cb;
  BYTE  *pb;
} KEYSVC_BLOB, *PKEYSVC_BLOB;
```



## <a name="members"></a><span data-ttu-id="63903-108">Member</span><span class="sxs-lookup"><span data-stu-id="63903-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="63903-109">**betrieben**</span><span class="sxs-lookup"><span data-stu-id="63903-109">**cb**</span></span>
</dt> <dd>

<span data-ttu-id="63903-110">Ein **ulong** -Wert, der die Größe von **PB** in Byte angibt.</span><span class="sxs-lookup"><span data-stu-id="63903-110">A **ULONG** value that specifies the size, in bytes, of **pb**.</span></span>

</dd> <dt>

<span data-ttu-id="63903-111">**PB**</span><span class="sxs-lookup"><span data-stu-id="63903-111">**pb**</span></span>
</dt> <dd>

<span data-ttu-id="63903-112">Ein Zeiger auf ein **Byte** , das das BLOB enthält, im [*PKCS \# 12*](../secgloss/p-gly.md) -Format.</span><span class="sxs-lookup"><span data-stu-id="63903-112">A pointer to a **BYTE** that contains the BLOB, in [*PKCS \#12*](../secgloss/p-gly.md) format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="63903-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63903-113">Requirements</span></span>



| <span data-ttu-id="63903-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63903-114">Requirement</span></span> | <span data-ttu-id="63903-115">Wert</span><span class="sxs-lookup"><span data-stu-id="63903-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63903-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="63903-116">Minimum supported client</span></span><br/> | <span data-ttu-id="63903-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="63903-117">None supported</span></span><br/>                                                             |
| <span data-ttu-id="63903-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="63903-118">Minimum supported server</span></span><br/> | <span data-ttu-id="63903-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63903-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="63903-120">Header</span><span class="sxs-lookup"><span data-stu-id="63903-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="63903-121"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="63903-121"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63903-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63903-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63903-123">**Rkeypfxinstall**</span><span class="sxs-lookup"><span data-stu-id="63903-123">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> <dt>

[<span data-ttu-id="63903-124">**keysvc- \_ Unicode- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="63903-124">**KEYSVC\_UNICODE\_STRING**</span></span>](keysvc-unicode-string.md)
</dt> </dl>

 

 
