---
title: MPTHREAT_INFOEX_UNUSED Struktur (mpclient. h)
description: Pseudo Struktur für nicht verhaltensänderungstyp Bedrohungen.
ms.assetid: 3C5305CD-D533-47B5-ADD3-BD8DA05F2046
keywords:
- MPTHREAT_INFOEX_UNUSED Struktur Funktionen der Legacy-Windows-Umgebung
- PMPTHREAT_INFOEX_UNUSED Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_UNUSED
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fed78d904bd03fee17676dced7c828aaea8d319d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104535"
---
# <a name="mpthreat_infoex_unused-structure"></a><span data-ttu-id="2b494-105">Nicht verwendete mpthreat \_ INFOEX- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="2b494-105">MPTHREAT\_INFOEX\_UNUSED structure</span></span>

<span data-ttu-id="2b494-106">Pseudo Struktur für nicht verhaltensänderungstyp Bedrohungen.</span><span class="sxs-lookup"><span data-stu-id="2b494-106">Dummy structure for non-behavior modification type threats.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b494-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b494-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFOEX_UNUSED {
  DWORD dwNone;
} MPTHREAT_INFOEX_UNUSED, *PMPTHREAT_INFOEX_UNUSED;
```



## <a name="members"></a><span data-ttu-id="2b494-108">Member</span><span class="sxs-lookup"><span data-stu-id="2b494-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="2b494-109">**dwnone**</span><span class="sxs-lookup"><span data-stu-id="2b494-109">**dwNone**</span></span>
</dt> <dd>

<span data-ttu-id="2b494-110">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2b494-110">Type: **DWORD**</span></span>

<span data-ttu-id="2b494-111"></dd> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2b494-111"></dd> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="2b494-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b494-112">Requirements</span></span>



| <span data-ttu-id="2b494-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b494-113">Requirement</span></span> | <span data-ttu-id="2b494-114">Wert</span><span class="sxs-lookup"><span data-stu-id="2b494-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b494-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b494-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2b494-116">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b494-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2b494-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b494-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2b494-118">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b494-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2b494-119">Header</span><span class="sxs-lookup"><span data-stu-id="2b494-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b494-120"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b494-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 





