---
title: Modify-Methode der MicrosoftDNS_RTType-Klasse
description: Die Modify-Methode aktualisiert einen Route-through-Ressourcen Daten Satz (RT).
ms.assetid: 80053ae6-8ce8-4aa1-be2b-aac9daa5dae3
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_RTType-Klasse
- DNS-MicrosoftDNS_RTType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8267bf1dc256ec95a456978643226ab5c01af93f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517939"
---
# <a name="modify-method-of-the-microsoftdns_rttype-class"></a><span data-ttu-id="ffe4e-106">Modify-Methode der MicrosoftDNS \_ rttype-Klasse</span><span class="sxs-lookup"><span data-stu-id="ffe4e-106">Modify method of the MicrosoftDNS\_RTType class</span></span>

<span data-ttu-id="ffe4e-107">Die **Modify** -Methode aktualisiert einen Route-through-Ressourcen Daten Satz (RT).</span><span class="sxs-lookup"><span data-stu-id="ffe4e-107">The **Modify** method updates a Route Through (RT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffe4e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffe4e-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              IntermediateHost,
  [out, ref]     MicrosoftDNS_RTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="ffe4e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffe4e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffe4e-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ffe4e-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ffe4e-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ffe4e-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="ffe4e-112">*Bevorzugen* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ffe4e-112">*Preference* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ffe4e-113">Die Einstellung, die diesem RR unter anderem beim gleichen Besitzer zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ffe4e-113">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="ffe4e-114">Niedrigere Werte werden bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="ffe4e-114">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="ffe4e-115">*Intermediatehost* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ffe4e-115">*IntermediateHost* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ffe4e-116">FQDN, der einen Host angibt, der als zwischengeschalteter Host zum Erreichen des vom Besitzer angegebenen Hosts dienen soll.</span><span class="sxs-lookup"><span data-stu-id="ffe4e-116">FQDN specifying a host to serve as an intermediate in reaching the host specified by owner.</span></span>

</dd> <dt>

<span data-ttu-id="ffe4e-117">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="ffe4e-117">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ffe4e-118">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ffe4e-118">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffe4e-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ffe4e-119">Return value</span></span>

<span data-ttu-id="ffe4e-120">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ffe4e-120">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffe4e-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ffe4e-121">Remarks</span></span>

<span data-ttu-id="ffe4e-122">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="ffe4e-122">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffe4e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffe4e-123">Requirements</span></span>



| <span data-ttu-id="ffe4e-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ffe4e-124">Requirement</span></span> | <span data-ttu-id="ffe4e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="ffe4e-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffe4e-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ffe4e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ffe4e-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ffe4e-127">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ffe4e-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ffe4e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ffe4e-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ffe4e-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ffe4e-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="ffe4e-130">Namespace</span></span><br/>                | <span data-ttu-id="ffe4e-131">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="ffe4e-131">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ffe4e-132">MOF</span><span class="sxs-lookup"><span data-stu-id="ffe4e-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffe4e-133"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ffe4e-133"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffe4e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ffe4e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffe4e-135">**MicrosoftDNS- \_ rttype**</span><span class="sxs-lookup"><span data-stu-id="ffe4e-135">**MicrosoftDNS\_RTType**</span></span>](microsoftdns-rttype.md)
</dt> <dt>

[<span data-ttu-id="ffe4e-136">**Methode "kreateinzustancefrompropertydata" der Klasse "MicrosoftDNS \_ rttype"**</span><span class="sxs-lookup"><span data-stu-id="ffe4e-136">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RTType Class**</span></span>](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="ffe4e-137">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="ffe4e-137">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





