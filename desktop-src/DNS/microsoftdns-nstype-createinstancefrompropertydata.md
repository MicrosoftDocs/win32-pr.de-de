---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_NSType-Klasse
description: Die Methode "kreateinstancefrompropertydata" instanziiert einen Namen Server-Ressourcen Eintrag (NS).
ms.assetid: f2399a9d-840d-4392-86c4-610894e60f8e
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_NSType
- DNS-MicrosoftDNS_NSType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_NSType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37b21323da53c592375a00be9303c321d270f9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517777"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_nstype-class"></a><span data-ttu-id="033d6-106">Methode "kreateinzustancefrompropertydata" der MicrosoftDNS- \_ nstype-Klasse</span><span class="sxs-lookup"><span data-stu-id="033d6-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_NSType class</span></span>

<span data-ttu-id="033d6-107">Die Methode " **kreateinstancefrompropertydata** " instanziiert einen Namen Server-Ressourcen Eintrag (NS).</span><span class="sxs-lookup"><span data-stu-id="033d6-107">The **CreateInstanceFromPropertyData** method instantiates a Name Server (NS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="033d6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="033d6-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              NSHost,
  [out, ref]     MicrosoftDNS_NSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="033d6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="033d6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="033d6-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="033d6-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="033d6-111">Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="033d6-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="033d6-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="033d6-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="033d6-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="033d6-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="033d6-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="033d6-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="033d6-115">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="033d6-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="033d6-116">*Recordclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="033d6-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="033d6-117">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="033d6-117">Class of the RR.</span></span> <span data-ttu-id="033d6-118">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="033d6-118">Default value is 1.</span></span> <span data-ttu-id="033d6-119">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="033d6-119">The following values are valid.</span></span>



| <span data-ttu-id="033d6-120">Wert</span><span class="sxs-lookup"><span data-stu-id="033d6-120">Value</span></span>                                                                                                | <span data-ttu-id="033d6-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="033d6-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="033d6-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="033d6-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="033d6-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="033d6-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="033d6-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="033d6-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="033d6-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="033d6-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="033d6-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="033d6-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="033d6-127">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="033d6-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="033d6-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="033d6-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="033d6-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="033d6-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="033d6-130">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="033d6-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="033d6-131">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="033d6-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="033d6-132">*NSHost* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="033d6-132">*NSHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="033d6-133">Autorisierender Host für die Domäne.</span><span class="sxs-lookup"><span data-stu-id="033d6-133">Authoritative host for the domain.</span></span>

</dd> <dt>

<span data-ttu-id="033d6-134">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="033d6-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="033d6-135">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="033d6-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="033d6-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="033d6-136">Return value</span></span>

<span data-ttu-id="033d6-137">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="033d6-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="033d6-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="033d6-138">Requirements</span></span>



| <span data-ttu-id="033d6-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="033d6-139">Requirement</span></span> | <span data-ttu-id="033d6-140">Wert</span><span class="sxs-lookup"><span data-stu-id="033d6-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="033d6-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="033d6-141">Minimum supported client</span></span><br/> | <span data-ttu-id="033d6-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="033d6-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="033d6-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="033d6-143">Minimum supported server</span></span><br/> | <span data-ttu-id="033d6-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="033d6-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="033d6-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="033d6-145">Namespace</span></span><br/>                | <span data-ttu-id="033d6-146">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="033d6-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="033d6-147">MOF</span><span class="sxs-lookup"><span data-stu-id="033d6-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="033d6-148"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="033d6-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="033d6-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="033d6-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="033d6-150">**MicrosoftDNS \_ nstype**</span><span class="sxs-lookup"><span data-stu-id="033d6-150">**MicrosoftDNS\_NSType**</span></span>](microsoftdns-nstype.md)
</dt> <dt>

[<span data-ttu-id="033d6-151">**Modify-Methode der MicrosoftDNS- \_ nstype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="033d6-151">**Modify Method of the MicrosoftDNS\_NSType Class**</span></span>](microsoftdns-nstype-modify.md)
</dt> <dt>

[<span data-ttu-id="033d6-152">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="033d6-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





