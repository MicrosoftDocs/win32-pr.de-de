---
description: Gibt an, dass ein BLOB signiert werden soll.
ms.assetid: 214c9c05-5c95-4803-8993-23a87266f991
title: SIGNER_BLOB_INFO Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_BLOB_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: a05e99cc4d7fa2eff196159bb449fa7dbfbf3026
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530290"
---
# <a name="signer_blob_info-structure"></a><span data-ttu-id="434d6-103">Signer \_ BLOB- \_ Informationsstruktur</span><span class="sxs-lookup"><span data-stu-id="434d6-103">SIGNER\_BLOB\_INFO structure</span></span>

<span data-ttu-id="434d6-104">\[Die Struktur der Signatur Geber- **\_ BLOB- \_ Informationen** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="434d6-104">\[The **SIGNER\_BLOB\_INFO** structure is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="434d6-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="434d6-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="434d6-106">Die **Signatur Geber- \_ BLOB- \_ Informations** Struktur gibt ein [*BLOB*](../secgloss/b-gly.md) an, das signiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="434d6-106">The **SIGNER\_BLOB\_INFO** structure specifies a [*BLOB*](../secgloss/b-gly.md) to sign.</span></span>

> [!Note]  
> <span data-ttu-id="434d6-107">Diese Struktur ist nicht in einer Header Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="434d6-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="434d6-108">Um diese Struktur verwenden zu können, müssen Sie Sie selbst definieren, wie in diesem Thema gezeigt.</span><span class="sxs-lookup"><span data-stu-id="434d6-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="434d6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="434d6-109">Syntax</span></span>


```C++
typedef struct _SIGNER_BLOB_INFO {
  DWORD   cbSize;
  GUID    *pGuidSubject;
  DWORD   cbBlob;
  BYTE    *pbBlob;
  LPCWSTR pwszDisplayName;
} SIGNER_BLOB_INFO, *PSIGNER_BLOB_INFO;
```



## <a name="members"></a><span data-ttu-id="434d6-110">Member</span><span class="sxs-lookup"><span data-stu-id="434d6-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="434d6-111">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="434d6-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="434d6-112">Die Größe der-Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="434d6-112">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="434d6-113">**pguidsubject**</span><span class="sxs-lookup"><span data-stu-id="434d6-113">**pGuidSubject**</span></span>
</dt> <dd>

<span data-ttu-id="434d6-114">Ein Zeiger auf eine **GUID** , die das zu ladende "Subject Interface Package" (SIP) angibt.</span><span class="sxs-lookup"><span data-stu-id="434d6-114">A pointer to a **GUID** that specifies the Subject Interface Package (SIP) to load.</span></span>

</dd> <dt>

<span data-ttu-id="434d6-115">**cbblob**</span><span class="sxs-lookup"><span data-stu-id="434d6-115">**cbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="434d6-116">Die Größe des zu Signier enden BLOBs in Byte.</span><span class="sxs-lookup"><span data-stu-id="434d6-116">The size, in bytes, of the BLOB to sign.</span></span>

</dd> <dt>

<span data-ttu-id="434d6-117">**pbBlob**</span><span class="sxs-lookup"><span data-stu-id="434d6-117">**pbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="434d6-118">Ein Zeiger auf das zu Signier-BLOB.</span><span class="sxs-lookup"><span data-stu-id="434d6-118">A pointer to the BLOB to sign.</span></span>

</dd> <dt>

<span data-ttu-id="434d6-119">**pwszdisplayname**</span><span class="sxs-lookup"><span data-stu-id="434d6-119">**pwszDisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="434d6-120">Der Anzeige Name des BLOBs.</span><span class="sxs-lookup"><span data-stu-id="434d6-120">The display name of the BLOB.</span></span> <span data-ttu-id="434d6-121">Dieser Member kann auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="434d6-121">This member can be set to **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="434d6-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="434d6-122">Requirements</span></span>



| <span data-ttu-id="434d6-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="434d6-123">Requirement</span></span> | <span data-ttu-id="434d6-124">Wert</span><span class="sxs-lookup"><span data-stu-id="434d6-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="434d6-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="434d6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="434d6-126">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="434d6-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="434d6-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="434d6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="434d6-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="434d6-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="434d6-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="434d6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="434d6-130">**Betreff- \_ Informationen des Signatur Gebers \_**</span><span class="sxs-lookup"><span data-stu-id="434d6-130">**SIGNER\_SUBJECT\_INFO**</span></span>](signer-subject-info.md)
</dt> </dl>

 

 
