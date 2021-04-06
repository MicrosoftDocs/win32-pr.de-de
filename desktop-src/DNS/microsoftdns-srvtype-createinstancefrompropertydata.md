---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_SRVType-Klasse
description: Die Methode "kreatinstancefrompropertydata" instanziiert einen Dienst Ressourcen Eintrag (SRV).
ms.assetid: ef55faa8-1109-4c96-98ac-2b01b940fa5c
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_SRVType
- DNS-MicrosoftDNS_SRVType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 607ed606bf12e9e2a6f90a6e7f309aa708b7f230
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743384"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_srvtype-class"></a><span data-ttu-id="dab0f-106">Die Methode "kreateinstancefrompropertydata" der Klasse "srvtype" von MicrosoftDNS \_</span><span class="sxs-lookup"><span data-stu-id="dab0f-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_SRVType class</span></span>

<span data-ttu-id="dab0f-107">Die Methode " **kreatinstancefrompropertydata** " instanziiert einen Dienst Ressourcen Eintrag (SRV).</span><span class="sxs-lookup"><span data-stu-id="dab0f-107">The **CreateInstanceFromPropertyData** method instantiates a Service (SRV) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="dab0f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="dab0f-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               Priority,
  [in]           uint16               Weight,
  [in]           uint16               Port,
  [in]           string               SRVDomainName,
  [out, ref]     MicrosoftDNS_SRVType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="dab0f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="dab0f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dab0f-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dab0f-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dab0f-111">Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="dab0f-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="dab0f-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dab0f-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dab0f-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="dab0f-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="dab0f-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dab0f-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dab0f-115">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="dab0f-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="dab0f-116">*Recordclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="dab0f-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dab0f-117">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="dab0f-117">Class of the RR.</span></span> <span data-ttu-id="dab0f-118">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="dab0f-118">Default value is 1.</span></span> <span data-ttu-id="dab0f-119">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="dab0f-119">The following values are valid.</span></span>



| <span data-ttu-id="dab0f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="dab0f-120">Value</span></span>                                                                                                | <span data-ttu-id="dab0f-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="dab0f-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="dab0f-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="dab0f-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="dab0f-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="dab0f-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="dab0f-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="dab0f-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="dab0f-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="dab0f-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="dab0f-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="dab0f-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="dab0f-127">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="dab0f-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="dab0f-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="dab0f-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="dab0f-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="dab0f-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="dab0f-130">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="dab0f-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dab0f-131">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="dab0f-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="dab0f-132">*Priorität* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dab0f-132">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dab0f-133">Priorität des im Besitzer Namen angegebenen Zielhosts.</span><span class="sxs-lookup"><span data-stu-id="dab0f-133">Priority of the target host specified in the owner name.</span></span> <span data-ttu-id="dab0f-134">Niedrigere Zahlen implizieren höhere Prioritäten.</span><span class="sxs-lookup"><span data-stu-id="dab0f-134">Lower numbers imply higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="dab0f-135">*Gewichtung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dab0f-135">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dab0f-136">Gewichtung des Zielhosts.</span><span class="sxs-lookup"><span data-stu-id="dab0f-136">Weight of the target host.</span></span> <span data-ttu-id="dab0f-137">Dies ist hilfreich bei der Auswahl zwischen Hosts mit der gleichen Priorität.</span><span class="sxs-lookup"><span data-stu-id="dab0f-137">This is useful when selecting among hosts that have the same priority.</span></span> <span data-ttu-id="dab0f-138">Die Wahrscheinlichkeit, diesen Host zu verwenden, sollte proportional zu seiner Gewichtung sein.</span><span class="sxs-lookup"><span data-stu-id="dab0f-138">The chances of using this host should be proportional to its weight.</span></span>

</dd> <dt>

<span data-ttu-id="dab0f-139">*Port* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dab0f-139">*Port* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dab0f-140">Port, der auf dem Zielhost eines Protokoll Diensts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dab0f-140">Port used on the target host of a protocol service.</span></span>

</dd> <dt>

<span data-ttu-id="dab0f-141">*Srvdomainname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dab0f-141">*SRVDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dab0f-142">Der voll qualifizierte Namen des Zielhosts.</span><span class="sxs-lookup"><span data-stu-id="dab0f-142">FQDN of the target host.</span></span> <span data-ttu-id="dab0f-143">Ein Ziel von \\ . \\ bedeutet, dass der Dienst in dieser Domäne nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="dab0f-143">A target of \\.\\ means that the service is decidedly not available at this domain.</span></span>

</dd> <dt>

<span data-ttu-id="dab0f-144">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="dab0f-144">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="dab0f-145">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="dab0f-145">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dab0f-146">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dab0f-146">Return value</span></span>

<span data-ttu-id="dab0f-147">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="dab0f-147">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="dab0f-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dab0f-148">Requirements</span></span>



| <span data-ttu-id="dab0f-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dab0f-149">Requirement</span></span> | <span data-ttu-id="dab0f-150">Wert</span><span class="sxs-lookup"><span data-stu-id="dab0f-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dab0f-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dab0f-151">Minimum supported client</span></span><br/> | <span data-ttu-id="dab0f-152">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="dab0f-152">None supported</span></span><br/>                                                              |
| <span data-ttu-id="dab0f-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dab0f-153">Minimum supported server</span></span><br/> | <span data-ttu-id="dab0f-154">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dab0f-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dab0f-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="dab0f-155">Namespace</span></span><br/>                | <span data-ttu-id="dab0f-156">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="dab0f-156">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="dab0f-157">MOF</span><span class="sxs-lookup"><span data-stu-id="dab0f-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dab0f-158"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dab0f-158"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dab0f-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dab0f-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dab0f-160">**MicrosoftDNS- \_ srvtype**</span><span class="sxs-lookup"><span data-stu-id="dab0f-160">**MicrosoftDNS\_SRVType**</span></span>](microsoftdns-srvtype.md)
</dt> <dt>

[<span data-ttu-id="dab0f-161">**Modify-Methode der MicrosoftDNS \_ srvtype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="dab0f-161">**Modify Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-modify.md)
</dt> <dt>

[<span data-ttu-id="dab0f-162">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="dab0f-162">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





