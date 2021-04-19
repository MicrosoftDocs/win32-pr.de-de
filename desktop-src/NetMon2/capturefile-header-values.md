---
description: Definiert die Struktur der Netzwerkmonitor-Header Datei.
ms.assetid: 944980c9-ebaa-4042-a112-d32b7a28ba21
title: CAPTUREFILE_HEADER_VALUES Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILE_HEADER_VALUES
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2597b3f83a65dafd2da0198aade5243acc1184fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356704"
---
# <a name="capturefile_header_values-structure"></a><span data-ttu-id="0258f-103">Capturefile- \_ Header \_ Werte-Struktur</span><span class="sxs-lookup"><span data-stu-id="0258f-103">CAPTUREFILE\_HEADER\_VALUES structure</span></span>

<span data-ttu-id="0258f-104">Die **capturefile- \_ Header \_ Werte** Struktur definiert die Struktur der Netzwerkmonitor-Header Datei.</span><span class="sxs-lookup"><span data-stu-id="0258f-104">The **CAPTUREFILE\_HEADER\_VALUES** structure defines the Network Monitor header file structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="0258f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0258f-105">Syntax</span></span>


```C++
typedef struct _CAPTUREFILE_HEADER_VALUES {
  DWORD      Signature;
  BYTE       BCDVerMinor;
  BYTE       BCDVerMajor;
  WORD       MacType;
  SYSTEMTIME TimeStamp;
  DWORD      FrameTableOffset;
  DWORD      FrameTableLength;
  DWORD      UserDataOffset;
  DWORD      UserDataLength;
  DWORD      CommentDataOffset;
  DWORD      CommentDataLength;
  DWORD      StatisticsOffset;
  DWORD      StatisticsLength;
  DWORD      NetworkInfoOffset;
  DWORD      NetworkInfoLength;
  DWORD      ConversationStatsOffset;
  DWORD      ConversationStatsLength;
} CAPTUREFILE_HEADER_VALUES, *LPCAPTUREFILE_HEADER_VALUES;
```



## <a name="members"></a><span data-ttu-id="0258f-106">Member</span><span class="sxs-lookup"><span data-stu-id="0258f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0258f-107">**Signature**</span><span class="sxs-lookup"><span data-stu-id="0258f-107">**Signature**</span></span>
</dt> <dd>

<span data-ttu-id="0258f-108">Eindeutiger Bezeichner: ' gmbu.</span><span class="sxs-lookup"><span data-stu-id="0258f-108">Unique identifier: 'GMBU.</span></span>

</dd> <dt>

<span data-ttu-id="0258f-109">**Bcdverminor**</span><span class="sxs-lookup"><span data-stu-id="0258f-109">**BCDVerMinor**</span></span>
</dt> <dd>

<span data-ttu-id="0258f-110">Binary, Coded Decimal (Minor).</span><span class="sxs-lookup"><span data-stu-id="0258f-110">Binary, coded decimal (minor).</span></span> <span data-ttu-id="0258f-111">Der Wert dieses Members sollte NULL (0) sein.</span><span class="sxs-lookup"><span data-stu-id="0258f-111">The value of this member should be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="0258f-112">**Bcdvermajor**</span><span class="sxs-lookup"><span data-stu-id="0258f-112">**BCDVerMajor**</span></span>
</dt> <dd>

<span data-ttu-id="0258f-113">Binary Coded Decimal (Major).</span><span class="sxs-lookup"><span data-stu-id="0258f-113">Binary coded decimal (major).</span></span> <span data-ttu-id="0258f-114">Dieser Wert sollte 2 lauten.</span><span class="sxs-lookup"><span data-stu-id="0258f-114">This value should be 2.</span></span>

</dd> <dt>

<span data-ttu-id="0258f-115">**MacType**</span><span class="sxs-lookup"><span data-stu-id="0258f-115">**MacType**</span></span>
</dt> <dd>

<span data-ttu-id="0258f-116">Topologietyp.</span><span class="sxs-lookup"><span data-stu-id="0258f-116">Topology type.</span></span>

</dd> <dt>

<span data-ttu-id="0258f-117">**Zeitstempel**</span><span class="sxs-lookup"><span data-stu-id="0258f-117">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="0258f-118">Erfassungs Zeit.</span><span class="sxs-lookup"><span data-stu-id="0258f-118">Time of capture.</span></span>

</dd> <dt>

<span data-ttu-id="0258f-119">**Frametableoffset**</span><span class="sxs-lookup"><span data-stu-id="0258f-119">**FrameTableOffset**</span></span>
</dt> <dd>

<span data-ttu-id="0258f-120">Tabelle für Frame index.</span><span class="sxs-lookup"><span data-stu-id="0258f-120">Frame index table.</span></span>

</dd> <dt>

<span data-ttu-id="0258f-121">**Frametablelength**</span><span class="sxs-lookup"><span data-stu-id="0258f-121">**FrameTableLength**</span></span>
</dt> <dd>

<span data-ttu-id="0258f-122">Tabellengröße für Frame index.</span><span class="sxs-lookup"><span data-stu-id="0258f-122">Frame index table size.</span></span>

</dd> <dt>

<span data-ttu-id="0258f-123">**Userdataoffset**</span><span class="sxs-lookup"><span data-stu-id="0258f-123">**UserDataOffset**</span></span>
</dt> <dd>

<span data-ttu-id="0258f-124">Offset von Benutzerdaten.</span><span class="sxs-lookup"><span data-stu-id="0258f-124">User data offset.</span></span>

</dd> <dt>

<span data-ttu-id="0258f-125">**User DATALENGTH**</span><span class="sxs-lookup"><span data-stu-id="0258f-125">**UserDataLength**</span></span>
</dt> <dd>

<span data-ttu-id="0258f-126">Benutzerdaten Länge.</span><span class="sxs-lookup"><span data-stu-id="0258f-126">User data length.</span></span>

</dd> <dt>

<span data-ttu-id="0258f-127">**Commentdataoffset**</span><span class="sxs-lookup"><span data-stu-id="0258f-127">**CommentDataOffset**</span></span>
</dt> <dd>

<span data-ttu-id="0258f-128">Kommentar Daten Offset.</span><span class="sxs-lookup"><span data-stu-id="0258f-128">Comment data offset.</span></span>

</dd> <dt>

<span data-ttu-id="0258f-129">**Commentdatalength**</span><span class="sxs-lookup"><span data-stu-id="0258f-129">**CommentDataLength**</span></span>
</dt> <dd>

<span data-ttu-id="0258f-130">Länge der Kommentar Daten.</span><span class="sxs-lookup"><span data-stu-id="0258f-130">Length of comment data.</span></span>

</dd> <dt>

<span data-ttu-id="0258f-131">**Statisticsoffset**</span><span class="sxs-lookup"><span data-stu-id="0258f-131">**StatisticsOffset**</span></span>
</dt> <dd>

<span data-ttu-id="0258f-132">Offset zur **Statistik** Struktur.</span><span class="sxs-lookup"><span data-stu-id="0258f-132">Offset to the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="0258f-133">**Statisticslength**</span><span class="sxs-lookup"><span data-stu-id="0258f-133">**StatisticsLength**</span></span>
</dt> <dd>

<span data-ttu-id="0258f-134">Länge der **Statistik** Struktur.</span><span class="sxs-lookup"><span data-stu-id="0258f-134">Length of the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="0258f-135">**Networkinfooffset**</span><span class="sxs-lookup"><span data-stu-id="0258f-135">**NetworkInfoOffset**</span></span>
</dt> <dd>

<span data-ttu-id="0258f-136">Offset zur **networkinfo** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="0258f-136">Offset to the **NETWORKINFO** structure.</span></span>

</dd> <dt>

<span data-ttu-id="0258f-137">**Networkinfolength**</span><span class="sxs-lookup"><span data-stu-id="0258f-137">**NetworkInfoLength**</span></span>
</dt> <dd>

<span data-ttu-id="0258f-138">Länge der **networkinfo** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="0258f-138">Length of the **NETWORKINFO** structure.</span></span>

</dd> <dt>

<span data-ttu-id="0258f-139">**Conversationstatusoffset**</span><span class="sxs-lookup"><span data-stu-id="0258f-139">**ConversationStatsOffset**</span></span>
</dt> <dd>

<span data-ttu-id="0258f-140">Dieser Member wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0258f-140">This member is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0258f-141">**Conversationstatuslength**</span><span class="sxs-lookup"><span data-stu-id="0258f-141">**ConversationStatsLength**</span></span>
</dt> <dd>

<span data-ttu-id="0258f-142">Dieser Member wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0258f-142">This member is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0258f-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0258f-143">Requirements</span></span>



| <span data-ttu-id="0258f-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0258f-144">Requirement</span></span> | <span data-ttu-id="0258f-145">Wert</span><span class="sxs-lookup"><span data-stu-id="0258f-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0258f-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0258f-146">Minimum supported client</span></span><br/> | <span data-ttu-id="0258f-147">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0258f-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0258f-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0258f-148">Minimum supported server</span></span><br/> | <span data-ttu-id="0258f-149">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0258f-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0258f-150">Header</span><span class="sxs-lookup"><span data-stu-id="0258f-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="0258f-151"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0258f-151"><dt>Netmon.h</dt></span></span> </dl> |



 

 




