---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_RPType-Klasse
description: Die Methode "kreatinstancefrompropertydata" instanziiert einen Ressourcen Eintrag für eine verantwortliche Person (RP).
ms.assetid: 6d9366c3-fc82-4c1f-8fa3-c107f6a1ff74
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_RPType
- DNS-MicrosoftDNS_RPType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c150a8a91a7a94fbea8492faea08b61d437a4c9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213719"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_rptype-class"></a><span data-ttu-id="eb256-106">Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ rptype-Klasse</span><span class="sxs-lookup"><span data-stu-id="eb256-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_RPType class</span></span>

<span data-ttu-id="eb256-107">Die Methode " **kreatinstancefrompropertydata** " instanziiert einen Ressourcen Eintrag für eine verantwortliche Person (RP).</span><span class="sxs-lookup"><span data-stu-id="eb256-107">The **CreateInstanceFromPropertyData** method instantiates a Responsible Person (RP) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb256-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb256-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              RPMailbox,
  [in]           string              TXTDomainName,
  [out, ref]     MicrosoftDNS_RPType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="eb256-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb256-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb256-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb256-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb256-111">Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="eb256-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="eb256-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb256-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb256-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="eb256-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="eb256-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb256-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb256-115">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="eb256-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="eb256-116">*Recordclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="eb256-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb256-117">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="eb256-117">Class of the RR.</span></span> <span data-ttu-id="eb256-118">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="eb256-118">Default value is 1.</span></span> <span data-ttu-id="eb256-119">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="eb256-119">The following values are valid.</span></span>



| <span data-ttu-id="eb256-120">Wert</span><span class="sxs-lookup"><span data-stu-id="eb256-120">Value</span></span>                                                                                                | <span data-ttu-id="eb256-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="eb256-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="eb256-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="eb256-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="eb256-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="eb256-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="eb256-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="eb256-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="eb256-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="eb256-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="eb256-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="eb256-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="eb256-127">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="eb256-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="eb256-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="eb256-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="eb256-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="eb256-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="eb256-130">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="eb256-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb256-131">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="eb256-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="eb256-132">*Rpmailbox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb256-132">*RPMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb256-133">Vollständiger vollständiger vollständiger Name des Postfachs.</span><span class="sxs-lookup"><span data-stu-id="eb256-133">FQDN specifying the mailbox for the responsible person.</span></span>

</dd> <dt>

<span data-ttu-id="eb256-134">*TxtDomainName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb256-134">*TXTDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb256-135">Der voll qualifizierte Daten Satz, für den txt-Ressourcen Einträge vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="eb256-135">FQDN for which TXT Resource Records exist.</span></span>

</dd> <dt>

<span data-ttu-id="eb256-136">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="eb256-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="eb256-137">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="eb256-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb256-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb256-138">Return value</span></span>

<span data-ttu-id="eb256-139">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="eb256-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb256-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb256-140">Requirements</span></span>



| <span data-ttu-id="eb256-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb256-141">Requirement</span></span> | <span data-ttu-id="eb256-142">Wert</span><span class="sxs-lookup"><span data-stu-id="eb256-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb256-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eb256-143">Minimum supported client</span></span><br/> | <span data-ttu-id="eb256-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="eb256-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="eb256-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eb256-145">Minimum supported server</span></span><br/> | <span data-ttu-id="eb256-146">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb256-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="eb256-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="eb256-147">Namespace</span></span><br/>                | <span data-ttu-id="eb256-148">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="eb256-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="eb256-149">MOF</span><span class="sxs-lookup"><span data-stu-id="eb256-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb256-150"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="eb256-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb256-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb256-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb256-152">**MicrosoftDNS- \_ rptype**</span><span class="sxs-lookup"><span data-stu-id="eb256-152">**MicrosoftDNS\_RPType**</span></span>](microsoftdns-rptype.md)
</dt> <dt>

[<span data-ttu-id="eb256-153">**Modify-Methode der MicrosoftDNS- \_ rptype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="eb256-153">**Modify Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-modify.md)
</dt> <dt>

[<span data-ttu-id="eb256-154">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="eb256-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





