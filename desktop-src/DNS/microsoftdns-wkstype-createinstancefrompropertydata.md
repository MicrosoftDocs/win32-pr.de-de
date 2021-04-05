---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_WKSType-Klasse
description: Die Methode "kreatinstancefrompropertydata" instanziiert einen Well-Known Services (WLS)-Ressourcen Eintrag.
ms.assetid: 6d910716-74f9-48a0-b43c-3243f5518caf
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_WKSType
- DNS-MicrosoftDNS_WKSType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e27b62bd2008c58d283d0e7564fa7821c452cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859039"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_wkstype-class"></a><span data-ttu-id="f6b4b-106">Methode "kreateinzustancefrompropertydata" der MicrosoftDNS- \_ Klasse "wkstype"</span><span class="sxs-lookup"><span data-stu-id="f6b4b-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_WKSType class</span></span>

<span data-ttu-id="f6b4b-107">Die Methode " **kreatinstancefrompropertydata** " instanziiert einen Well-Known Services (WLS)-Ressourcen Eintrag.</span><span class="sxs-lookup"><span data-stu-id="f6b4b-107">The **CreateInstanceFromPropertyData** method instantiates a Well-Known Services (WKS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6b4b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6b4b-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               InternetAddress,
  [in]           string               IPProtocol,
  [in]           string               Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="f6b4b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6b4b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6b4b-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6b4b-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6b4b-111">Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="f6b4b-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="f6b4b-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6b4b-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6b4b-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="f6b4b-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="f6b4b-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6b4b-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6b4b-115">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="f6b4b-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="f6b4b-116">*Recordclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="f6b4b-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f6b4b-117">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="f6b4b-117">Class of the RR.</span></span> <span data-ttu-id="f6b4b-118">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="f6b4b-118">Default value is 1.</span></span> <span data-ttu-id="f6b4b-119">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="f6b4b-119">The following values are valid.</span></span>



| <span data-ttu-id="f6b4b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f6b4b-120">Value</span></span>                                                                                                | <span data-ttu-id="f6b4b-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f6b4b-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="f6b4b-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="f6b4b-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="f6b4b-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="f6b4b-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="f6b4b-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="f6b4b-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="f6b4b-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="f6b4b-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="f6b4b-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="f6b4b-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="f6b4b-127">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="f6b4b-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="f6b4b-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="f6b4b-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="f6b4b-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="f6b4b-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="f6b4b-130">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="f6b4b-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f6b4b-131">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f6b4b-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="f6b4b-132">*Internetadresse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6b4b-132">*InternetAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6b4b-133">Internet-IP-Adresse für den Besitzer des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="f6b4b-133">Internet IP address for the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="f6b4b-134">*Ipprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6b4b-134">*IPProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6b4b-135">Zeichenfolge, die das IP-Protokoll für diesen Datensatz darstellt.</span><span class="sxs-lookup"><span data-stu-id="f6b4b-135">String representing the IP protocol for this record.</span></span> <span data-ttu-id="f6b4b-136">Gültige Werte sind UDP oder TCP.</span><span class="sxs-lookup"><span data-stu-id="f6b4b-136">Valid values are UDP or TCP.</span></span>

</dd> <dt>

<span data-ttu-id="f6b4b-137">*Dienste* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6b4b-137">*Services* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6b4b-138">Eine Zeichenfolge, die alle Dienste enthält, die vom Wi-Datensatz (well known Service) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6b4b-138">String containing all services used by the Well Known Service (WKS) record.</span></span>

</dd> <dt>

<span data-ttu-id="f6b4b-139">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="f6b4b-139">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f6b4b-140">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f6b4b-140">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6b4b-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6b4b-141">Return value</span></span>

<span data-ttu-id="f6b4b-142">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f6b4b-142">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6b4b-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6b4b-143">Requirements</span></span>



| <span data-ttu-id="f6b4b-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6b4b-144">Requirement</span></span> | <span data-ttu-id="f6b4b-145">Wert</span><span class="sxs-lookup"><span data-stu-id="f6b4b-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6b4b-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f6b4b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="f6b4b-147">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f6b4b-147">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f6b4b-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f6b4b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="f6b4b-149">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f6b4b-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f6b4b-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="f6b4b-150">Namespace</span></span><br/>                | <span data-ttu-id="f6b4b-151">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="f6b4b-151">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f6b4b-152">MOF</span><span class="sxs-lookup"><span data-stu-id="f6b4b-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6b4b-153"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f6b4b-153"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6b4b-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6b4b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6b4b-155">**MicrosoftDNS \_ wkstype**</span><span class="sxs-lookup"><span data-stu-id="f6b4b-155">**MicrosoftDNS\_WKSType**</span></span>](microsoftdns-wkstype.md)
</dt> <dt>

[<span data-ttu-id="f6b4b-156">**Modify-Methode der MicrosoftDNS- \_ Klasse "wkstype"**</span><span class="sxs-lookup"><span data-stu-id="f6b4b-156">**Modify Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-modify.md)
</dt> <dt>

[<span data-ttu-id="f6b4b-157">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="f6b4b-157">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





