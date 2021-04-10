---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_WINSRType-Klasse
description: Die Methode "kreateinstancefrompropertydata" instanziiert einen WINS-Ressourcen Eintrag (Reverse Lookup, WINSR).
ms.assetid: e14e81be-fc5c-4a6f-b6d1-cb3ce5005e00
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_WINSRType
- DNS-MicrosoftDNS_WINSRType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c35863e00ace6c0772383604d0fbdfd7915cd02c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104732"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_winsrtype-class"></a><span data-ttu-id="d6ecd-106">Die Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ Klasse "winsrtype"</span><span class="sxs-lookup"><span data-stu-id="d6ecd-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_WINSRType class</span></span>

<span data-ttu-id="d6ecd-107">Die Methode " **kreateinstancefrompropertydata** " instanziiert einen WINS-Ressourcen Eintrag (Reverse Lookup, WINSR).</span><span class="sxs-lookup"><span data-stu-id="d6ecd-107">The **CreateInstanceFromPropertyData** method instantiates a WINS Reverse Lookup (WINSR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6ecd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6ecd-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           uint32                 MappingFlag,
  [in]           uint32                 LookupTimeout,
  [in]           uint32                 CacheTimeout,
  [in]           string                 ResultDomain,
  [out, ref]     MicrosoftDNS_WINSRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="d6ecd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6ecd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6ecd-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6ecd-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ecd-111">Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="d6ecd-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="d6ecd-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6ecd-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ecd-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="d6ecd-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="d6ecd-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6ecd-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ecd-115">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="d6ecd-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="d6ecd-116">*Recordclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="d6ecd-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ecd-117">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="d6ecd-117">Class of the RR.</span></span> <span data-ttu-id="d6ecd-118">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="d6ecd-118">Default value is 1.</span></span> <span data-ttu-id="d6ecd-119">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="d6ecd-119">The following values are valid.</span></span>



| <span data-ttu-id="d6ecd-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d6ecd-120">Value</span></span>                                                                                                | <span data-ttu-id="d6ecd-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d6ecd-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="d6ecd-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="d6ecd-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="d6ecd-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="d6ecd-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="d6ecd-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="d6ecd-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="d6ecd-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="d6ecd-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="d6ecd-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="d6ecd-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="d6ecd-127">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="d6ecd-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="d6ecd-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="d6ecd-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="d6ecd-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="d6ecd-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="d6ecd-130">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="d6ecd-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ecd-131">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d6ecd-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="d6ecd-132">*Mappingflag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6ecd-132">*MappingFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ecd-133">Das WINSR-ZuordnungsFlag, das angibt, ob der Datensatz in die Zonen Replikation eingeschlossen werden muss.</span><span class="sxs-lookup"><span data-stu-id="d6ecd-133">WINSR mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="d6ecd-134">Sie kann nur zwei Werte aufweisen: 0x80000000 und 0x00010000 bis, die den Replikations-und No-Replication-Flags (local Record) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d6ecd-134">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="d6ecd-135">*Lookuptimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6ecd-135">*LookupTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ecd-136">Timeout (in Sekunden) für einen DNS-Server mit umgekehrter WINS-Suche.</span><span class="sxs-lookup"><span data-stu-id="d6ecd-136">Time out, in seconds, for a DNS Server using WINS Reverse Look up.</span></span>

</dd> <dt>

<span data-ttu-id="d6ecd-137">*Cachetimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6ecd-137">*CacheTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ecd-138">Die Zeit in Sekunden, in der ein DNS-Server mit WINS-Suche die Antwort des WINS-Servers zwischenspeichern kann.</span><span class="sxs-lookup"><span data-stu-id="d6ecd-138">Time, in seconds, a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="d6ecd-139">*Resultdomain* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6ecd-139">*ResultDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ecd-140">Domänen Name, der an zurückgegebene NetBIOS-Namen angehängt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6ecd-140">Domain name to append to returned NetBIOS names.</span></span>

</dd> <dt>

<span data-ttu-id="d6ecd-141">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="d6ecd-141">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ecd-142">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d6ecd-142">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6ecd-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6ecd-143">Return value</span></span>

<span data-ttu-id="d6ecd-144">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d6ecd-144">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6ecd-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6ecd-145">Requirements</span></span>



| <span data-ttu-id="d6ecd-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6ecd-146">Requirement</span></span> | <span data-ttu-id="d6ecd-147">Wert</span><span class="sxs-lookup"><span data-stu-id="d6ecd-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6ecd-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6ecd-148">Minimum supported client</span></span><br/> | <span data-ttu-id="d6ecd-149">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d6ecd-149">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d6ecd-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6ecd-150">Minimum supported server</span></span><br/> | <span data-ttu-id="d6ecd-151">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6ecd-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d6ecd-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="d6ecd-152">Namespace</span></span><br/>                | <span data-ttu-id="d6ecd-153">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="d6ecd-153">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d6ecd-154">MOF</span><span class="sxs-lookup"><span data-stu-id="d6ecd-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6ecd-155"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d6ecd-155"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6ecd-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6ecd-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6ecd-157">**MicrosoftDNS \_ winsrtype**</span><span class="sxs-lookup"><span data-stu-id="d6ecd-157">**MicrosoftDNS\_WINSRType**</span></span>](microsoftdns-winsrtype.md)
</dt> <dt>

[<span data-ttu-id="d6ecd-158">**Modify-Methode der MicrosoftDNS \_ winsrtype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d6ecd-158">**Modify Method of the MicrosoftDNS\_WINSRType Class**</span></span>](microsoftdns-winsrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="d6ecd-159">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="d6ecd-159">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





