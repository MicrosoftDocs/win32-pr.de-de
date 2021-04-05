---
title: Modify-Methode der MicrosoftDNS_WINSType-Klasse
description: Die Modify-Methode aktualisiert einen Windows Internet Name Service (WINS)-Ressourcen Daten Satz.
ms.assetid: b61c429a-6b01-4b17-9312-bc5b69d1e76a
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_WINSType-Klasse
- DNS-MicrosoftDNS_WINSType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1469d1a9d50c72cdf3699bdc2ab9b96f51dfce86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859041"
---
# <a name="modify-method-of-the-microsoftdns_winstype-class"></a><span data-ttu-id="bd3cf-106">Modify-Methode der MicrosoftDNS- \_ winstype-Klasse</span><span class="sxs-lookup"><span data-stu-id="bd3cf-106">Modify method of the MicrosoftDNS\_WINSType class</span></span>

<span data-ttu-id="bd3cf-107">Die **Modify** -Methode aktualisiert einen Windows Internet Name Service (WINS)-Ressourcen Daten Satz.</span><span class="sxs-lookup"><span data-stu-id="bd3cf-107">The **Modify** method updates a Windows Internet Name Service (WINS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd3cf-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd3cf-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint32                MappingFlag,
  [in, optional] uint32                LookupTimeout,
  [in, optional] uint32                CacheTimeout,
  [in, optional] string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="bd3cf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd3cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd3cf-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="bd3cf-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bd3cf-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="bd3cf-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="bd3cf-112">*Mappingflag* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="bd3cf-112">*MappingFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bd3cf-113">WINS-ZuordnungsFlag, das angibt, ob der Datensatz in die Zonen Replikation eingeschlossen werden muss.</span><span class="sxs-lookup"><span data-stu-id="bd3cf-113">WINS mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="bd3cf-114">Sie kann nur zwei Werte aufweisen: 0x80000000 und 0x00010000 bis, die den Replikations-und No-Replication-Flags (local Record) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="bd3cf-114">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span> <span data-ttu-id="bd3cf-115">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="bd3cf-115">The following values are valid.</span></span>



| <span data-ttu-id="bd3cf-116">Wert</span><span class="sxs-lookup"><span data-stu-id="bd3cf-116">Value</span></span>                                                                                                                                               | <span data-ttu-id="bd3cf-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bd3cf-117">Meaning</span></span>                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <span data-ttu-id="bd3cf-118"><dt>**0x80000000**</dt></span><span class="sxs-lookup"><span data-stu-id="bd3cf-118"><dt>**0x80000000**</dt></span></span> </dl> | <span data-ttu-id="bd3cf-119">Replikationsflag</span><span class="sxs-lookup"><span data-stu-id="bd3cf-119">Replication flag</span></span><br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <span data-ttu-id="bd3cf-120"><dt>**0x00010000**</dt></span><span class="sxs-lookup"><span data-stu-id="bd3cf-120"><dt>**0x00010000**</dt></span></span> </dl> | <span data-ttu-id="bd3cf-121">Flag "keine Replikation (lokaler Datensatz)"</span><span class="sxs-lookup"><span data-stu-id="bd3cf-121">No-replication (local record) flag</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bd3cf-122">*Lookuptimeout* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="bd3cf-122">*LookupTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bd3cf-123">Zeit (in Sekunden), die ein DNS-Server versucht, mithilfe von WINS eine Auflösung durchsuchen zu können.</span><span class="sxs-lookup"><span data-stu-id="bd3cf-123">Time, in seconds, that a DNS Server attempts resolution using WINS Look up.</span></span>

</dd> <dt>

<span data-ttu-id="bd3cf-124">*Cachetimeout* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="bd3cf-124">*CacheTimeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bd3cf-125">Zeit in Sekunden, für die ein DNS-Server mit WINS-Suche die Antwort des WINS-Servers zwischenspeichern kann.</span><span class="sxs-lookup"><span data-stu-id="bd3cf-125">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="bd3cf-126">*Windows Server* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="bd3cf-126">*WinsServers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bd3cf-127">Liste mit durch Trennzeichen getrennten IP-Adressen von WINS-Servern, die in WINS-suchen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bd3cf-127">List of comma-separated IP addresses of WINS servers used in WINS Look ups.</span></span>

</dd> <dt>

<span data-ttu-id="bd3cf-128">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="bd3cf-128">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="bd3cf-129">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="bd3cf-129">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd3cf-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd3cf-130">Return value</span></span>

<span data-ttu-id="bd3cf-131">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bd3cf-131">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd3cf-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd3cf-132">Remarks</span></span>

<span data-ttu-id="bd3cf-133">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="bd3cf-133">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd3cf-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd3cf-134">Requirements</span></span>



| <span data-ttu-id="bd3cf-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd3cf-135">Requirement</span></span> | <span data-ttu-id="bd3cf-136">Wert</span><span class="sxs-lookup"><span data-stu-id="bd3cf-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd3cf-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd3cf-137">Minimum supported client</span></span><br/> | <span data-ttu-id="bd3cf-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bd3cf-138">None supported</span></span><br/>                                                              |
| <span data-ttu-id="bd3cf-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd3cf-139">Minimum supported server</span></span><br/> | <span data-ttu-id="bd3cf-140">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd3cf-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bd3cf-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="bd3cf-141">Namespace</span></span><br/>                | <span data-ttu-id="bd3cf-142">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="bd3cf-142">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="bd3cf-143">MOF</span><span class="sxs-lookup"><span data-stu-id="bd3cf-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd3cf-144"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bd3cf-144"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd3cf-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd3cf-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd3cf-146">**MicrosoftDNS \_ winstype**</span><span class="sxs-lookup"><span data-stu-id="bd3cf-146">**MicrosoftDNS\_WINSType**</span></span>](microsoftdns-winstype.md)
</dt> <dt>

[<span data-ttu-id="bd3cf-147">**Methode "kreateinzustancefrompropertydata" der MicrosoftDNS- \_ winstype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="bd3cf-147">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="bd3cf-148">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="bd3cf-148">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





