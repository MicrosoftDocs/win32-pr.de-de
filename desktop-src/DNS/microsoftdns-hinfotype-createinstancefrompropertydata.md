---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_HINFOType-Klasse
description: Die Methode "kreateinstancefrompropertydata" instanziiert einen Ressourcen Eintrag für die Host Informationen (HINFO).
ms.assetid: dfc11ae8-5013-4b48-a1e9-78566dc32297
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_HINFOType
- DNS-MicrosoftDNS_HINFOType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2c8386a9c66ec94436fe4ae4c886ec62ff5b96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743160"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_hinfotype-class"></a><span data-ttu-id="8b7d7-106">Methode "kreateinstancefrompropertydata" der "hinfotype"-Klasse von MicrosoftDNS \_</span><span class="sxs-lookup"><span data-stu-id="8b7d7-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_HINFOType class</span></span>

<span data-ttu-id="8b7d7-107">Die Methode " **kreateinstancefrompropertydata** " instanziiert einen Ressourcen Eintrag für die Host Informationen (HINFO).</span><span class="sxs-lookup"><span data-stu-id="8b7d7-107">The **CreateInstanceFromPropertyData** method instantiates a Host Information (HINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b7d7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b7d7-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in, optional] string                 CPU,
  [in, optional] string                 OS,
  [out, ref]     MicrosoftDNS_HINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="8b7d7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b7d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b7d7-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b7d7-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b7d7-111">Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="8b7d7-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="8b7d7-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b7d7-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b7d7-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="8b7d7-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="8b7d7-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b7d7-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b7d7-115">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="8b7d7-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="8b7d7-116">*Recordclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8b7d7-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8b7d7-117">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="8b7d7-117">Class of the RR.</span></span> <span data-ttu-id="8b7d7-118">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="8b7d7-118">Default value is 1.</span></span> <span data-ttu-id="8b7d7-119">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="8b7d7-119">The following values are valid.</span></span>



| <span data-ttu-id="8b7d7-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8b7d7-120">Value</span></span>                                                                                                | <span data-ttu-id="8b7d7-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8b7d7-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="8b7d7-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="8b7d7-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="8b7d7-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="8b7d7-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="8b7d7-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="8b7d7-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="8b7d7-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="8b7d7-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="8b7d7-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="8b7d7-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="8b7d7-127">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="8b7d7-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="8b7d7-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="8b7d7-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="8b7d7-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="8b7d7-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="8b7d7-130">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8b7d7-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8b7d7-131">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="8b7d7-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="8b7d7-132">*CPU* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8b7d7-132">*CPU* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8b7d7-133">Der CPU-Typ des Daten Satz Besitzers.</span><span class="sxs-lookup"><span data-stu-id="8b7d7-133">CPU type of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="8b7d7-134">*Betriebssystem* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8b7d7-134">*OS* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8b7d7-135">Das Betriebssystem des Daten Satz Besitzers.</span><span class="sxs-lookup"><span data-stu-id="8b7d7-135">Operating system of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="8b7d7-136">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="8b7d7-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8b7d7-137">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8b7d7-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b7d7-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b7d7-138">Return value</span></span>

<span data-ttu-id="8b7d7-139">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8b7d7-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b7d7-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b7d7-140">Requirements</span></span>



| <span data-ttu-id="8b7d7-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b7d7-141">Requirement</span></span> | <span data-ttu-id="8b7d7-142">Wert</span><span class="sxs-lookup"><span data-stu-id="8b7d7-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b7d7-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b7d7-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8b7d7-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8b7d7-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8b7d7-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b7d7-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8b7d7-146">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b7d7-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8b7d7-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="8b7d7-147">Namespace</span></span><br/>                | <span data-ttu-id="8b7d7-148">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="8b7d7-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="8b7d7-149">MOF</span><span class="sxs-lookup"><span data-stu-id="8b7d7-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b7d7-150"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8b7d7-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b7d7-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b7d7-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b7d7-152">**MicrosoftDNS \_ hinfotype**</span><span class="sxs-lookup"><span data-stu-id="8b7d7-152">**MicrosoftDNS\_HINFOType**</span></span>](microsoftdns-hinfotype.md)
</dt> <dt>

[<span data-ttu-id="8b7d7-153">**Modify-Methode der MicrosoftDNS- \_ hinfotype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8b7d7-153">**Modify Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="8b7d7-154">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="8b7d7-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





