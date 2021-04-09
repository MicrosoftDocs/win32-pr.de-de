---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_MGType-Klasse
description: Die Methode "kreatinstancefrompropertydata" instanziiert einen Ressourcen Eintrag für eine e-Mail-Gruppe (mg).
ms.assetid: 98e2ecb3-bf2f-42db-8a8b-de10a29f5a5a
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_MGType
- DNS-MicrosoftDNS_MGType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 313f6d14a10b1de9bc1d3b3b8042020ea5b0a522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104733"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mgtype-class"></a><span data-ttu-id="97407-106">Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ mgtype-Klasse</span><span class="sxs-lookup"><span data-stu-id="97407-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MGType class</span></span>

<span data-ttu-id="97407-107">Die Methode " **kreatinstancefrompropertydata** " instanziiert einen Ressourcen Eintrag für eine e-Mail-Gruppe (mg).</span><span class="sxs-lookup"><span data-stu-id="97407-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Group (MG) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="97407-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="97407-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              MGMailbox,
  [out, ref]     MicrosoftDNS_MGType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="97407-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="97407-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97407-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97407-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97407-111">Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="97407-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="97407-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97407-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97407-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="97407-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="97407-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97407-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97407-115">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="97407-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="97407-116">*Recordclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="97407-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97407-117">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="97407-117">Class of the RR.</span></span> <span data-ttu-id="97407-118">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="97407-118">Default value is 1.</span></span> <span data-ttu-id="97407-119">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="97407-119">The following values are valid.</span></span>



| <span data-ttu-id="97407-120">Wert</span><span class="sxs-lookup"><span data-stu-id="97407-120">Value</span></span>                                                                                                | <span data-ttu-id="97407-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="97407-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="97407-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="97407-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="97407-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="97407-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="97407-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="97407-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="97407-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="97407-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="97407-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="97407-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="97407-127">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="97407-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="97407-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="97407-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="97407-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="97407-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="97407-130">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="97407-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="97407-131">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="97407-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="97407-132">*Mgmailbox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97407-132">*MGMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97407-133">FQDN, der ein Postfach angibt, das Mitglied der durch den Besitzer Namen des Datensatzes angegebenen e-Mail-Gruppe ist.</span><span class="sxs-lookup"><span data-stu-id="97407-133">FQDN specifying a mailbox that is a member of the mail group specified by the record's owner name.</span></span>

</dd> <dt>

<span data-ttu-id="97407-134">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="97407-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="97407-135">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="97407-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97407-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97407-136">Return value</span></span>

<span data-ttu-id="97407-137">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="97407-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="97407-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97407-138">Requirements</span></span>



| <span data-ttu-id="97407-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97407-139">Requirement</span></span> | <span data-ttu-id="97407-140">Wert</span><span class="sxs-lookup"><span data-stu-id="97407-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97407-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97407-141">Minimum supported client</span></span><br/> | <span data-ttu-id="97407-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="97407-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="97407-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97407-143">Minimum supported server</span></span><br/> | <span data-ttu-id="97407-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97407-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="97407-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="97407-145">Namespace</span></span><br/>                | <span data-ttu-id="97407-146">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="97407-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="97407-147">MOF</span><span class="sxs-lookup"><span data-stu-id="97407-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97407-148"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="97407-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97407-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97407-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97407-150">**MicrosoftDNS- \_ mgtype**</span><span class="sxs-lookup"><span data-stu-id="97407-150">**MicrosoftDNS\_MGType**</span></span>](microsoftdns-mgtype.md)
</dt> <dt>

[<span data-ttu-id="97407-151">**Modify-Methode der MicrosoftDNS- \_ mgtype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="97407-151">**Modify Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-modify.md)
</dt> <dt>

[<span data-ttu-id="97407-152">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="97407-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





