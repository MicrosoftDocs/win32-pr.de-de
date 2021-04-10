---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_MFType-Klasse
description: Die Methode "kreatinstancefrompropertydata" instanziiert einen e-Mail-Weiterleitungs-Agent für eine Domänen Ressource (MF).
ms.assetid: e669d065-bfba-4a86-8519-2317e03ed4ee
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_MFType
- DNS-MicrosoftDNS_MFType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26cafc766a6ea6419432b279f5389721f6572b44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956444"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mftype-class"></a><span data-ttu-id="c5d30-106">Methode "kreateinzustancefrompropertydata" der MicrosoftDNS- \_ Klasse "mftype"</span><span class="sxs-lookup"><span data-stu-id="c5d30-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MFType class</span></span>

<span data-ttu-id="c5d30-107">Die Methode " **kreatinstancefrompropertydata** " instanziiert einen e-Mail-Weiterleitungs-Agent für eine Domänen Ressource (MF).</span><span class="sxs-lookup"><span data-stu-id="c5d30-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Forwarding Agent for Domain (MF) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5d30-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5d30-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              MFHost,
  [out, ref]     MicrosoftDNS_MFType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="c5d30-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5d30-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5d30-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5d30-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5d30-111">Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="c5d30-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="c5d30-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5d30-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5d30-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="c5d30-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="c5d30-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5d30-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5d30-115">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="c5d30-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="c5d30-116">*Recordclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c5d30-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c5d30-117">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="c5d30-117">Class of the RR.</span></span> <span data-ttu-id="c5d30-118">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="c5d30-118">Default value is 1.</span></span> <span data-ttu-id="c5d30-119">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="c5d30-119">The following values are valid.</span></span>



| <span data-ttu-id="c5d30-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c5d30-120">Value</span></span>                                                                                                | <span data-ttu-id="c5d30-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c5d30-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="c5d30-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c5d30-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="c5d30-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="c5d30-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="c5d30-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="c5d30-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="c5d30-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="c5d30-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="c5d30-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="c5d30-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="c5d30-127">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="c5d30-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="c5d30-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="c5d30-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="c5d30-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="c5d30-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="c5d30-130">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c5d30-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c5d30-131">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c5d30-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="c5d30-132">*MF-Host* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5d30-132">*MFHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5d30-133">Der Name des Hosts, der den postweiterleitungs-Agent bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c5d30-133">Name of the host that provides the mail forwarding agent.</span></span>

</dd> <dt>

<span data-ttu-id="c5d30-134">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="c5d30-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c5d30-135">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c5d30-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5d30-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5d30-136">Return value</span></span>

<span data-ttu-id="c5d30-137">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c5d30-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5d30-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5d30-138">Requirements</span></span>



| <span data-ttu-id="c5d30-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5d30-139">Requirement</span></span> | <span data-ttu-id="c5d30-140">Wert</span><span class="sxs-lookup"><span data-stu-id="c5d30-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5d30-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5d30-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c5d30-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c5d30-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c5d30-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5d30-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c5d30-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5d30-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c5d30-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5d30-145">Namespace</span></span><br/>                | <span data-ttu-id="c5d30-146">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="c5d30-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c5d30-147">MOF</span><span class="sxs-lookup"><span data-stu-id="c5d30-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5d30-148"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c5d30-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5d30-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5d30-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5d30-150">**MicrosoftDNS- \_ mftype**</span><span class="sxs-lookup"><span data-stu-id="c5d30-150">**MicrosoftDNS\_MFType**</span></span>](microsoftdns-mftype.md)
</dt> <dt>

[<span data-ttu-id="c5d30-151">**Modify-Methode der MicrosoftDNS \_ mftype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c5d30-151">**Modify Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-modify.md)
</dt> <dt>

[<span data-ttu-id="c5d30-152">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="c5d30-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





