---
title: Modify-Methode der MicrosoftDNS_SOAType-Klasse
description: Die Modify-Methode aktualisiert einen Start of Authority (SOA)-Ressourcen Daten Satz.
ms.assetid: 531b770d-9ac9-43da-8595-fbc175b51b23
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_SOAType-Klasse
- DNS-MicrosoftDNS_SOAType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff40abc7f4e93b7122a1c48889c17f9efc4f625
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040227"
---
# <a name="modify-method-of-the-microsoftdns_soatype-class"></a><span data-ttu-id="3cb03-106">Modify-Methode der MicrosoftDNS- \_ soatype-Klasse</span><span class="sxs-lookup"><span data-stu-id="3cb03-106">Modify method of the MicrosoftDNS\_SOAType class</span></span>

<span data-ttu-id="3cb03-107">Die **Modify** -Methode aktualisiert einen Start of Authority (SOA)-Ressourcen Daten Satz.</span><span class="sxs-lookup"><span data-stu-id="3cb03-107">The **Modify** method updates a Start Of Authority (SOA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cb03-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cb03-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               SerialNumber,
  [in, optional] string               PrimaryServer,
  [in, optional] string               ResponsibleParty,
  [in, optional] uint32               RefreshInterval,
  [in, optional] uint32               RetryDelay,
  [in, optional] uint32               ExpireLimit,
  [in, optional] uint32               MinimumTTL,
  [out, ref]     MicrosoftDNS_SOAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="3cb03-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cb03-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cb03-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3cb03-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3cb03-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="3cb03-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="3cb03-112">*SerialNumber* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3cb03-112">*SerialNumber* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3cb03-113">Eine SOA-Seriennummer, die angibt, wie oft die Zone aktualisiert wurde, und wird von [*sekundären Servern*](s-gly.md) verwendet, um zu bestimmen, ob eine Zonen Übertragung notwendig ist.</span><span class="sxs-lookup"><span data-stu-id="3cb03-113">SOA serial number representing the number of times the zone has been updated, used by [*secondary servers*](s-gly.md) to determine whether zone transfer is necessary.</span></span>

</dd> <dt>

<span data-ttu-id="3cb03-114">*Primaryserver* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3cb03-114">*PrimaryServer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3cb03-115">Der Name des primären Servers.</span><span class="sxs-lookup"><span data-stu-id="3cb03-115">Name of the primary server.</span></span>

</dd> <dt>

<span data-ttu-id="3cb03-116">*Verantwortliche Partei* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3cb03-116">*ResponsibleParty* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3cb03-117">Post Fach Adresse der verantwortlichen Partei in Form von Alias. Domain, z. b. xyz.Microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="3cb03-117">Mailbox address of the responsible party, in the form of alias.domain, such as xyz.microsoft.com.</span></span> <span data-ttu-id="3cb03-118">Beachten Sie die Verwendung eines Zeitraums anstelle eines bei-Symbol (@).</span><span class="sxs-lookup"><span data-stu-id="3cb03-118">Note the use of a period rather than an at symbol (@).</span></span>

</dd> <dt>

<span data-ttu-id="3cb03-119">*Aktuerfrischendes Intervall* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3cb03-119">*RefreshInterval* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3cb03-120">Zeit in Sekunden, bevor die Zone, in der dieser Datensatz enthalten ist, aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3cb03-120">Time, in seconds, before the zone containing this record should be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="3cb03-121">*RetryDelay* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3cb03-121">*RetryDelay* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3cb03-122">Die Zeit (in Sekunden), die der DNS-Server zwischen namens Auflösungs versuchen verzögert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3cb03-122">Time, in seconds, the DNS Server should delay between name resolution attempts.</span></span>

</dd> <dt>

<span data-ttu-id="3cb03-123">*Expirelimit* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3cb03-123">*ExpireLimit* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3cb03-124">Zeit (in Sekunden), die sekundäre Server auf eine Antwort vom primären Server warten sollten, bevor die Kopien der Zonendatei als ungültig verworfen werden.</span><span class="sxs-lookup"><span data-stu-id="3cb03-124">Time, in seconds, that secondary servers should wait for a response from the primary server before discarding their copies of the zone file as invalid.</span></span>

</dd> <dt>

<span data-ttu-id="3cb03-125">*Minimumttl* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3cb03-125">*MinimumTTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3cb03-126">TTL-Zeit (in Sekunden), die auf Ressourcen Einträge in der Zone angewendet wird, die nicht Ihre eigene Gültigkeitsdauer angeben.</span><span class="sxs-lookup"><span data-stu-id="3cb03-126">TTL time, in seconds, applied to resource records in the zone that do not specify their own TTL.</span></span>

</dd> <dt>

<span data-ttu-id="3cb03-127">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="3cb03-127">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="3cb03-128">Verweis auf das geänderte Objekt</span><span class="sxs-lookup"><span data-stu-id="3cb03-128">Reference to the modified object</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cb03-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3cb03-129">Return value</span></span>

<span data-ttu-id="3cb03-130">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3cb03-130">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cb03-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3cb03-131">Remarks</span></span>

<span data-ttu-id="3cb03-132">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="3cb03-132">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cb03-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3cb03-133">Requirements</span></span>



| <span data-ttu-id="3cb03-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3cb03-134">Requirement</span></span> | <span data-ttu-id="3cb03-135">Wert</span><span class="sxs-lookup"><span data-stu-id="3cb03-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3cb03-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3cb03-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3cb03-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3cb03-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3cb03-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3cb03-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3cb03-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3cb03-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3cb03-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="3cb03-140">Namespace</span></span><br/>                | <span data-ttu-id="3cb03-141">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="3cb03-141">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="3cb03-142">MOF</span><span class="sxs-lookup"><span data-stu-id="3cb03-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3cb03-143"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3cb03-143"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cb03-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3cb03-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cb03-145">**MicrosoftDNS- \_ soatype**</span><span class="sxs-lookup"><span data-stu-id="3cb03-145">**MicrosoftDNS\_SOAType**</span></span>](microsoftdns-soatype.md)
</dt> <dt>

[<span data-ttu-id="3cb03-146">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="3cb03-146">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





