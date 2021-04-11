---
title: MPRESERVED_DATA Struktur (mpclient. h)
description: Reservierte Benachrichtigungs Daten.
ms.assetid: C92206BD-6E56-4B7D-ABB1-DC1149AE141D
keywords:
- MPRESERVED_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPRESERVED_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPRESERVED_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b1e08184da71fe857cb412ef986c986a0c59baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104547"
---
# <a name="mpreserved_data-structure"></a><span data-ttu-id="3a51d-105">Mbeibehaltene \_ Datenstruktur</span><span class="sxs-lookup"><span data-stu-id="3a51d-105">MPRESERVED\_DATA structure</span></span>

<span data-ttu-id="3a51d-106">Reservierte Benachrichtigungs Daten.</span><span class="sxs-lookup"><span data-stu-id="3a51d-106">Reserved notification data.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a51d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a51d-107">Syntax</span></span>


```C++
typedef struct tagMPRESERVED_DATA {
  DWORD cbReservedData;
  BYTE  *pbReservedData;
} MPRESERVED_DATA, *PMPRESERVED_DATA;
```



## <a name="members"></a><span data-ttu-id="3a51d-108">Member</span><span class="sxs-lookup"><span data-stu-id="3a51d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3a51d-109">**cbreserveddata**</span><span class="sxs-lookup"><span data-stu-id="3a51d-109">**cbReservedData**</span></span>
</dt> <dd>

<span data-ttu-id="3a51d-110">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3a51d-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3a51d-111">Größe der reservierten Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="3a51d-111">Size of reserved data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3a51d-112">**pbreserveddata**</span><span class="sxs-lookup"><span data-stu-id="3a51d-112">**pbReservedData**</span></span>
</dt> <dd>

<span data-ttu-id="3a51d-113">Type: **Byte \***</span><span class="sxs-lookup"><span data-stu-id="3a51d-113">Type: **BYTE\***</span></span>

</dd> <dd>

<span data-ttu-id="3a51d-114">Zeiger auf reservierte Daten.</span><span class="sxs-lookup"><span data-stu-id="3a51d-114">Pointer to reserved data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a51d-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a51d-115">Requirements</span></span>



| <span data-ttu-id="3a51d-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a51d-116">Requirement</span></span> | <span data-ttu-id="3a51d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="3a51d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a51d-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3a51d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3a51d-119">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a51d-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3a51d-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3a51d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3a51d-121">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a51d-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a51d-122">Header</span><span class="sxs-lookup"><span data-stu-id="3a51d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a51d-123"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a51d-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





