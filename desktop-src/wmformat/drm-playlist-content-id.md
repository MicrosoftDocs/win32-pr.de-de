---
title: DRM_PLAYLIST_CONTENT_ID Struktur (drmexternals. h)
description: Die Struktur der DRM- \_ Wiedergabelisten \_ Inhalts- \_ ID enthält Informationen zu Inhalten, die im Rahmen einer Wiedergabeliste auf CD kopiert werden sollen.
ms.assetid: 124e86ac-b0d4-40b2-868b-fe2fed1898e1
keywords:
- DRM_PLAYLIST_CONTENT_ID Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- DRM_PLAYLIST_CONTENT_ID
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f475a8c3620ff1af64cb70914ca1ac591aa55106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341408"
---
# <a name="drm_playlist_content_id-structure"></a><span data-ttu-id="33417-105">Struktur der DRM- \_ Wiedergabelisten \_ Content \_ ID</span><span class="sxs-lookup"><span data-stu-id="33417-105">DRM\_PLAYLIST\_CONTENT\_ID structure</span></span>

<span data-ttu-id="33417-106">Die Struktur der **DRM- \_ Wiedergabelisten Inhalts- \_ \_ ID** enthält Informationen zu Inhalten, die im Rahmen einer Wiedergabeliste auf CD kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="33417-106">The **DRM\_PLAYLIST\_CONTENT\_ID** structure contains information about content that is to be copied to CD as part of a playlist burn.</span></span>

## <a name="syntax"></a><span data-ttu-id="33417-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="33417-107">Syntax</span></span>


```C++
typedef struct DRM_PLAYLIST_CONTENT_ID {
  LPCWSTR lpcwszV2Header;
  LPCSTR  lpcszV1KID;
  BYTE    *pbOtherData;
  DWORD   cbOtherData;
  DWORD   dwUniqueIDForSession;
  DWORD   dwValidFields;
} ;
```



## <a name="members"></a><span data-ttu-id="33417-108">Member</span><span class="sxs-lookup"><span data-stu-id="33417-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="33417-109">**lpcwszV2Header**</span><span class="sxs-lookup"><span data-stu-id="33417-109">**lpcwszV2Header**</span></span>
</dt> <dd>

<span data-ttu-id="33417-110">DRM-Header.</span><span class="sxs-lookup"><span data-stu-id="33417-110">DRM header.</span></span> <span data-ttu-id="33417-111">Verwenden Sie dieses Mitglied, wenn der Inhalt durch Windows Media DRM Version 2 oder höher geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="33417-111">Use this member if the content is protected by Windows Media DRM version 2 or later.</span></span>

</dd> <dt>

<span data-ttu-id="33417-112">**lpcszV1KID**</span><span class="sxs-lookup"><span data-stu-id="33417-112">**lpcszV1KID**</span></span>
</dt> <dd>

<span data-ttu-id="33417-113">Schlüssel-ID</span><span class="sxs-lookup"><span data-stu-id="33417-113">Key ID.</span></span> <span data-ttu-id="33417-114">Verwenden Sie dieses Mitglied, wenn der Inhalt durch Windows Media DRM, Version 1, geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="33417-114">Use this member if the content is protected by Windows Media DRM version 1.</span></span>

</dd> <dt>

<span data-ttu-id="33417-115">**pbotherdata**</span><span class="sxs-lookup"><span data-stu-id="33417-115">**pbOtherData**</span></span>
</dt> <dd>

<span data-ttu-id="33417-116">Puffer mit ergänzenden Daten.</span><span class="sxs-lookup"><span data-stu-id="33417-116">Buffer containing supplementary data.</span></span>

</dd> <dt>

<span data-ttu-id="33417-117">**cbotherdata**</span><span class="sxs-lookup"><span data-stu-id="33417-117">**cbOtherData**</span></span>
</dt> <dd>

<span data-ttu-id="33417-118">Größe des **pbotherdata** -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="33417-118">Size of the **pbOtherData** buffer in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="33417-119">**dwuniqueidforsession**</span><span class="sxs-lookup"><span data-stu-id="33417-119">**dwUniqueIDForSession**</span></span>
</dt> <dd>

<span data-ttu-id="33417-120">Eindeutiger Bezeichner für den in der aktuellen Sitzung zu verwendenden Inhalt.</span><span class="sxs-lookup"><span data-stu-id="33417-120">Unique identifier for the content to be used in the current session.</span></span>

</dd> <dt>

<span data-ttu-id="33417-121">**dwvalidfields**</span><span class="sxs-lookup"><span data-stu-id="33417-121">**dwValidFields**</span></span>
</dt> <dd>

<span data-ttu-id="33417-122">**DWORD** , das die gültigen Felder dieser-Struktur angibt.</span><span class="sxs-lookup"><span data-stu-id="33417-122">**DWORD** indicating the valid fields of this structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="33417-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33417-123">Requirements</span></span>



| <span data-ttu-id="33417-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33417-124">Requirement</span></span> | <span data-ttu-id="33417-125">Wert</span><span class="sxs-lookup"><span data-stu-id="33417-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="33417-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="33417-126">Minimum supported client</span></span><br/> | <span data-ttu-id="33417-127">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33417-127">Windows XP \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="33417-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="33417-128">Minimum supported server</span></span><br/> | <span data-ttu-id="33417-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33417-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="33417-130">Version</span><span class="sxs-lookup"><span data-stu-id="33417-130">Version</span></span><br/>                  | <span data-ttu-id="33417-131">SDK für Windows Media-Format 11</span><span class="sxs-lookup"><span data-stu-id="33417-131">Windows Media Format 11 SDK</span></span><br/>                                                    |
| <span data-ttu-id="33417-132">Header</span><span class="sxs-lookup"><span data-stu-id="33417-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="33417-133"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="33417-133"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33417-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33417-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33417-135">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="33417-135">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





