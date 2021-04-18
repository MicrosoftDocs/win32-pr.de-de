---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_TXTType-Klasse
description: Die Methode "kreatinstancefrompropertydata" instanziiert einen Text Ressourcen Eintrag (txt).
ms.assetid: f518bb07-e64f-4240-a7b8-9363374b83d6
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_TXTType
- DNS-MicrosoftDNS_TXTType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f23f9790189ca182cd65d9fe34890c31a90921d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345323"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_txttype-class"></a><span data-ttu-id="4cb6c-106">Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS- \_ Klasse "txttype"</span><span class="sxs-lookup"><span data-stu-id="4cb6c-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_TXTType class</span></span>

<span data-ttu-id="4cb6c-107">Die Methode " **kreatinstancefrompropertydata** " instanziiert einen Text Ressourcen Eintrag (txt).</span><span class="sxs-lookup"><span data-stu-id="4cb6c-107">The **CreateInstanceFromPropertyData** method instantiates a Text (TXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cb6c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cb6c-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               DescriptiveText,
  [out, ref]     MicrosoftDNS_TXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="4cb6c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cb6c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cb6c-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cb6c-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cb6c-111">Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="4cb6c-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="4cb6c-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cb6c-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cb6c-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="4cb6c-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="4cb6c-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cb6c-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cb6c-115">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="4cb6c-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="4cb6c-116">*Recordclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="4cb6c-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4cb6c-117">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="4cb6c-117">Class of the RR.</span></span> <span data-ttu-id="4cb6c-118">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="4cb6c-118">Default value is 1.</span></span> <span data-ttu-id="4cb6c-119">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="4cb6c-119">The following values are valid.</span></span>



| <span data-ttu-id="4cb6c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4cb6c-120">Value</span></span>                                                                                                | <span data-ttu-id="4cb6c-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4cb6c-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="4cb6c-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="4cb6c-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="4cb6c-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="4cb6c-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="4cb6c-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="4cb6c-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="4cb6c-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="4cb6c-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="4cb6c-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="4cb6c-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="4cb6c-127">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="4cb6c-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="4cb6c-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="4cb6c-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="4cb6c-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="4cb6c-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="4cb6c-130">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="4cb6c-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4cb6c-131">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4cb6c-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="4cb6c-132">*Deskriptivetext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4cb6c-132">*DescriptiveText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cb6c-133">Beschreibender Text, die Semantik, von der abhängig von der Besitzer Domäne ist.</span><span class="sxs-lookup"><span data-stu-id="4cb6c-133">Descriptive text, the semantics of which depend on the owner domain.</span></span>

</dd> <dt>

<span data-ttu-id="4cb6c-134">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="4cb6c-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="4cb6c-135">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4cb6c-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cb6c-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4cb6c-136">Return value</span></span>

<span data-ttu-id="4cb6c-137">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4cb6c-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cb6c-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4cb6c-138">Requirements</span></span>



| <span data-ttu-id="4cb6c-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4cb6c-139">Requirement</span></span> | <span data-ttu-id="4cb6c-140">Wert</span><span class="sxs-lookup"><span data-stu-id="4cb6c-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cb6c-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4cb6c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4cb6c-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4cb6c-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4cb6c-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4cb6c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4cb6c-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4cb6c-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4cb6c-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="4cb6c-145">Namespace</span></span><br/>                | <span data-ttu-id="4cb6c-146">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="4cb6c-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="4cb6c-147">MOF</span><span class="sxs-lookup"><span data-stu-id="4cb6c-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4cb6c-148"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4cb6c-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cb6c-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cb6c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cb6c-150">**MicrosoftDNS- \_ txttype**</span><span class="sxs-lookup"><span data-stu-id="4cb6c-150">**MicrosoftDNS\_TXTType**</span></span>](microsoftdns-txttype.md)
</dt> <dt>

[<span data-ttu-id="4cb6c-151">**Modify-Methode der MicrosoftDNS \_ txttype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4cb6c-151">**Modify Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-modify.md)
</dt> <dt>

[<span data-ttu-id="4cb6c-152">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="4cb6c-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





