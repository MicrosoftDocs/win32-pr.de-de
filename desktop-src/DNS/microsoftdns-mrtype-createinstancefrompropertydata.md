---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_MRType-Klasse
description: Die Methode "kreatinstancefrompropertydata" instanziiert einen Ressourcen Eintrag für die Post Fach Umbenennung (Mr).
ms.assetid: 7dab86e0-bf05-4e98-b1f8-e1daecd4425c
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_MRType
- DNS-MicrosoftDNS_MRType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f41478d4ff59ff7999f6f3b052f203aeda78803
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858920"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mrtype-class"></a><span data-ttu-id="be2b3-106">Methode "kreateinstancefrompropertydata" der Klasse "MicrosoftDNS \_ mrtype"</span><span class="sxs-lookup"><span data-stu-id="be2b3-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MRType class</span></span>

<span data-ttu-id="be2b3-107">Die Methode " **kreatinstancefrompropertydata** " instanziiert einen Ressourcen Eintrag für die Post Fach Umbenennung (Mr).</span><span class="sxs-lookup"><span data-stu-id="be2b3-107">The **CreateInstanceFromPropertyData** method instantiates a Mailbox Rename (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="be2b3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="be2b3-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              MRMailbox,
  [out, ref]     MicrosoftDNS_MRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="be2b3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="be2b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be2b3-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be2b3-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be2b3-111">Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="be2b3-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="be2b3-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be2b3-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be2b3-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="be2b3-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="be2b3-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be2b3-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be2b3-115">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="be2b3-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="be2b3-116">*Recordclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="be2b3-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="be2b3-117">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="be2b3-117">Class of the RR.</span></span> <span data-ttu-id="be2b3-118">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="be2b3-118">Default value is 1.</span></span> <span data-ttu-id="be2b3-119">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="be2b3-119">The following values are valid.</span></span>



| <span data-ttu-id="be2b3-120">Wert</span><span class="sxs-lookup"><span data-stu-id="be2b3-120">Value</span></span>                                                                                                | <span data-ttu-id="be2b3-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="be2b3-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="be2b3-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="be2b3-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="be2b3-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="be2b3-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="be2b3-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="be2b3-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="be2b3-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="be2b3-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="be2b3-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="be2b3-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="be2b3-127">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="be2b3-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="be2b3-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="be2b3-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="be2b3-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="be2b3-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="be2b3-130">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="be2b3-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="be2b3-131">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="be2b3-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="be2b3-132">*Mrmailbox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be2b3-132">*MRMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be2b3-133">Der voll qualifizierte Name des Postfachs, bei dem es sich um den ordnungsgemäßen Umbenennen des im Namen des Datensatzes angegebenen Postfachs handelt</span><span class="sxs-lookup"><span data-stu-id="be2b3-133">FQDN specifying a mailbox that is the proper rename of the mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="be2b3-134">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="be2b3-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="be2b3-135">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="be2b3-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be2b3-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be2b3-136">Return value</span></span>

<span data-ttu-id="be2b3-137">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="be2b3-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="be2b3-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be2b3-138">Requirements</span></span>



| <span data-ttu-id="be2b3-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be2b3-139">Requirement</span></span> | <span data-ttu-id="be2b3-140">Wert</span><span class="sxs-lookup"><span data-stu-id="be2b3-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be2b3-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="be2b3-141">Minimum supported client</span></span><br/> | <span data-ttu-id="be2b3-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="be2b3-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="be2b3-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="be2b3-143">Minimum supported server</span></span><br/> | <span data-ttu-id="be2b3-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be2b3-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="be2b3-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="be2b3-145">Namespace</span></span><br/>                | <span data-ttu-id="be2b3-146">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="be2b3-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="be2b3-147">MOF</span><span class="sxs-lookup"><span data-stu-id="be2b3-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be2b3-148"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="be2b3-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be2b3-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be2b3-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be2b3-150">**MicrosoftDNS- \_ mrtype**</span><span class="sxs-lookup"><span data-stu-id="be2b3-150">**MicrosoftDNS\_MRType**</span></span>](microsoftdns-mrtype.md)
</dt> <dt>

[<span data-ttu-id="be2b3-151">**Modify-Methode der MicrosoftDNS- \_ mrtype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="be2b3-151">**Modify Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-modify.md)
</dt> <dt>

[<span data-ttu-id="be2b3-152">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="be2b3-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





