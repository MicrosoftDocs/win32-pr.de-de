---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_NXTType-Klasse
description: Die Methode "kreatinstancefrompropertydata" instanziiert einen nächsten (NXT) Ressourcen Eintrag.
ms.assetid: d0e4f3bf-f835-4341-a614-539975e6be11
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_NXTType
- DNS-MicrosoftDNS_NXTType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fee00cd0afdb6ac629a981dbdb586a30252eac1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477523"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_nxttype-class"></a><span data-ttu-id="deae1-106">Die Methode "kreateinzustancefrompropertydata" der Klasse "MicrosoftDNS \_ nxttype"</span><span class="sxs-lookup"><span data-stu-id="deae1-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_NXTType class</span></span>

<span data-ttu-id="deae1-107">Die Methode " **kreatinstancefrompropertydata** " instanziiert einen nächsten (NXT) Ressourcen Eintrag.</span><span class="sxs-lookup"><span data-stu-id="deae1-107">The **CreateInstanceFromPropertyData** method instantiates a Next (NXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="deae1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="deae1-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               NextDomainName,
  [in]           string               Types,
  [out, ref]     MicrosoftDNS_NXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="deae1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="deae1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deae1-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="deae1-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deae1-111">Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="deae1-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="deae1-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="deae1-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deae1-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="deae1-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="deae1-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="deae1-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deae1-115">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="deae1-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="deae1-116">*Recordclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="deae1-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="deae1-117">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="deae1-117">Class of the RR.</span></span> <span data-ttu-id="deae1-118">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="deae1-118">Default value is 1.</span></span> <span data-ttu-id="deae1-119">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="deae1-119">The following values are valid.</span></span>



| <span data-ttu-id="deae1-120">Wert</span><span class="sxs-lookup"><span data-stu-id="deae1-120">Value</span></span>                                                                                                | <span data-ttu-id="deae1-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="deae1-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="deae1-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="deae1-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="deae1-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="deae1-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="deae1-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="deae1-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="deae1-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="deae1-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="deae1-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="deae1-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="deae1-127">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="deae1-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="deae1-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="deae1-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="deae1-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="deae1-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="deae1-130">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="deae1-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="deae1-131">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="deae1-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="deae1-132">*Nextdomainname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="deae1-132">*NextDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deae1-133">Der nächste Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="deae1-133">Next domain name.</span></span>

</dd> <dt>

<span data-ttu-id="deae1-134">*Typen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="deae1-134">*Types* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deae1-135">Durch Leerzeichen getrennte Liste der RR-Type-mnetmonics für den Besitzer Namen des NXT-Ressourcen Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="deae1-135">Space-separated list of the RR-type mnemonics for the owner name of the NXT Resource Record.</span></span>

</dd> <dt>

<span data-ttu-id="deae1-136">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="deae1-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="deae1-137">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="deae1-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deae1-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="deae1-138">Return value</span></span>

<span data-ttu-id="deae1-139">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="deae1-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="deae1-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="deae1-140">Requirements</span></span>



| <span data-ttu-id="deae1-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="deae1-141">Requirement</span></span> | <span data-ttu-id="deae1-142">Wert</span><span class="sxs-lookup"><span data-stu-id="deae1-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="deae1-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="deae1-143">Minimum supported client</span></span><br/> | <span data-ttu-id="deae1-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="deae1-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="deae1-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="deae1-145">Minimum supported server</span></span><br/> | <span data-ttu-id="deae1-146">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="deae1-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="deae1-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="deae1-147">Namespace</span></span><br/>                | <span data-ttu-id="deae1-148">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="deae1-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="deae1-149">MOF</span><span class="sxs-lookup"><span data-stu-id="deae1-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="deae1-150"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="deae1-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="deae1-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="deae1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deae1-152">**MicrosoftDNS \_ nxttype**</span><span class="sxs-lookup"><span data-stu-id="deae1-152">**MicrosoftDNS\_NXTType**</span></span>](microsoftdns-nxttype.md)
</dt> <dt>

[<span data-ttu-id="deae1-153">**Modify-Methode der MicrosoftDNS- \_ nxttype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="deae1-153">**Modify Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-modify.md)
</dt> <dt>

[<span data-ttu-id="deae1-154">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="deae1-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





