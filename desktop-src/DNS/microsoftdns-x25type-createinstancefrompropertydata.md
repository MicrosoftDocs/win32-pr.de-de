---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_X25Type-Klasse
description: Die Methode "kreatinstancefrompropertydata" instanziiert einen X. 25 (x25)-Ressourcen Eintrag.
ms.assetid: fe89f829-79b9-457e-b455-899b2706ef04
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_X25Type
- DNS-MicrosoftDNS_X25Type Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_X25Type.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f198bf7b843b5633acd0b1515e9e3573f5ebb55d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040755"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_x25type-class"></a><span data-ttu-id="af28c-106">Die Methode "kreateinzustancefrompropertydata" der X25Type-Klasse von MicrosoftDNS \_</span><span class="sxs-lookup"><span data-stu-id="af28c-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_X25Type class</span></span>

<span data-ttu-id="af28c-107">Die Methode " **kreatinstancefrompropertydata** " instanziiert einen X. 25 (x25)-Ressourcen Eintrag.</span><span class="sxs-lookup"><span data-stu-id="af28c-107">The **CreateInstanceFromPropertyData** method instantiates an X.25 (X25) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="af28c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="af28c-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               PSDNAddress,
  [out, ref]     MicrosoftDNS_X25Type &RR
);
```



## <a name="parameters"></a><span data-ttu-id="af28c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="af28c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af28c-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af28c-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af28c-111">Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="af28c-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="af28c-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af28c-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af28c-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="af28c-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="af28c-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af28c-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af28c-115">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="af28c-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="af28c-116">*Recordclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="af28c-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="af28c-117">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="af28c-117">Class of the RR.</span></span> <span data-ttu-id="af28c-118">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="af28c-118">Default value is 1.</span></span> <span data-ttu-id="af28c-119">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="af28c-119">The following values are valid.</span></span>



| <span data-ttu-id="af28c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="af28c-120">Value</span></span>                                                                                                | <span data-ttu-id="af28c-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="af28c-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="af28c-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="af28c-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="af28c-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="af28c-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="af28c-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="af28c-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="af28c-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="af28c-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="af28c-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="af28c-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="af28c-127">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="af28c-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="af28c-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="af28c-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="af28c-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="af28c-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="af28c-130">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="af28c-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="af28c-131">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="af28c-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="af28c-132">*Psdnaddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af28c-132">*PSDNAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af28c-133">PSDN-Adresse des Besitzers der RR.</span><span class="sxs-lookup"><span data-stu-id="af28c-133">PSDN address of the owner of the RR.</span></span>

</dd> <dt>

<span data-ttu-id="af28c-134">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="af28c-134">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="af28c-135">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="af28c-135">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af28c-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="af28c-136">Return value</span></span>

<span data-ttu-id="af28c-137">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="af28c-137">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="af28c-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af28c-138">Requirements</span></span>



| <span data-ttu-id="af28c-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af28c-139">Requirement</span></span> | <span data-ttu-id="af28c-140">Wert</span><span class="sxs-lookup"><span data-stu-id="af28c-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af28c-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="af28c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="af28c-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="af28c-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="af28c-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="af28c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="af28c-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af28c-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="af28c-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="af28c-145">Namespace</span></span><br/>                | <span data-ttu-id="af28c-146">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="af28c-146">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="af28c-147">MOF</span><span class="sxs-lookup"><span data-stu-id="af28c-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af28c-148"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="af28c-148"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af28c-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af28c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af28c-150">**MicrosoftDNS \_ X25Type**</span><span class="sxs-lookup"><span data-stu-id="af28c-150">**MicrosoftDNS\_X25Type**</span></span>](microsoftdns-x25type.md)
</dt> <dt>

[<span data-ttu-id="af28c-151">**Modify-Methode der MicrosoftDNS \_ X25Type-Klasse**</span><span class="sxs-lookup"><span data-stu-id="af28c-151">**Modify Method of the MicrosoftDNS\_X25Type Class**</span></span>](microsoftdns-x25type-modify.md)
</dt> <dt>

[<span data-ttu-id="af28c-152">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="af28c-152">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





