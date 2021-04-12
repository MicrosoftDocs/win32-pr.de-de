---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_AAAAType-Klasse
description: Die Methode "kreatinstancefrompropertydata" instanziiert einen Ressourcen Eintrag der IPv6-Adresse (AAAA).
ms.assetid: 3f2774d8-1eb6-4300-95e2-f918fc6612e0
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_AAAAType
- DNS-MicrosoftDNS_AAAAType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9232506b52795521300e827701f685e351d8ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517783"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_aaaatype-class"></a><span data-ttu-id="4c44b-106">Methode "kreateinzustancefrompropertydata" der Klasse "MicrosoftDNS \_ aaaatype"</span><span class="sxs-lookup"><span data-stu-id="4c44b-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_AAAAType class</span></span>

<span data-ttu-id="4c44b-107">Die Methode " **kreatinstancefrompropertydata** " instanziiert einen Ressourcen Eintrag der IPv6-Adresse (AAAA).</span><span class="sxs-lookup"><span data-stu-id="4c44b-107">The **CreateInstanceFromPropertyData** method instantiates an IPv6 address (AAAA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c44b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c44b-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           string                IPv6Address,
  [out, ref]     MicrosoftDNS_AAAAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="4c44b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c44b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c44b-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c44b-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c44b-111">Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="4c44b-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="4c44b-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c44b-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c44b-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="4c44b-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="4c44b-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c44b-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c44b-115">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="4c44b-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="4c44b-116">*Recordclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="4c44b-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c44b-117">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="4c44b-117">Class of the RR.</span></span> <span data-ttu-id="4c44b-118">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="4c44b-118">Default value is 1.</span></span> <span data-ttu-id="4c44b-119">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="4c44b-119">The following values are valid.</span></span>



| <span data-ttu-id="4c44b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4c44b-120">Value</span></span>                                                                                                | <span data-ttu-id="4c44b-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4c44b-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="4c44b-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="4c44b-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="4c44b-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="4c44b-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="4c44b-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="4c44b-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="4c44b-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="4c44b-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="4c44b-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="4c44b-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="4c44b-127">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="4c44b-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="4c44b-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="4c44b-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="4c44b-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="4c44b-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="4c44b-130">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="4c44b-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c44b-131">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4c44b-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="4c44b-132">*IPv6Address* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c44b-132">*IPv6Address* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c44b-133">IPv6-Adresse für den Host.</span><span class="sxs-lookup"><span data-stu-id="4c44b-133">IPv6 address for the host.</span></span>

</dd> <dt>

<span data-ttu-id="4c44b-134">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="4c44b-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="4c44b-135">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4c44b-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c44b-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4c44b-136">Return value</span></span>

<span data-ttu-id="4c44b-137">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4c44b-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c44b-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c44b-138">Requirements</span></span>



| <span data-ttu-id="4c44b-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c44b-139">Requirement</span></span> | <span data-ttu-id="4c44b-140">Wert</span><span class="sxs-lookup"><span data-stu-id="4c44b-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c44b-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4c44b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4c44b-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4c44b-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4c44b-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4c44b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4c44b-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4c44b-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4c44b-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="4c44b-145">Namespace</span></span><br/>                | <span data-ttu-id="4c44b-146">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="4c44b-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="4c44b-147">MOF</span><span class="sxs-lookup"><span data-stu-id="4c44b-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c44b-148"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4c44b-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c44b-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c44b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c44b-150">**MicrosoftDNS \_ aaaatype**</span><span class="sxs-lookup"><span data-stu-id="4c44b-150">**MicrosoftDNS\_AAAAType**</span></span>](microsoftdns-aaaatype.md)
</dt> <dt>

[<span data-ttu-id="4c44b-151">**Modify-Methode der MicrosoftDNS \_ aaaatype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4c44b-151">**Modify Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-modify.md)
</dt> <dt>

[<span data-ttu-id="4c44b-152">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="4c44b-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





