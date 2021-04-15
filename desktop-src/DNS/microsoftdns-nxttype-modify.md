---
title: Modify-Methode der MicrosoftDNS_NXTType-Klasse
description: Die Modify-Methode aktualisiert einen nächsten (NXT) Ressourcen Daten Satz.
ms.assetid: 5a21b843-0761-4022-b00a-9dbcd6814454
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_NXTType-Klasse
- DNS-MicrosoftDNS_NXTType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bab7bf8480c7e18914cac4f7ae0deb8a608090f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475879"
---
# <a name="modify-method-of-the-microsoftdns_nxttype-class"></a><span data-ttu-id="ac1f2-106">Modify-Methode der MicrosoftDNS- \_ nxttype-Klasse</span><span class="sxs-lookup"><span data-stu-id="ac1f2-106">Modify method of the MicrosoftDNS\_NXTType class</span></span>

<span data-ttu-id="ac1f2-107">Die **Modify** -Methode aktualisiert einen nächsten (NXT) Ressourcen Daten Satz.</span><span class="sxs-lookup"><span data-stu-id="ac1f2-107">The **Modify** method updates a Next (NXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac1f2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac1f2-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               NextDomainName,
  [in]           string               Types,
  [out, ref]     MicrosoftDNS_NXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="ac1f2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac1f2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac1f2-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ac1f2-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ac1f2-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ac1f2-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="ac1f2-112">*Nextdomainname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac1f2-112">*NextDomainName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac1f2-113">Der nächste Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="ac1f2-113">Next domain name.</span></span>

</dd> <dt>

<span data-ttu-id="ac1f2-114">*Typen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac1f2-114">*Types* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac1f2-115">Durch Leerzeichen getrennte Liste der RR-Type-mnetmonics für den Besitzer Namen des NXT-Ressourcen Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="ac1f2-115">Space-separated list of the RR-type mnemonics for the owner name of the NXT Resource Record.</span></span>

</dd> <dt>

<span data-ttu-id="ac1f2-116">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="ac1f2-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ac1f2-117">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ac1f2-117">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac1f2-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac1f2-118">Return value</span></span>

<span data-ttu-id="ac1f2-119">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ac1f2-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac1f2-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac1f2-120">Remarks</span></span>

<span data-ttu-id="ac1f2-121">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="ac1f2-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac1f2-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac1f2-122">Requirements</span></span>



| <span data-ttu-id="ac1f2-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac1f2-123">Requirement</span></span> | <span data-ttu-id="ac1f2-124">Wert</span><span class="sxs-lookup"><span data-stu-id="ac1f2-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac1f2-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac1f2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ac1f2-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ac1f2-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ac1f2-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac1f2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ac1f2-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac1f2-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ac1f2-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac1f2-129">Namespace</span></span><br/>                | <span data-ttu-id="ac1f2-130">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="ac1f2-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ac1f2-131">MOF</span><span class="sxs-lookup"><span data-stu-id="ac1f2-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac1f2-132"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ac1f2-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac1f2-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac1f2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac1f2-134">**MicrosoftDNS \_ nxttype**</span><span class="sxs-lookup"><span data-stu-id="ac1f2-134">**MicrosoftDNS\_NXTType**</span></span>](microsoftdns-nxttype.md)
</dt> <dt>

[<span data-ttu-id="ac1f2-135">**Die Methode "kreateinzustancefrompropertydata" der Klasse "MicrosoftDNS \_ nxttype"**</span><span class="sxs-lookup"><span data-stu-id="ac1f2-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_NXTType Class**</span></span>](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ac1f2-136">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="ac1f2-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





