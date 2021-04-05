---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_MBType-Klasse
description: Die Methode "kreatinstancefrompropertydata" instanziiert einen Post Fach Ressourcen Eintrag (MB).
ms.assetid: ac160a4d-2af7-428e-9cbd-bdd28f7c0910
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_MBType
- DNS-MicrosoftDNS_MBType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e340d78057c12e58159a293468598da7dbf53e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858994"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mbtype-class"></a><span data-ttu-id="2d18d-106">Die Methode "kreateinstancefrompropertydata" der Klasse "MicrosoftDNS \_ mbtype"</span><span class="sxs-lookup"><span data-stu-id="2d18d-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MBType class</span></span>

<span data-ttu-id="2d18d-107">Die Methode " **kreatinstancefrompropertydata** " instanziiert einen Post Fach Ressourcen Eintrag (MB).</span><span class="sxs-lookup"><span data-stu-id="2d18d-107">The **CreateInstanceFromPropertyData** method instantiates a Mailbox (MB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d18d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d18d-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]       string              DnsServerName,
  [in]       string              ContainerName,
  [in]       string              OwnerName,
  [in]       uint32              RecordClass = 1,
  [in]       uint32              TTL,
  [in]       string              MBHost,
  [out, ref] MicrosoftDNS_MBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="2d18d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d18d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d18d-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d18d-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d18d-111">Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="2d18d-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="2d18d-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d18d-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d18d-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="2d18d-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="2d18d-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d18d-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d18d-115">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="2d18d-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="2d18d-116">*Recordclass* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d18d-116">*RecordClass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d18d-117">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="2d18d-117">Optional.</span></span> <span data-ttu-id="2d18d-118">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="2d18d-118">Class of the RR.</span></span> <span data-ttu-id="2d18d-119">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="2d18d-119">Default value is 1.</span></span> <span data-ttu-id="2d18d-120">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="2d18d-120">The following values are valid.</span></span>



| <span data-ttu-id="2d18d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="2d18d-121">Value</span></span>                                                                                                | <span data-ttu-id="2d18d-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2d18d-122">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="2d18d-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="2d18d-123"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="2d18d-124">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="2d18d-124">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="2d18d-125"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="2d18d-125"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="2d18d-126">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="2d18d-126">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="2d18d-127"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="2d18d-127"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="2d18d-128">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="2d18d-128">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="2d18d-129"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="2d18d-129"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="2d18d-130">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="2d18d-130">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="2d18d-131">Gültigkeitsdauer  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d18d-131">*TTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d18d-132">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="2d18d-132">Optional.</span></span> <span data-ttu-id="2d18d-133">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="2d18d-133">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="2d18d-134">*Mbhost* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d18d-134">*MBHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d18d-135">Der Postfach-Hostname für den RR.</span><span class="sxs-lookup"><span data-stu-id="2d18d-135">Mailbox host name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="2d18d-136">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="2d18d-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="2d18d-137">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2d18d-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d18d-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d18d-138">Return value</span></span>

<span data-ttu-id="2d18d-139">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2d18d-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d18d-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d18d-140">Requirements</span></span>



| <span data-ttu-id="2d18d-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d18d-141">Requirement</span></span> | <span data-ttu-id="2d18d-142">Wert</span><span class="sxs-lookup"><span data-stu-id="2d18d-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d18d-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2d18d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="2d18d-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2d18d-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2d18d-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2d18d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="2d18d-146">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d18d-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2d18d-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="2d18d-147">Namespace</span></span><br/>                | <span data-ttu-id="2d18d-148">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="2d18d-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="2d18d-149">MOF</span><span class="sxs-lookup"><span data-stu-id="2d18d-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d18d-150"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2d18d-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d18d-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d18d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d18d-152">**MicrosoftDNS \_ mbtype**</span><span class="sxs-lookup"><span data-stu-id="2d18d-152">**MicrosoftDNS\_MBType**</span></span>](microsoftdns-mbtype.md)
</dt> <dt>

[<span data-ttu-id="2d18d-153">**Modify-Methode der MicrosoftDNS- \_ Klasse von mbtype**</span><span class="sxs-lookup"><span data-stu-id="2d18d-153">**Modify Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="2d18d-154">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="2d18d-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





