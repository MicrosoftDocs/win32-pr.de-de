---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_RTType-Klasse
description: Die Methode "kreatinstancefrompropertydata" instanziiert einen Routen-through-Ressourcen Daten Satz (RT).
ms.assetid: 1ebb0543-d031-4430-acbe-708c4931b7a4
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_RTType
- DNS-MicrosoftDNS_RTType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c3b8d71c41fefa9b78aa9a469ee1426c553e1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517942"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_rttype-class"></a><span data-ttu-id="f0919-106">Methode "kreateinzustancefrompropertydata" der Klasse "MicrosoftDNS \_ rttype"</span><span class="sxs-lookup"><span data-stu-id="f0919-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_RTType class</span></span>

<span data-ttu-id="f0919-107">Die Methode " **kreatinstancefrompropertydata** " instanziiert einen Routen-through-Ressourcen Daten Satz (RT).</span><span class="sxs-lookup"><span data-stu-id="f0919-107">The **CreateInstanceFromPropertyData** method instantiates a Route Through (RT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0919-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0919-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           uint16              Preference,
  [in]           string              IntermediateHost,
  [out, ref]     MicrosoftDNS_RTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="f0919-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0919-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0919-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0919-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0919-111">Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="f0919-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="f0919-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0919-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0919-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="f0919-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="f0919-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0919-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0919-115">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="f0919-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="f0919-116">*Recordclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="f0919-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f0919-117">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="f0919-117">Class of the RR.</span></span> <span data-ttu-id="f0919-118">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="f0919-118">Default value is 1.</span></span> <span data-ttu-id="f0919-119">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="f0919-119">The following values are valid.</span></span>



| <span data-ttu-id="f0919-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f0919-120">Value</span></span>                                                                                                | <span data-ttu-id="f0919-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f0919-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="f0919-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="f0919-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="f0919-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="f0919-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="f0919-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="f0919-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="f0919-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="f0919-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="f0919-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="f0919-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="f0919-127">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="f0919-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="f0919-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="f0919-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="f0919-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="f0919-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="f0919-130">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="f0919-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f0919-131">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f0919-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="f0919-132">*Bevorzugen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0919-132">*Preference* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0919-133">Die Einstellung, die diesem RR unter anderem beim gleichen Besitzer zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f0919-133">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="f0919-134">Niedrigere Werte werden bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="f0919-134">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="f0919-135">*Intermediatehost* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0919-135">*IntermediateHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0919-136">FQDN, der einen Host angibt, der als zwischengeschalteter Host zum Erreichen des vom Besitzer angegebenen Hosts dienen soll.</span><span class="sxs-lookup"><span data-stu-id="f0919-136">FQDN specifying a host to serve as an intermediate in reaching the host specified by owner.</span></span>

</dd> <dt>

<span data-ttu-id="f0919-137">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="f0919-137">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f0919-138">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f0919-138">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0919-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0919-139">Return value</span></span>

<span data-ttu-id="f0919-140">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f0919-140">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0919-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0919-141">Requirements</span></span>



| <span data-ttu-id="f0919-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0919-142">Requirement</span></span> | <span data-ttu-id="f0919-143">Wert</span><span class="sxs-lookup"><span data-stu-id="f0919-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0919-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0919-144">Minimum supported client</span></span><br/> | <span data-ttu-id="f0919-145">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f0919-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f0919-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0919-146">Minimum supported server</span></span><br/> | <span data-ttu-id="f0919-147">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0919-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f0919-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="f0919-148">Namespace</span></span><br/>                | <span data-ttu-id="f0919-149">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="f0919-149">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f0919-150">MOF</span><span class="sxs-lookup"><span data-stu-id="f0919-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0919-151"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f0919-151"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0919-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0919-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0919-153">**MicrosoftDNS- \_ rttype**</span><span class="sxs-lookup"><span data-stu-id="f0919-153">**MicrosoftDNS\_RTType**</span></span>](microsoftdns-rttype.md)
</dt> <dt>

[<span data-ttu-id="f0919-154">**Modify-Methode der MicrosoftDNS \_ rttype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f0919-154">**Modify Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-modify.md)
</dt> <dt>

[<span data-ttu-id="f0919-155">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="f0919-155">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





