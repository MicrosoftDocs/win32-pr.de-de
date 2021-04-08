---
title: MPNIS_PRIVATE_DATA Struktur (mpclient. h)
description: Private NIS-Benachrichtigungen.
ms.assetid: 19B4928F-BC78-4DEA-A563-1516B6454465
keywords:
- MPNIS_PRIVATE_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPNIS_PRIVATE_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPNIS_PRIVATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21340665a32b619c42d7909e8cd1b72ca6d09fb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740137"
---
# <a name="mpnis_private_data-structure"></a><span data-ttu-id="79296-105">Private mpnis- \_ \_ Datenstruktur</span><span class="sxs-lookup"><span data-stu-id="79296-105">MPNIS\_PRIVATE\_DATA structure</span></span>

<span data-ttu-id="79296-106">Private NIS-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="79296-106">Private NIS notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="79296-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="79296-107">Syntax</span></span>


```C++
typedef struct tagMPNIS_PRIVATE_DATA {
  DWORD dwNotificationType;
  DWORD cbDataSize;
  BYTE  *pbData;
} MPNIS_PRIVATE_DATA, *PMPNIS_PRIVATE_DATA;
```



## <a name="members"></a><span data-ttu-id="79296-108">Member</span><span class="sxs-lookup"><span data-stu-id="79296-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="79296-109">**dwnotificationtype**</span><span class="sxs-lookup"><span data-stu-id="79296-109">**dwNotificationType**</span></span>
</dt> <dd>

<span data-ttu-id="79296-110">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="79296-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="79296-111">Hier wird der Benachrichtigungstyp angegeben.</span><span class="sxs-lookup"><span data-stu-id="79296-111">Type of notification.</span></span>

</dd> <dt>

<span data-ttu-id="79296-112">**cbDataSize**</span><span class="sxs-lookup"><span data-stu-id="79296-112">**cbDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="79296-113">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="79296-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="79296-114">Größe der reservierten Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="79296-114">Size of reserved data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="79296-115">**pbData**</span><span class="sxs-lookup"><span data-stu-id="79296-115">**pbData**</span></span>
</dt> <dd>

<span data-ttu-id="79296-116">Type: **Byte \***</span><span class="sxs-lookup"><span data-stu-id="79296-116">Type: **BYTE\***</span></span>

</dd> <dd>

<span data-ttu-id="79296-117">Zeiger auf reservierte Daten.</span><span class="sxs-lookup"><span data-stu-id="79296-117">Pointer to reserved data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="79296-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79296-118">Requirements</span></span>



| <span data-ttu-id="79296-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79296-119">Requirement</span></span> | <span data-ttu-id="79296-120">Wert</span><span class="sxs-lookup"><span data-stu-id="79296-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79296-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79296-121">Minimum supported client</span></span><br/> | <span data-ttu-id="79296-122">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79296-122">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="79296-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79296-123">Minimum supported server</span></span><br/> | <span data-ttu-id="79296-124">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79296-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="79296-125">Header</span><span class="sxs-lookup"><span data-stu-id="79296-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="79296-126"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="79296-126"><dt>MpClient.h</dt></span></span> </dl> |



 

 





