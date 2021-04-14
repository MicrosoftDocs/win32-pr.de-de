---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_ISDNType-Klasse
description: Die Methode "kreatinstancefrompropertydata" instanziiert einen ISDN-Ressourcen Eintrag.
ms.assetid: cd3b98e3-a804-473e-8831-5f045d43a54f
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_ISDNType
- DNS-MicrosoftDNS_ISDNType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39f6adaaf374cac56d7d29d04d83c8765b0080ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518257"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_isdntype-class"></a><span data-ttu-id="c1d56-106">Die Methode "kreateinstancefrompropertydata" der Klasse "MicrosoftDNS \_ isdntype"</span><span class="sxs-lookup"><span data-stu-id="c1d56-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_ISDNType class</span></span>

<span data-ttu-id="c1d56-107">Die Methode " **kreatinstancefrompropertydata** " instanziiert einen ISDN-Ressourcen Eintrag.</span><span class="sxs-lookup"><span data-stu-id="c1d56-107">The **CreateInstanceFromPropertyData** method instantiates an ISDN Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1d56-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1d56-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           string                ISDNNumber,
  [in]           string                SubAddress,
  [out, ref]     MicrosoftDNS_ISDNType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="c1d56-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1d56-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1d56-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1d56-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d56-111">Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="c1d56-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="c1d56-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1d56-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d56-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="c1d56-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="c1d56-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1d56-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d56-115">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="c1d56-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="c1d56-116">*Recordclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c1d56-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d56-117">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="c1d56-117">Class of the RR.</span></span> <span data-ttu-id="c1d56-118">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="c1d56-118">Default value is 1.</span></span> <span data-ttu-id="c1d56-119">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="c1d56-119">The following values are valid.</span></span>



| <span data-ttu-id="c1d56-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c1d56-120">Value</span></span>                                                                                                | <span data-ttu-id="c1d56-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c1d56-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="c1d56-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d56-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="c1d56-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="c1d56-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="c1d56-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d56-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="c1d56-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="c1d56-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="c1d56-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d56-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="c1d56-127">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="c1d56-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="c1d56-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="c1d56-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="c1d56-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="c1d56-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="c1d56-130">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c1d56-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d56-131">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c1d56-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="c1d56-132">*Isdnnumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1d56-132">*ISDNNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d56-133">ISDN-Nummer und DDI für den Besitzer des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="c1d56-133">ISDN number and DDI of the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="c1d56-134">*Unter Adresse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1d56-134">*SubAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d56-135">Die untergeordnete Adresse des Besitzers, sofern definiert.</span><span class="sxs-lookup"><span data-stu-id="c1d56-135">Subaddress of the owner, if defined.</span></span>

</dd> <dt>

<span data-ttu-id="c1d56-136">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="c1d56-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d56-137">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c1d56-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1d56-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1d56-138">Return value</span></span>

<span data-ttu-id="c1d56-139">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c1d56-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1d56-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1d56-140">Requirements</span></span>



| <span data-ttu-id="c1d56-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1d56-141">Requirement</span></span> | <span data-ttu-id="c1d56-142">Wert</span><span class="sxs-lookup"><span data-stu-id="c1d56-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1d56-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1d56-143">Minimum supported client</span></span><br/> | <span data-ttu-id="c1d56-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c1d56-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c1d56-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1d56-145">Minimum supported server</span></span><br/> | <span data-ttu-id="c1d56-146">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1d56-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c1d56-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1d56-147">Namespace</span></span><br/>                | <span data-ttu-id="c1d56-148">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="c1d56-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c1d56-149">MOF</span><span class="sxs-lookup"><span data-stu-id="c1d56-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1d56-150"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c1d56-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1d56-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1d56-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1d56-152">**MicrosoftDNS \_ isdntype**</span><span class="sxs-lookup"><span data-stu-id="c1d56-152">**MicrosoftDNS\_ISDNType**</span></span>](microsoftdns-isdntype.md)
</dt> <dt>

[<span data-ttu-id="c1d56-153">**Modify-Methode der MicrosoftDNS- \_ isdntype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c1d56-153">**Modify Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-modify.md)
</dt> <dt>

[<span data-ttu-id="c1d56-154">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="c1d56-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





