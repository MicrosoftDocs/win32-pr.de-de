---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_MINFOType-Klasse
description: Die Methode "kreateinstancefrompropertydata" instanziiert einen Ressourcen Eintrag für e-Mail-Informationen (MINFO).
ms.assetid: 693b4b19-cbdd-48d5-89e0-a700a60477aa
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_MINFOType
- DNS-MicrosoftDNS_MINFOType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a565b1575dc51a59a09faea6fd271d719518f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040136"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_minfotype-class"></a><span data-ttu-id="268a7-106">Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ minfotype-Klasse</span><span class="sxs-lookup"><span data-stu-id="268a7-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_MINFOType class</span></span>

<span data-ttu-id="268a7-107">Die Methode " **kreateinstancefrompropertydata** " instanziiert einen Ressourcen Eintrag für e-Mail-Informationen (MINFO).</span><span class="sxs-lookup"><span data-stu-id="268a7-107">The **CreateInstanceFromPropertyData** method instantiates a Mail Information (MINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="268a7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="268a7-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           string                 ResponsibleMailbox,
  [in]           string                 ErrorMailbox,
  [out, ref]     MicrosoftDNS_MINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="268a7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="268a7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="268a7-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="268a7-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="268a7-111">Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="268a7-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="268a7-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="268a7-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="268a7-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="268a7-113">Name of the Container for the Zone, Cache, or RootHints instance that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="268a7-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="268a7-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="268a7-115">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="268a7-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="268a7-116">*Recordclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="268a7-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="268a7-117">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="268a7-117">Class of the RR.</span></span> <span data-ttu-id="268a7-118">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="268a7-118">Default value is 1.</span></span> <span data-ttu-id="268a7-119">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="268a7-119">The following values are valid.</span></span>



| <span data-ttu-id="268a7-120">Wert</span><span class="sxs-lookup"><span data-stu-id="268a7-120">Value</span></span>                                                                                                | <span data-ttu-id="268a7-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="268a7-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="268a7-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="268a7-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="268a7-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="268a7-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="268a7-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="268a7-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="268a7-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="268a7-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="268a7-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="268a7-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="268a7-127">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="268a7-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="268a7-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="268a7-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="268a7-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="268a7-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="268a7-130">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="268a7-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="268a7-131">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="268a7-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="268a7-132">" *Verantworblemailbox* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="268a7-132">*ResponsibleMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="268a7-133">Der voll qualifizierte Name ist ein Postfach, das für die Mailingliste oder das Postfach zuständig ist, die im Besitzer Namen des Datensatzes angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="268a7-133">FQDN specifying a mailbox responsible for the mailing list or mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="268a7-134">*Errormailbox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="268a7-134">*ErrorMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="268a7-135">FQDN, der ein Postfach für den Empfang von Fehlermeldungen in Bezug auf die Mailingliste oder das Postfach angibt, das durch den Besitzer Namen des MINFO-Datensatzes angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="268a7-135">FQDN specifying a mailbox to receive error messages related to either the mailing list, or to the mailbox specified by the owner name of the MINFO record.</span></span>

</dd> <dt>

<span data-ttu-id="268a7-136">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="268a7-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="268a7-137">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="268a7-137">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="268a7-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="268a7-138">Return value</span></span>

<span data-ttu-id="268a7-139">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="268a7-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="268a7-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="268a7-140">Requirements</span></span>



| <span data-ttu-id="268a7-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="268a7-141">Requirement</span></span> | <span data-ttu-id="268a7-142">Wert</span><span class="sxs-lookup"><span data-stu-id="268a7-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="268a7-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="268a7-143">Minimum supported client</span></span><br/> | <span data-ttu-id="268a7-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="268a7-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="268a7-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="268a7-145">Minimum supported server</span></span><br/> | <span data-ttu-id="268a7-146">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="268a7-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="268a7-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="268a7-147">Namespace</span></span><br/>                | <span data-ttu-id="268a7-148">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="268a7-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="268a7-149">MOF</span><span class="sxs-lookup"><span data-stu-id="268a7-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="268a7-150"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="268a7-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="268a7-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="268a7-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="268a7-152">**MicrosoftDNS- \_ minfotype**</span><span class="sxs-lookup"><span data-stu-id="268a7-152">**MicrosoftDNS\_MINFOType**</span></span>](microsoftdns-minfotype.md)
</dt> <dt>

[<span data-ttu-id="268a7-153">**Modify-Methode der MicrosoftDNS- \_ minfotype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="268a7-153">**Modify Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-modify.md)
</dt> <dt>

[<span data-ttu-id="268a7-154">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="268a7-154">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





