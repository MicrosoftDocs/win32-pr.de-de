---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_MXType-Klasse
description: Die Methode "kreatinstancefrompropertydata" instanziiert einen e-Mail-Austausch Ressourcen Eintrag (Mr).
ms.assetid: 5724b14a-bb64-460c-ac49-28bac85b8620
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_MXType
- DNS-MicrosoftDNS_MXType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8154e8ccdc6ac18824e2d56597ac8e0f186f3912
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103851"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mxtype-class"></a><span data-ttu-id="f0424-106">Die Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ mxtype-Klasse</span><span class="sxs-lookup"><span data-stu-id="f0424-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MXType class</span></span>

<span data-ttu-id="f0424-107">Die Methode " **kreatinstancefrompropertydata** " instanziiert einen e-Mail-Austausch Ressourcen Eintrag (Mr).</span><span class="sxs-lookup"><span data-stu-id="f0424-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Exchanger (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0424-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0424-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           uint16              Preference,
  [in]           string              MailExchange,
  [out, ref]     MicrosoftDNS_MXType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="f0424-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0424-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0424-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0424-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0424-111">Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="f0424-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="f0424-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0424-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0424-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="f0424-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="f0424-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0424-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0424-115">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="f0424-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="f0424-116">*Recordclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="f0424-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f0424-117">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="f0424-117">Class of the RR.</span></span> <span data-ttu-id="f0424-118">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="f0424-118">Default value is 1.</span></span> <span data-ttu-id="f0424-119">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="f0424-119">The following values are valid.</span></span>



| <span data-ttu-id="f0424-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f0424-120">Value</span></span>                                                                                                | <span data-ttu-id="f0424-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f0424-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="f0424-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="f0424-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="f0424-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="f0424-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="f0424-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="f0424-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="f0424-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="f0424-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="f0424-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="f0424-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="f0424-127">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="f0424-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="f0424-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="f0424-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="f0424-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="f0424-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="f0424-130">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="f0424-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f0424-131">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f0424-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="f0424-132">*Bevorzugen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0424-132">*Preference* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0424-133">Die Einstellung, die diesem RR unter anderem beim gleichen Besitzer zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f0424-133">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="f0424-134">Niedrigere Werte werden bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="f0424-134">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="f0424-135">*Mailexchange* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f0424-135">*MailExchange* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0424-136">FQDN, der einen Host angibt, der als e-Mail-Austausch für den Namen des Besitzers fungieren soll.</span><span class="sxs-lookup"><span data-stu-id="f0424-136">FQDN specifying a host willing to act as a mail exchange for the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="f0424-137">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="f0424-137">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f0424-138">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f0424-138">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0424-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0424-139">Return value</span></span>

<span data-ttu-id="f0424-140">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f0424-140">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0424-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0424-141">Requirements</span></span>



| <span data-ttu-id="f0424-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0424-142">Requirement</span></span> | <span data-ttu-id="f0424-143">Wert</span><span class="sxs-lookup"><span data-stu-id="f0424-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0424-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0424-144">Minimum supported client</span></span><br/> | <span data-ttu-id="f0424-145">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f0424-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f0424-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0424-146">Minimum supported server</span></span><br/> | <span data-ttu-id="f0424-147">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0424-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f0424-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="f0424-148">Namespace</span></span><br/>                | <span data-ttu-id="f0424-149">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="f0424-149">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f0424-150">MOF</span><span class="sxs-lookup"><span data-stu-id="f0424-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0424-151"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f0424-151"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0424-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0424-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0424-153">**MicrosoftDNS- \_ mxtype**</span><span class="sxs-lookup"><span data-stu-id="f0424-153">**MicrosoftDNS\_MXType**</span></span>](microsoftdns-mxtype.md)
</dt> <dt>

[<span data-ttu-id="f0424-154">**Modify-Methode der MicrosoftDNS- \_ mxtype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f0424-154">**Modify Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-modify.md)
</dt> <dt>

[<span data-ttu-id="f0424-155">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="f0424-155">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





