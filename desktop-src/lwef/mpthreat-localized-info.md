---
title: MPTHREAT_LOCALIZED_INFO Struktur (mpclient. h)
description: Lokalisierte Informationen zu einer Bedrohung.
ms.assetid: 99DC9737-9A61-4407-B544-A7A979C5B556
keywords:
- MPTHREAT_LOCALIZED_INFO Struktur Funktionen der Legacy-Windows-Umgebung
- PMPTHREAT_LOCALIZED_INFO Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPTHREAT_LOCALIZED_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87ea0bee7c8cae15389b40b64038aad92a56dd5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391883"
---
# <a name="mpthreat_localized_info-structure"></a><span data-ttu-id="a0759-105">Lokalisierte mpthreat- \_ \_ Informationsstruktur</span><span class="sxs-lookup"><span data-stu-id="a0759-105">MPTHREAT\_LOCALIZED\_INFO structure</span></span>

<span data-ttu-id="a0759-106">Lokalisierte Informationen zu einer Bedrohung.</span><span class="sxs-lookup"><span data-stu-id="a0759-106">Localized information for a threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0759-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0759-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_LOCALIZED_INFO {
  MPTHREAT_ID           ThreatID;
  MP_MIDL_STRING LPWSTR CategoryName;
  MP_MIDL_STRING LPWSTR CategoryDescription;
  MP_MIDL_STRING LPWSTR SeverityName;
  MP_MIDL_STRING LPWSTR SeverityDescription;
  MP_MIDL_STRING LPWSTR ShortDescription;
  MP_MIDL_STRING LPWSTR DefaultActionName;;
  MP_MIDL_STRING LPWSTR Advice;
  MP_MIDL_STRING LPWSTR ThreatUrl;
} MPTHREAT_LOCALIZED_INFO, *PMPTHREAT_LOCALIZED_INFO;
```



## <a name="members"></a><span data-ttu-id="a0759-108">Member</span><span class="sxs-lookup"><span data-stu-id="a0759-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a0759-109">**Threatid**</span><span class="sxs-lookup"><span data-stu-id="a0759-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="a0759-110">Typ: **mpthreat- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="a0759-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="a0759-111">Bedrohungs Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="a0759-111">Threat identifier.</span></span> <span data-ttu-id="a0759-112">Das obere Bit ist festgelegt, um antivirenbezogene Bedrohungen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a0759-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="a0759-113">**CategoryName**</span><span class="sxs-lookup"><span data-stu-id="a0759-113">**CategoryName**</span></span>
</dt> <dd>

<span data-ttu-id="a0759-114">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a0759-114">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="a0759-115">Bedrohungs Klassifizierung, z. b. ein Trojaner oder eine Keylogger.</span><span class="sxs-lookup"><span data-stu-id="a0759-115">Threat classification, such as a trojan or a keylogger.</span></span>

</dd> <dt>

<span data-ttu-id="a0759-116">**Categorydescription**</span><span class="sxs-lookup"><span data-stu-id="a0759-116">**CategoryDescription**</span></span>
</dt> <dd>

<span data-ttu-id="a0759-117">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a0759-117">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="a0759-118">Beschreibung der Bedrohungs Kategorie.</span><span class="sxs-lookup"><span data-stu-id="a0759-118">Description of threat category.</span></span>

</dd> <dt>

<span data-ttu-id="a0759-119">**Schweregrad Name**</span><span class="sxs-lookup"><span data-stu-id="a0759-119">**SeverityName**</span></span>
</dt> <dd>

<span data-ttu-id="a0759-120">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a0759-120">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="a0759-121">Bedrohungs Schweregrad, z. b. schwerwiegend oder Mittel.</span><span class="sxs-lookup"><span data-stu-id="a0759-121">Threat severity level, such as severe or moderate.</span></span>

</dd> <dt>

<span data-ttu-id="a0759-122">**"Severitydescription"**</span><span class="sxs-lookup"><span data-stu-id="a0759-122">**SeverityDescription**</span></span>
</dt> <dd>

<span data-ttu-id="a0759-123">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a0759-123">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="a0759-124">Beschreibung des Bedrohungs schwere Grads.</span><span class="sxs-lookup"><span data-stu-id="a0759-124">Description of threat severity level.</span></span>

</dd> <dt>

<span data-ttu-id="a0759-125">**Kurzbeschreibung**</span><span class="sxs-lookup"><span data-stu-id="a0759-125">**ShortDescription**</span></span>
</dt> <dd>

<span data-ttu-id="a0759-126">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a0759-126">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="a0759-127">Kurze Beschreibung der Bedrohung.</span><span class="sxs-lookup"><span data-stu-id="a0759-127">Short description of threat.</span></span>

</dd> <dt>

<span data-ttu-id="a0759-128">**Defaultactionname;**</span><span class="sxs-lookup"><span data-stu-id="a0759-128">**DefaultActionName;**</span></span>
</dt> <dd>

<span data-ttu-id="a0759-129">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a0759-129">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="a0759-130">Der Name der Standardaktion, wie z. b. Remove oder Quarantäne, von der Engine vorgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="a0759-130">Name of default action, such as remove or quarantine, suggested by engine.</span></span>

</dd> <dt>

<span data-ttu-id="a0759-131">**Advice**</span><span class="sxs-lookup"><span data-stu-id="a0759-131">**Advice**</span></span>
</dt> <dd>

<span data-ttu-id="a0759-132">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a0759-132">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="a0759-133">Ratschläge für eine bestimmte Bedrohung.</span><span class="sxs-lookup"><span data-stu-id="a0759-133">Advice for the particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="a0759-134">**"-URL"**</span><span class="sxs-lookup"><span data-stu-id="a0759-134">**ThreatUrl**</span></span>
</dt> <dd>

<span data-ttu-id="a0759-135">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a0759-135">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="a0759-136">Eine URL zu einer Webseite, die Informationen über die Bedrohung enthält.</span><span class="sxs-lookup"><span data-stu-id="a0759-136">A URL to a webpage containing information about the threat.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0759-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0759-137">Requirements</span></span>



| <span data-ttu-id="a0759-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0759-138">Requirement</span></span> | <span data-ttu-id="a0759-139">Wert</span><span class="sxs-lookup"><span data-stu-id="a0759-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0759-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a0759-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a0759-141">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a0759-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a0759-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a0759-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a0759-143">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a0759-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a0759-144">Header</span><span class="sxs-lookup"><span data-stu-id="a0759-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0759-145"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0759-145"><dt>MpClient.h</dt></span></span> </dl> |



 

 





