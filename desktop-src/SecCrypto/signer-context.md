---
description: Enthält ein signiertes BLOB.
ms.assetid: c12d9007-c779-4363-8e28-6387a665a0d6
title: SIGNER_CONTEXT Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CONTEXT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4ebc7d5380438fc6cd28a43136273387c1919713
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362685"
---
# <a name="signer_context-structure"></a><span data-ttu-id="cc282-103">Signatur Geber- \_ Kontext Struktur</span><span class="sxs-lookup"><span data-stu-id="cc282-103">SIGNER\_CONTEXT structure</span></span>

<span data-ttu-id="cc282-104">Die **Signatur Geber- \_ Kontext** Struktur enthält ein signiertes [*BLOB*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="cc282-104">The **SIGNER\_CONTEXT** structure contains a signed [*BLOB*](../secgloss/b-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="cc282-105">Diese Struktur ist nicht in einer Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="cc282-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="cc282-106">Um diese Struktur verwenden zu können, müssen Sie Sie selbst definieren, wie in diesem Thema gezeigt.</span><span class="sxs-lookup"><span data-stu-id="cc282-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="cc282-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc282-107">Syntax</span></span>


```C++
typedef struct _SIGNER_CONTEXT {
  DWORD cbSize;
  DWORD cbBlob;
  BYTE  *pbBlob;
} SIGNER_CONTEXT, *PSIGNER_CONTEXT;
```



## <a name="members"></a><span data-ttu-id="cc282-108">Member</span><span class="sxs-lookup"><span data-stu-id="cc282-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="cc282-109">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="cc282-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="cc282-110">Die Größe der-Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="cc282-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="cc282-111">**cbblob**</span><span class="sxs-lookup"><span data-stu-id="cc282-111">**cbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="cc282-112">Die Größe (in Bytes) des **pbBlob** -Members.</span><span class="sxs-lookup"><span data-stu-id="cc282-112">The size, in bytes, of the **pbBlob** member.</span></span>

</dd> <dt>

<span data-ttu-id="cc282-113">**pbBlob**</span><span class="sxs-lookup"><span data-stu-id="cc282-113">**pbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="cc282-114">Ein Zeiger auf das signierte BLOB.</span><span class="sxs-lookup"><span data-stu-id="cc282-114">A pointer to the signed BLOB.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc282-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc282-115">Requirements</span></span>



| <span data-ttu-id="cc282-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc282-116">Requirement</span></span> | <span data-ttu-id="cc282-117">Wert</span><span class="sxs-lookup"><span data-stu-id="cc282-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cc282-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cc282-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cc282-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc282-119">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="cc282-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cc282-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cc282-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc282-121">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cc282-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc282-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc282-123">**Signersign**</span><span class="sxs-lookup"><span data-stu-id="cc282-123">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="cc282-124">**Signersignetx**</span><span class="sxs-lookup"><span data-stu-id="cc282-124">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
