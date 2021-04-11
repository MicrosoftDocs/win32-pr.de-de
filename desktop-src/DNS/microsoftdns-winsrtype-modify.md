---
title: Modify-Methode der MicrosoftDNS_WINSRType-Klasse
description: Die Modify-Methode aktualisiert einen WINS-Ressourcen Daten Satz (Reverse-Suche).
ms.assetid: 28be0045-5b0d-4434-a2a9-b56191f1e213
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_WINSRType-Klasse
- DNS-MicrosoftDNS_WINSRType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02d89c3cd191262136035f9006853e2f1a7f7dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105933"
---
# <a name="modify-method-of-the-microsoftdns_winsrtype-class"></a><span data-ttu-id="b23cf-106">Modify-Methode der MicrosoftDNS \_ winsrtype-Klasse</span><span class="sxs-lookup"><span data-stu-id="b23cf-106">Modify method of the MicrosoftDNS\_WINSRType class</span></span>

<span data-ttu-id="b23cf-107">Die **Modify** -Methode aktualisiert einen WINS-Ressourcen Daten Satz (Reverse-Suche).</span><span class="sxs-lookup"><span data-stu-id="b23cf-107">The **Modify** method updates a WINS Reverse Look up (WINSR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="b23cf-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b23cf-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint32                 MappingFlag,
  [in, optional] uint32                 LookupTimeout,
  [in, optional] uint32                 CacheTimeout,
  [in, optional] string                 ResultDomain,
  [out, ref]     MicrosoftDNS_WINSRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="b23cf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b23cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b23cf-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b23cf-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b23cf-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b23cf-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="b23cf-112">*Mappingflag* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b23cf-112">*MappingFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b23cf-113">Das WINSR-ZuordnungsFlag, das angibt, ob der Datensatz in die Zonen Replikation eingeschlossen werden muss.</span><span class="sxs-lookup"><span data-stu-id="b23cf-113">WINSR mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="b23cf-114">Sie kann nur zwei Werte aufweisen: 0x80000000 und 0x00010000 bis, die den Replikations-und No-Replication-Flags (local Record) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b23cf-114">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="b23cf-115">*Lookuptimeout* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b23cf-115">*LookupTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b23cf-116">Timeout (in Sekunden) für einen DNS-Server mit umgekehrter WINS-Suche.</span><span class="sxs-lookup"><span data-stu-id="b23cf-116">Time out, in seconds, for a DNS Server using WINS Reverse Look up.</span></span>

</dd> <dt>

<span data-ttu-id="b23cf-117">*Cachetimeout* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b23cf-117">*CacheTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b23cf-118">Die Zeit in Sekunden, in der ein DNS-Server mit WINS-Suche die Antwort des WINS-Servers zwischenspeichern kann.</span><span class="sxs-lookup"><span data-stu-id="b23cf-118">Time, in seconds, a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="b23cf-119">*Resultdomain* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b23cf-119">*ResultDomain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b23cf-120">Domänen Name, der an zurückgegebene NetBIOS-Namen angehängt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b23cf-120">Domain name to append to returned NetBIOS names.</span></span>

</dd> <dt>

<span data-ttu-id="b23cf-121">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="b23cf-121">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="b23cf-122">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b23cf-122">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b23cf-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b23cf-123">Return value</span></span>

<span data-ttu-id="b23cf-124">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b23cf-124">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b23cf-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b23cf-125">Remarks</span></span>

<span data-ttu-id="b23cf-126">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="b23cf-126">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="b23cf-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b23cf-127">Requirements</span></span>



| <span data-ttu-id="b23cf-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b23cf-128">Requirement</span></span> | <span data-ttu-id="b23cf-129">Wert</span><span class="sxs-lookup"><span data-stu-id="b23cf-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b23cf-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b23cf-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b23cf-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b23cf-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b23cf-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b23cf-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b23cf-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b23cf-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b23cf-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="b23cf-134">Namespace</span></span><br/>                | <span data-ttu-id="b23cf-135">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="b23cf-135">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="b23cf-136">MOF</span><span class="sxs-lookup"><span data-stu-id="b23cf-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b23cf-137"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b23cf-137"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b23cf-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b23cf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b23cf-139">**MicrosoftDNS \_ winsrtype**</span><span class="sxs-lookup"><span data-stu-id="b23cf-139">**MicrosoftDNS\_WINSRType**</span></span>](microsoftdns-winsrtype.md)
</dt> <dt>

[<span data-ttu-id="b23cf-140">**Die Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ Klasse "winsrtype"**</span><span class="sxs-lookup"><span data-stu-id="b23cf-140">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="b23cf-141">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="b23cf-141">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





