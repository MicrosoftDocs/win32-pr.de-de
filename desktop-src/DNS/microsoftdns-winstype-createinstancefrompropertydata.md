---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_WINSType-Klasse
description: Die Methode "kreateinstancefrompropertydata" instanziiert einen WINS-Ressourcen Eintrag (Windows Internet Name Service).
ms.assetid: 0b41a6a5-0bb1-467b-9089-2c721d521887
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_WINSType
- DNS-MicrosoftDNS_WINSType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf584bd34f59391a49fd5f7ec13cb49e18ef68fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742248"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_winstype-class"></a><span data-ttu-id="3bba7-106">Methode "kreateinzustancefrompropertydata" der MicrosoftDNS- \_ winstype-Klasse</span><span class="sxs-lookup"><span data-stu-id="3bba7-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_WINSType class</span></span>

<span data-ttu-id="3bba7-107">Die Methode " **kreateinstancefrompropertydata** " instanziiert einen WINS-Ressourcen Eintrag (Windows Internet Name Service).</span><span class="sxs-lookup"><span data-stu-id="3bba7-107">The **CreateInstanceFromPropertyData** method instantiates a Windows Internet Name Service (WINS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bba7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3bba7-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           uint32                MappingFlag,
  [in]           uint32                LookupTimeout,
  [in]           uint32                CacheTimeout,
  [in]           string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="3bba7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3bba7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bba7-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3bba7-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bba7-111">Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="3bba7-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="3bba7-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3bba7-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bba7-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="3bba7-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="3bba7-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3bba7-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bba7-115">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="3bba7-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="3bba7-116">*Recordclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3bba7-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3bba7-117">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="3bba7-117">Class of the RR.</span></span> <span data-ttu-id="3bba7-118">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="3bba7-118">Default value is 1.</span></span> <span data-ttu-id="3bba7-119">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="3bba7-119">The following values are valid.</span></span>



| <span data-ttu-id="3bba7-120">Wert</span><span class="sxs-lookup"><span data-stu-id="3bba7-120">Value</span></span>                                                                                                | <span data-ttu-id="3bba7-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3bba7-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="3bba7-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="3bba7-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="3bba7-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="3bba7-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="3bba7-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="3bba7-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="3bba7-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="3bba7-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="3bba7-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="3bba7-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="3bba7-127">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="3bba7-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="3bba7-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="3bba7-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="3bba7-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="3bba7-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="3bba7-130">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3bba7-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3bba7-131">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="3bba7-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="3bba7-132">*Mappingflag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3bba7-132">*MappingFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bba7-133">WINS-ZuordnungsFlag, das angibt, ob der Datensatz in die Zonen Replikation eingeschlossen werden muss.</span><span class="sxs-lookup"><span data-stu-id="3bba7-133">WINS mapping flag that specifies whether the record must be included into the zone replication.</span></span> <span data-ttu-id="3bba7-134">Sie kann nur zwei Werte aufweisen: 0x80000000 und 0x00010000 bis, die den Replikations-und No-Replication-Flags (local Record) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3bba7-134">It may have only two values: 0x80000000 and 0x00010000 corresponding to the replication and no-replication (local record) flags, respectively.</span></span> <span data-ttu-id="3bba7-135">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="3bba7-135">The following values are valid.</span></span>



| <span data-ttu-id="3bba7-136">Wert</span><span class="sxs-lookup"><span data-stu-id="3bba7-136">Value</span></span>                                                                                                                                               | <span data-ttu-id="3bba7-137">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3bba7-137">Meaning</span></span>                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <span data-ttu-id="3bba7-138"><dt>**0x80000000**</dt></span><span class="sxs-lookup"><span data-stu-id="3bba7-138"><dt>**0x80000000**</dt></span></span> </dl> | <span data-ttu-id="3bba7-139">Replikationsflag</span><span class="sxs-lookup"><span data-stu-id="3bba7-139">Replication flag</span></span><br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <span data-ttu-id="3bba7-140"><dt>**0x00010000**</dt></span><span class="sxs-lookup"><span data-stu-id="3bba7-140"><dt>**0x00010000**</dt></span></span> </dl> | <span data-ttu-id="3bba7-141">Flag "keine Replikation (lokaler Datensatz)"</span><span class="sxs-lookup"><span data-stu-id="3bba7-141">No-replication (local record) flag</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3bba7-142">*Lookuptimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3bba7-142">*LookupTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bba7-143">Zeit (in Sekunden), die ein DNS-Server versucht, mithilfe von WINS eine Auflösung durchsuchen zu können.</span><span class="sxs-lookup"><span data-stu-id="3bba7-143">Time, in seconds, that a DNS Server attempts resolution using WINS Look up.</span></span>

</dd> <dt>

<span data-ttu-id="3bba7-144">*Cachetimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3bba7-144">*CacheTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bba7-145">Zeit in Sekunden, für die ein DNS-Server mit WINS-Suche die Antwort des WINS-Servers zwischenspeichern kann.</span><span class="sxs-lookup"><span data-stu-id="3bba7-145">Time, in seconds, that a DNS Server using WINS Look up may cache the WINS server's response.</span></span>

</dd> <dt>

<span data-ttu-id="3bba7-146">*Windows Server* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3bba7-146">*WinsServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bba7-147">Liste mit durch Trennzeichen getrennten IP-Adressen von WINS-Servern, die in WINS-suchen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3bba7-147">List of comma-separated IP addresses of WINS servers used in WINS Look ups.</span></span>

</dd> <dt>

<span data-ttu-id="3bba7-148">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="3bba7-148">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="3bba7-149">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3bba7-149">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bba7-150">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3bba7-150">Return value</span></span>

<span data-ttu-id="3bba7-151">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3bba7-151">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bba7-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3bba7-152">Requirements</span></span>



| <span data-ttu-id="3bba7-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3bba7-153">Requirement</span></span> | <span data-ttu-id="3bba7-154">Wert</span><span class="sxs-lookup"><span data-stu-id="3bba7-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bba7-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3bba7-155">Minimum supported client</span></span><br/> | <span data-ttu-id="3bba7-156">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3bba7-156">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3bba7-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3bba7-157">Minimum supported server</span></span><br/> | <span data-ttu-id="3bba7-158">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3bba7-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3bba7-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="3bba7-159">Namespace</span></span><br/>                | <span data-ttu-id="3bba7-160">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="3bba7-160">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="3bba7-161">MOF</span><span class="sxs-lookup"><span data-stu-id="3bba7-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3bba7-162"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3bba7-162"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bba7-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bba7-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bba7-164">**MicrosoftDNS \_ winstype**</span><span class="sxs-lookup"><span data-stu-id="3bba7-164">**MicrosoftDNS\_WINSType**</span></span>](microsoftdns-winstype.md)
</dt> <dt>

[<span data-ttu-id="3bba7-165">**Modify-Methode der MicrosoftDNS- \_ winstype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3bba7-165">**Modify Method of the MicrosoftDNS\_WINSType Class**</span></span>](microsoftdns-winstype-modify.md)
</dt> <dt>

[<span data-ttu-id="3bba7-166">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="3bba7-166">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





