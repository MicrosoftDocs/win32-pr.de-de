---
title: Modify-Methode der MicrosoftDNS_SRVType-Klasse
description: Die Modify-Methode aktualisiert einen Dienst Ressourcen Daten Satz (SRV).
ms.assetid: 626483c9-4b36-4e62-b9ad-dd7bb18f2e1e
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_SRVType-Klasse
- DNS-MicrosoftDNS_SRVType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1174e7a8096d70a3e6305a5d24b9ae1f4915096e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040939"
---
# <a name="modify-method-of-the-microsoftdns_srvtype-class"></a><span data-ttu-id="d4c1a-106">Modify-Methode der MicrosoftDNS \_ srvtype-Klasse</span><span class="sxs-lookup"><span data-stu-id="d4c1a-106">Modify method of the MicrosoftDNS\_SRVType class</span></span>

<span data-ttu-id="d4c1a-107">Die **Modify** -Methode aktualisiert einen Dienst Ressourcen Daten Satz (SRV).</span><span class="sxs-lookup"><span data-stu-id="d4c1a-107">The **Modify** method updates a Service (SRV) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4c1a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4c1a-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Priority,
  [in, optional] uint16               Weight,
  [in, optional] uint16               Port,
  [in, optional] string               SRVDomainName,
  [out, ref]     MicrosoftDNS_SRVType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="d4c1a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4c1a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4c1a-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="d4c1a-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4c1a-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="d4c1a-112">*Priorität* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="d4c1a-112">*Priority* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4c1a-113">Priorität des im Besitzer Namen angegebenen Zielhosts.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-113">Priority of the target host specified in the owner name.</span></span> <span data-ttu-id="d4c1a-114">Niedrigere Zahlen implizieren höhere Prioritäten.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-114">Lower numbers imply higher priorities.</span></span>

</dd> <dt>

<span data-ttu-id="d4c1a-115">*Gewichtung* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="d4c1a-115">*Weight* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4c1a-116">Gewichtung des Zielhosts.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-116">Weight of the target host.</span></span> <span data-ttu-id="d4c1a-117">Dies ist hilfreich bei der Auswahl zwischen Hosts mit der gleichen Priorität.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-117">This is useful when selecting among hosts that have the same priority.</span></span> <span data-ttu-id="d4c1a-118">Die Wahrscheinlichkeit, diesen Host zu verwenden, sollte proportional zu seiner Gewichtung sein.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-118">The chances of using this host should be proportional to its weight.</span></span>

</dd> <dt>

<span data-ttu-id="d4c1a-119">*Port* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="d4c1a-119">*Port* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4c1a-120">Port, der auf dem Zielhost eines Protokoll Diensts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-120">Port used on the target host of a protocol service.</span></span>

</dd> <dt>

<span data-ttu-id="d4c1a-121">*Srvdomainname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="d4c1a-121">*SRVDomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4c1a-122">Der voll qualifizierte Namen des Zielhosts.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-122">FQDN of the target host.</span></span> <span data-ttu-id="d4c1a-123">Ein Ziel von \\ . \\ bedeutet, dass der Dienst in dieser Domäne nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-123">A target of \\.\\ means that the service is decidedly not available at this domain.</span></span>

</dd> <dt>

<span data-ttu-id="d4c1a-124">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="d4c1a-124">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d4c1a-125">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-125">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4c1a-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d4c1a-126">Return value</span></span>

<span data-ttu-id="d4c1a-127">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-127">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4c1a-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4c1a-128">Remarks</span></span>

<span data-ttu-id="d4c1a-129">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-129">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4c1a-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4c1a-130">Requirements</span></span>



| <span data-ttu-id="d4c1a-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4c1a-131">Requirement</span></span> | <span data-ttu-id="d4c1a-132">Wert</span><span class="sxs-lookup"><span data-stu-id="d4c1a-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4c1a-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4c1a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d4c1a-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d4c1a-134">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d4c1a-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4c1a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d4c1a-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4c1a-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d4c1a-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="d4c1a-137">Namespace</span></span><br/>                | <span data-ttu-id="d4c1a-138">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="d4c1a-138">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="d4c1a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="d4c1a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4c1a-140"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d4c1a-140"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4c1a-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4c1a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4c1a-142">**MicrosoftDNS- \_ srvtype**</span><span class="sxs-lookup"><span data-stu-id="d4c1a-142">**MicrosoftDNS\_SRVType**</span></span>](microsoftdns-srvtype.md)
</dt> <dt>

[<span data-ttu-id="d4c1a-143">**Die Methode "kreateinstancefrompropertydata" der Klasse "srvtype" von MicrosoftDNS \_**</span><span class="sxs-lookup"><span data-stu-id="d4c1a-143">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_SRVType Class**</span></span>](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="d4c1a-144">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="d4c1a-144">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





