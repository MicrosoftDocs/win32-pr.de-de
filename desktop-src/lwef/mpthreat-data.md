---
title: MPTHREAT_DATA Struktur (mpclient. h)
description: Benachrichtigungs Daten wurden aufgrund von Bedrohungserkennung oder-Änderung übermittelt.
ms.assetid: 07A2F88B-9D58-44EC-86D0-BDCC1DF44B94
keywords:
- MPTHREAT_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPTHREAT_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPTHREAT_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cafbb11dbb3b1a34b38ffd0448db96fd1409efd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344720"
---
# <a name="mpthreat_data-structure"></a><span data-ttu-id="39fcb-105">Mpthreat- \_ Datenstruktur</span><span class="sxs-lookup"><span data-stu-id="39fcb-105">MPTHREAT\_DATA structure</span></span>

<span data-ttu-id="39fcb-106">Benachrichtigungs Daten wurden aufgrund von Bedrohungserkennung oder-Änderung übermittelt.</span><span class="sxs-lookup"><span data-stu-id="39fcb-106">Notification data passed due to threat detection or modification.</span></span>

## <a name="syntax"></a><span data-ttu-id="39fcb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="39fcb-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_DATA {
  MPTHREAT_ID     ThreatID;
  DWORD           dwSessionID;
  MPTHREAT_ACTION ThreatAction;
  DWORD           dwStatus;
} MPTHREAT_DATA, *PMPTHREAT_DATA;
```



## <a name="members"></a><span data-ttu-id="39fcb-108">Member</span><span class="sxs-lookup"><span data-stu-id="39fcb-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="39fcb-109">**Threatid**</span><span class="sxs-lookup"><span data-stu-id="39fcb-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="39fcb-110">Typ: **mpthreat- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="39fcb-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="39fcb-111">Bedrohungs Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="39fcb-111">Threat identifier.</span></span> <span data-ttu-id="39fcb-112">Das obere Bit ist festgelegt, um antivirenbezogene Bedrohungen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="39fcb-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="39fcb-113">**dwsessionid**</span><span class="sxs-lookup"><span data-stu-id="39fcb-113">**dwSessionID**</span></span>
</dt> <dd>

<span data-ttu-id="39fcb-114">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="39fcb-114">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="39fcb-115">Die der Bedrohung zugeordnete Sitzung.</span><span class="sxs-lookup"><span data-stu-id="39fcb-115">Session associated with the threat.</span></span> <span data-ttu-id="39fcb-116">Auf-1 festgelegt, wenn keine Sitzungs spezifischen Informationen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="39fcb-116">Set to -1 if no session specific information is available.</span></span>

</dd> <dt>

<span data-ttu-id="39fcb-117">**Maßnahme**</span><span class="sxs-lookup"><span data-stu-id="39fcb-117">**ThreatAction**</span></span>
</dt> <dd>

<span data-ttu-id="39fcb-118">Typ: **[ **mpthreat- \_ Aktion**](mpthreat-action.md)**</span><span class="sxs-lookup"><span data-stu-id="39fcb-118">Type: **[**MPTHREAT\_ACTION**](mpthreat-action.md)**</span></span>

</dd> <dd>

<span data-ttu-id="39fcb-119">Es wurde versucht, die Bedrohungs Aktion für den Fehler "mpnotify Threat Clean failed-Ereignisse **\_ \_ \_ erfolgreich**" zu beheben / **\_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="39fcb-119">Threat action tried for the **MPNOTIFY\_THREAT\_CLEAN\_SUCCEEDED**/**MPNOTIFY\_THREAT\_CLEAN\_FAILED** events.</span></span>

</dd> <dt>

<span data-ttu-id="39fcb-120">**dwStatus**</span><span class="sxs-lookup"><span data-stu-id="39fcb-120">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="39fcb-121">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="39fcb-121">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="39fcb-122">Zusätzliche Status oder Aktionen, die der ausgeführten Aktion zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="39fcb-122">Additional status or actions associated with the action taken.</span></span> <span data-ttu-id="39fcb-123">Dies ist eine Kombination von Bitflags aus dem [**mpstatus- \_ Flag**](mpstatus-flag.md).</span><span class="sxs-lookup"><span data-stu-id="39fcb-123">This is a combination of bit flags from [**MPSTATUS\_FLAG**](mpstatus-flag.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="39fcb-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39fcb-124">Requirements</span></span>



| <span data-ttu-id="39fcb-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39fcb-125">Requirement</span></span> | <span data-ttu-id="39fcb-126">Wert</span><span class="sxs-lookup"><span data-stu-id="39fcb-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39fcb-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39fcb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="39fcb-128">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39fcb-128">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="39fcb-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39fcb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="39fcb-130">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39fcb-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39fcb-131">Header</span><span class="sxs-lookup"><span data-stu-id="39fcb-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="39fcb-132"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="39fcb-132"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39fcb-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39fcb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39fcb-134">**\_mpstatusflag**</span><span class="sxs-lookup"><span data-stu-id="39fcb-134">**MPSTATUS\_FLAG**</span></span>](mpstatus-flag.md)
</dt> <dt>

[<span data-ttu-id="39fcb-135">**mpthreat- \_ Aktion**</span><span class="sxs-lookup"><span data-stu-id="39fcb-135">**MPTHREAT\_ACTION**</span></span>](mpthreat-action.md)
</dt> </dl>

 

 





