---
title: MPCLEAN_DATA Struktur (mpclient. h)
description: Benachrichtigungs Daten wurden an eine saubere Rückruffunktion übermittelt.
ms.assetid: 475A6525-5BD8-4B29-A684-53EE2758C790
keywords:
- MPCLEAN_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPCLEAN_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPCLEAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89f0c7e867918b6567279be7c41ce72e7e396576
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741025"
---
# <a name="mpclean_data-structure"></a><span data-ttu-id="04cd3-105">Mpclean- \_ Datenstruktur</span><span class="sxs-lookup"><span data-stu-id="04cd3-105">MPCLEAN\_DATA structure</span></span>

<span data-ttu-id="04cd3-106">Benachrichtigungs Daten wurden an eine saubere Rückruffunktion übermittelt.</span><span class="sxs-lookup"><span data-stu-id="04cd3-106">Notification data passed to clean callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="04cd3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="04cd3-107">Syntax</span></span>


```C++
typedef struct tagMPCLEAN_DATA {
  MPTHREAT_ID      ThreatID;
  MPTHREAT_ACTION  ThreatAction;
  DWORD            dwStatus;
  PMPRESOURCE_INFO ResourceInfo;
} MPCLEAN_DATA, *PMPCLEAN_DATA;
```



## <a name="members"></a><span data-ttu-id="04cd3-108">Member</span><span class="sxs-lookup"><span data-stu-id="04cd3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="04cd3-109">**Threatid**</span><span class="sxs-lookup"><span data-stu-id="04cd3-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="04cd3-110">Typ: **mpthreat- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="04cd3-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="04cd3-111">Bedrohungs Bezeichner für die **mpnotify- \_ Bereinigung \_ \_** bereinigen, dass Fehler bei der Bereinigung der Clean Threat-Ereignisse aufgetreten sind / **\_ \_ \_** / **\_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="04cd3-111">Threat identifier for the **MPNOTIFY\_CLEAN\_THREAT\_START**/**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**/**MPNOTIFY\_CLEAN\_THREAT\_FAILED** events.</span></span> <span data-ttu-id="04cd3-112">Das obere Bit ist festgelegt, um antivirenbezogene Bedrohungen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="04cd3-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="04cd3-113">**Maßnahme**</span><span class="sxs-lookup"><span data-stu-id="04cd3-113">**ThreatAction**</span></span>
</dt> <dd>

<span data-ttu-id="04cd3-114">Typ: **[ **mpthreat- \_ Aktion**](mpthreat-action.md)**</span><span class="sxs-lookup"><span data-stu-id="04cd3-114">Type: **[**MPTHREAT\_ACTION**](mpthreat-action.md)**</span></span>

</dd> <dd>

<span data-ttu-id="04cd3-115">Bedrohungs Aktion für den Fehler "mpnotify Clean Threat **\_ \_ \_ Start** / **mpnotify Clean \_ \_ Threat \_** failed", Fehler bei / **\_ Clean \_ Threat \_ failed** -Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="04cd3-115">Threat action for the **MPNOTIFY\_CLEAN\_THREAT\_START**/**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**/**MPNOTIFY\_CLEAN\_THREAT\_FAILED** events.</span></span> <span data-ttu-id="04cd3-116">Siehe [**mpthreat- \_ Aktion**](mpthreat-action.md).</span><span class="sxs-lookup"><span data-stu-id="04cd3-116">See [**MPTHREAT\_ACTION**](mpthreat-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="04cd3-117">**dwStatus**</span><span class="sxs-lookup"><span data-stu-id="04cd3-117">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="04cd3-118">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="04cd3-118">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="04cd3-119">Zusätzliche Status oder Aktionen, die der ausgeführten Aktion zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="04cd3-119">Additional status or actions associated with the action taken.</span></span> <span data-ttu-id="04cd3-120">Dies ist eine Kombination von Bitflags aus dem [**mpstatus- \_ Flag**](mpstatus-flag.md).</span><span class="sxs-lookup"><span data-stu-id="04cd3-120">This is a combination of bit flags from [**MPSTATUS\_FLAG**](mpstatus-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="04cd3-121">**ResourceInfo**</span><span class="sxs-lookup"><span data-stu-id="04cd3-121">**ResourceInfo**</span></span>
</dt> <dd>

<span data-ttu-id="04cd3-122">Typ: **pmpresource- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="04cd3-122">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="04cd3-123">In den Ressourcen Informationen für die **mpnotify- \_ Bereinigung \_ \_** wurde ein Fehler bei der Bereinigung der Bereinigung von Clean Threat / **\_ \_ \_** / **\_ \_ \_ failed** -Ereignissen gemeldet.</span><span class="sxs-lookup"><span data-stu-id="04cd3-123">Resource information for the **MPNOTIFY\_CLEAN\_THREAT\_START**/**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**/**MPNOTIFY\_CLEAN\_THREAT\_FAILED** events.</span></span> <span data-ttu-id="04cd3-124">Informationen finden Sie unter [**mpresource- \_ Informationen**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="04cd3-124">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="04cd3-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04cd3-125">Requirements</span></span>



| <span data-ttu-id="04cd3-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04cd3-126">Requirement</span></span> | <span data-ttu-id="04cd3-127">Wert</span><span class="sxs-lookup"><span data-stu-id="04cd3-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04cd3-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="04cd3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="04cd3-129">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04cd3-129">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="04cd3-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="04cd3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="04cd3-131">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04cd3-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="04cd3-132">Header</span><span class="sxs-lookup"><span data-stu-id="04cd3-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="04cd3-133"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="04cd3-133"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04cd3-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04cd3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04cd3-135">**mpresource- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="04cd3-135">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="04cd3-136">**\_mpstatusflag**</span><span class="sxs-lookup"><span data-stu-id="04cd3-136">**MPSTATUS\_FLAG**</span></span>](mpstatus-flag.md)
</dt> <dt>

[<span data-ttu-id="04cd3-137">**mpthreat- \_ Aktion**</span><span class="sxs-lookup"><span data-stu-id="04cd3-137">**MPTHREAT\_ACTION**</span></span>](mpthreat-action.md)
</dt> </dl>

 

 





