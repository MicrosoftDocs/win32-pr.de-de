---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_CNAMEType-Klasse
description: Die Methode "kreateinstancefrompropertydata" instanziiert einen kanonischen Namens Ressourcen Eintrag (CNAME).
ms.assetid: b5a5e14a-fb30-4cdf-90d0-7ef446350ac6
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_CNAMEType
- DNS-MicrosoftDNS_CNAMEType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aceb65a76002651e98dd8751e0a5c0c56aca3e1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956472"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_cnametype-class"></a><span data-ttu-id="d1be7-106">Die Methode "kreatinstancefrompropertydata" der MicrosoftDNS \_ cnametype-Klasse</span><span class="sxs-lookup"><span data-stu-id="d1be7-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_CNAMEType class</span></span>

<span data-ttu-id="d1be7-107">Die Methode " **kreateinstancefrompropertydata** " instanziiert einen kanonischen Namens Ressourcen Eintrag (CNAME).</span><span class="sxs-lookup"><span data-stu-id="d1be7-107">The **CreateInstanceFromPropertyData** method instantiates a Canonical Name (CNAME) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1be7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1be7-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           string                 PrimaryName,
  [out, ref]     MicrosoftDNS_CNAMEType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="d1be7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1be7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1be7-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1be7-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1be7-111">Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="d1be7-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="d1be7-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1be7-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1be7-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="d1be7-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="d1be7-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1be7-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1be7-115">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="d1be7-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="d1be7-116">*Recordclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="d1be7-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d1be7-117">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="d1be7-117">Class of the RR.</span></span> <span data-ttu-id="d1be7-118">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="d1be7-118">Default value is 1.</span></span> <span data-ttu-id="d1be7-119">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="d1be7-119">The following values are valid.</span></span>



| <span data-ttu-id="d1be7-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d1be7-120">Value</span></span>                                                                                                | <span data-ttu-id="d1be7-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d1be7-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="d1be7-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="d1be7-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="d1be7-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="d1be7-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="d1be7-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="d1be7-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="d1be7-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="d1be7-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="d1be7-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="d1be7-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="d1be7-127">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="d1be7-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="d1be7-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="d1be7-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="d1be7-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="d1be7-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="d1be7-130">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="d1be7-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d1be7-131">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d1be7-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="d1be7-132">*Primaryname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1be7-132">*PrimaryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1be7-133">Primärer Name des CNAME RR.</span><span class="sxs-lookup"><span data-stu-id="d1be7-133">Primary name of the CNAME RR.</span></span>

</dd> <dt>

<span data-ttu-id="d1be7-134">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="d1be7-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d1be7-135">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d1be7-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1be7-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1be7-136">Return value</span></span>

<span data-ttu-id="d1be7-137">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d1be7-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1be7-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1be7-138">Requirements</span></span>



| <span data-ttu-id="d1be7-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1be7-139">Requirement</span></span> | <span data-ttu-id="d1be7-140">Wert</span><span class="sxs-lookup"><span data-stu-id="d1be7-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1be7-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d1be7-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d1be7-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d1be7-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d1be7-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d1be7-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d1be7-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1be7-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d1be7-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1be7-145">Namespace</span></span><br/>                | <span data-ttu-id="d1be7-146">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="d1be7-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d1be7-147">MOF</span><span class="sxs-lookup"><span data-stu-id="d1be7-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1be7-148"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d1be7-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1be7-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1be7-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1be7-150">**MicrosoftDNS \_ cnametype**</span><span class="sxs-lookup"><span data-stu-id="d1be7-150">**MicrosoftDNS\_CNAMEType**</span></span>](microsoftdns-cnametype.md)
</dt> <dt>

[<span data-ttu-id="d1be7-151">**Modify-Methode der MicrosoftDNS \_ cnametype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d1be7-151">**Modify Method of the MicrosoftDNS\_CNAMEType Class**</span></span>](microsoftdns-cnametype-modify.md)
</dt> <dt>

[<span data-ttu-id="d1be7-152">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="d1be7-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





