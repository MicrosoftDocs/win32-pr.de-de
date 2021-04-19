---
description: Gibt einen Betreff an, der signiert werden soll.
ms.assetid: ba569443-e50f-450b-82cc-b7328f0ca25a
title: SIGNER_SUBJECT_INFO Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SUBJECT_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 05b5d780e50f8ea10fcf68cc90ae7092bbc2c473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349807"
---
# <a name="signer_subject_info-structure"></a><span data-ttu-id="471d9-103">Struktur der Signatur Geber \_ \_ Informationen</span><span class="sxs-lookup"><span data-stu-id="471d9-103">SIGNER\_SUBJECT\_INFO structure</span></span>

<span data-ttu-id="471d9-104">Die **\_ \_ betreffinformations** Struktur des Signatur Gebers gibt einen Betreff an, der signiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="471d9-104">The **SIGNER\_SUBJECT\_INFO** structure specifies a subject to sign.</span></span>

> [!Note]  
> <span data-ttu-id="471d9-105">Diese Struktur ist nicht in einer Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="471d9-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="471d9-106">Um diese Struktur verwenden zu können, müssen Sie Sie selbst definieren, wie in diesem Thema gezeigt.</span><span class="sxs-lookup"><span data-stu-id="471d9-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="471d9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="471d9-107">Syntax</span></span>


```C++
typedef struct _SIGNER_SUBJECT_INFO {
  DWORD cbSize;
  DWORD *pdwIndex;
  DWORD dwSubjectChoice;
  union {
    SIGNER_FILE_INFO *pSignerFileInfo;
    SIGNER_BLOB_INFO *pSignerBlobInfo;
  };
} SIGNER_SUBJECT_INFO, *PSIGNER_SUBJECT_INFO;
```



## <a name="members"></a><span data-ttu-id="471d9-108">Member</span><span class="sxs-lookup"><span data-stu-id="471d9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="471d9-109">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="471d9-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="471d9-110">Die Größe der-Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="471d9-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="471d9-111">**pdwindex**</span><span class="sxs-lookup"><span data-stu-id="471d9-111">**pdwIndex**</span></span>
</dt> <dd>

<span data-ttu-id="471d9-112">Dieser Member ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="471d9-112">This member is reserved.</span></span> <span data-ttu-id="471d9-113">Er muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="471d9-113">It must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="471d9-114">**dwsubjetchoice**</span><span class="sxs-lookup"><span data-stu-id="471d9-114">**dwSubjectChoice**</span></span>
</dt> <dd>

<span data-ttu-id="471d9-115">Gibt an, ob der Betreff eine Datei oder ein [*BLOB*](../secgloss/b-gly.md)ist.</span><span class="sxs-lookup"><span data-stu-id="471d9-115">Specifies whether the subject is a file or a [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="471d9-116">Dieser Member kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="471d9-116">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="471d9-117">Wert</span><span class="sxs-lookup"><span data-stu-id="471d9-117">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="471d9-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="471d9-118">Meaning</span></span>                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SIGNER_SUBJECT_BLOB"></span><span id="signer_subject_blob"></span><dl> <span data-ttu-id="471d9-119"><dt>**Signatur \_ Geber Subject \_ BLOB**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="471d9-119"><dt>**SIGNER\_SUBJECT\_BLOB**</dt> <dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="471d9-120">Der Betreff ist ein BLOB.</span><span class="sxs-lookup"><span data-stu-id="471d9-120">The subject is a BLOB.</span></span><br/> |
| <span id="SIGNER_SUBJECT_FILE"></span><span id="signer_subject_file"></span><dl> <span data-ttu-id="471d9-121"><dt>**Signatur \_ Geber \_Betreffdatei**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="471d9-121"><dt>**SIGNER\_SUBJECT\_FILE**</dt> <dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="471d9-122">Der Betreff ist eine Datei.</span><span class="sxs-lookup"><span data-stu-id="471d9-122">The subject is a file.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="471d9-123">**psignerfileingefo**</span><span class="sxs-lookup"><span data-stu-id="471d9-123">**pSignerFileInfo**</span></span>
</dt> <dd>

<span data-ttu-id="471d9-124">Ein Zeiger auf die [**\_ \_ Informations**](signer-file-info.md) Struktur der Signatur Geber Datei, die die zu Signier ender Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="471d9-124">A pointer to a [**SIGNER\_FILE\_INFO**](signer-file-info.md) structure that specifies the file to sign.</span></span>

</dd> <dt>

<span data-ttu-id="471d9-125">**psignerblobinfo**</span><span class="sxs-lookup"><span data-stu-id="471d9-125">**pSignerBlobInfo**</span></span>
</dt> <dd>

<span data-ttu-id="471d9-126">Ein Zeiger auf eine [**Signatur Geber- \_ BLOB- \_ Informations**](signer-blob-info.md) Struktur, die das zu Signier ender BLOB angibt.</span><span class="sxs-lookup"><span data-stu-id="471d9-126">A pointer to a [**SIGNER\_BLOB\_INFO**](signer-blob-info.md) structure that specifies the BLOB to sign.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="471d9-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="471d9-127">Requirements</span></span>



| <span data-ttu-id="471d9-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="471d9-128">Requirement</span></span> | <span data-ttu-id="471d9-129">Wert</span><span class="sxs-lookup"><span data-stu-id="471d9-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="471d9-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="471d9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="471d9-131">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="471d9-131">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="471d9-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="471d9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="471d9-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="471d9-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="471d9-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="471d9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="471d9-135">**Signersign**</span><span class="sxs-lookup"><span data-stu-id="471d9-135">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="471d9-136">**Signersignetx**</span><span class="sxs-lookup"><span data-stu-id="471d9-136">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
