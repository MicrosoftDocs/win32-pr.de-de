---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_AType-Klasse
description: Die Methode "kreatinstancefrompropertydata" instanziiert einen Adresseintrag (A) für die Ressource.
ms.assetid: 81d67eba-f2c6-49c0-af29-be3f3724a973
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_AType
- DNS-MicrosoftDNS_AType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1d8d3e5c9d0ad4302da2243a3ef9611e295c86e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103713"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_atype-class"></a><span data-ttu-id="29be1-106">Methode "kreateinzustancefrompropertydata" der Klasse "MicrosoftDNS \_ aType"</span><span class="sxs-lookup"><span data-stu-id="29be1-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_AType class</span></span>

<span data-ttu-id="29be1-107">Die Methode " **kreatinstancefrompropertydata** " instanziiert einen Adresseintrag (A) für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="29be1-107">The **CreateInstanceFromPropertyData** method instantiates an Address (A) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="29be1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="29be1-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string             DnsServerName,
  [in]           string             ContainerName,
  [in]           string             OwnerName,
  [in, optional] uint32             RecordClass = 1,
  [in, optional] uint32             TTL,
  [in]           string             IPAddress,
  [out, ref]     MicrosoftDNS_AType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="29be1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="29be1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29be1-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29be1-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29be1-111">Der voll qualifizierte Domänen Name (FQDN) oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="29be1-111">Fully Qualified Domain Name (FQDN) or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="29be1-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29be1-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29be1-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="29be1-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="29be1-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29be1-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29be1-115">Der Besitzer-voll qualifizierte Name für den RR.</span><span class="sxs-lookup"><span data-stu-id="29be1-115">Owner FQDN for the RR.</span></span>

> [!Note]  
> <span data-ttu-id="29be1-116">Verwenden Sie nicht den NetBIOS-Namen des Besitzers.</span><span class="sxs-lookup"><span data-stu-id="29be1-116">Do not use the owner NetBIOS name.</span></span>

 

</dd> <dt>

<span data-ttu-id="29be1-117">*Recordclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="29be1-117">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="29be1-118">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="29be1-118">Class of the RR.</span></span> <span data-ttu-id="29be1-119">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="29be1-119">Default value is 1.</span></span> <span data-ttu-id="29be1-120">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="29be1-120">The following values are valid.</span></span>



| <span data-ttu-id="29be1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="29be1-121">Value</span></span>                                                                                                | <span data-ttu-id="29be1-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="29be1-122">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="29be1-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="29be1-123"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="29be1-124">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="29be1-124">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="29be1-125"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="29be1-125"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="29be1-126">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="29be1-126">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="29be1-127"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="29be1-127"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="29be1-128">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="29be1-128">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="29be1-129"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="29be1-129"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="29be1-130">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="29be1-130">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="29be1-131">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="29be1-131">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="29be1-132">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="29be1-132">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="29be1-133">*IPAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29be1-133">*IPAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29be1-134">Zeichenfolge, die die IP-Adresse des Hosts darstellt.</span><span class="sxs-lookup"><span data-stu-id="29be1-134">String representing the IP address of the host.</span></span>

</dd> <dt>

<span data-ttu-id="29be1-135">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="29be1-135">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="29be1-136">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="29be1-136">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29be1-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29be1-137">Return value</span></span>

<span data-ttu-id="29be1-138">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="29be1-138">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="29be1-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29be1-139">Requirements</span></span>



| <span data-ttu-id="29be1-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29be1-140">Requirement</span></span> | <span data-ttu-id="29be1-141">Wert</span><span class="sxs-lookup"><span data-stu-id="29be1-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="29be1-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29be1-142">Minimum supported client</span></span><br/> | <span data-ttu-id="29be1-143">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="29be1-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="29be1-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29be1-144">Minimum supported server</span></span><br/> | <span data-ttu-id="29be1-145">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29be1-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="29be1-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="29be1-146">Namespace</span></span><br/>                | <span data-ttu-id="29be1-147">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="29be1-147">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="29be1-148">MOF</span><span class="sxs-lookup"><span data-stu-id="29be1-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29be1-149"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="29be1-149"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29be1-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29be1-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29be1-151">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="29be1-151">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="29be1-152">**Modify-Methode der MicrosoftDNS- \_ atyp-Klasse**</span><span class="sxs-lookup"><span data-stu-id="29be1-152">**Modify Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-modify.md)
</dt> </dl>

 

 





