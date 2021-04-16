---
title: Modify-Methode der MicrosoftDNS_CNAMEType-Klasse
description: Die Modify-Methode aktualisiert einen kanonischen Namens Ressourcen Daten Satz (CNAME).
ms.assetid: 7e550026-d901-44a0-86ac-520682232ccb
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_CNAMEType-Klasse
- DNS-MicrosoftDNS_CNAMEType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ddbe1e1592c4331be808340c216954cd8d7b14f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476761"
---
# <a name="modify-method-of-the-microsoftdns_cnametype-class"></a><span data-ttu-id="a8ada-106">Modify-Methode der MicrosoftDNS \_ cnametype-Klasse</span><span class="sxs-lookup"><span data-stu-id="a8ada-106">Modify method of the MicrosoftDNS\_CNAMEType class</span></span>

<span data-ttu-id="a8ada-107">Die **Modify** -Methode aktualisiert einen kanonischen Namens Ressourcen Daten Satz (CNAME).</span><span class="sxs-lookup"><span data-stu-id="a8ada-107">The **Modify** method updates a Canonical Name (CNAME) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8ada-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8ada-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 PrimaryName,
  [out, ref]     MicrosoftDNS_CNAMEType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="a8ada-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8ada-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8ada-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="a8ada-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a8ada-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a8ada-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="a8ada-112">*Primaryname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="a8ada-112">*PrimaryName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a8ada-113">Zeichenfolge, die den primären Namen für den CNAME-Datensatz darstellt.</span><span class="sxs-lookup"><span data-stu-id="a8ada-113">String representing the primary name for the CNAME record.</span></span>

</dd> <dt>

<span data-ttu-id="a8ada-114">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="a8ada-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="a8ada-115">Verweis auf das geänderte Objekt.</span><span class="sxs-lookup"><span data-stu-id="a8ada-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8ada-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8ada-116">Return value</span></span>

<span data-ttu-id="a8ada-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a8ada-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8ada-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8ada-118">Remarks</span></span>

<span data-ttu-id="a8ada-119">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="a8ada-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8ada-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8ada-120">Requirements</span></span>



| <span data-ttu-id="a8ada-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8ada-121">Requirement</span></span> | <span data-ttu-id="a8ada-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a8ada-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8ada-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8ada-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a8ada-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a8ada-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a8ada-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8ada-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a8ada-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8ada-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a8ada-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="a8ada-127">Namespace</span></span><br/>                | <span data-ttu-id="a8ada-128">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="a8ada-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="a8ada-129">MOF</span><span class="sxs-lookup"><span data-stu-id="a8ada-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8ada-130"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a8ada-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8ada-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8ada-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8ada-132">**MicrosoftDNS \_ cnametype**</span><span class="sxs-lookup"><span data-stu-id="a8ada-132">**MicrosoftDNS\_CNAMEType**</span></span>](microsoftdns-cnametype.md)
</dt> <dt>

[<span data-ttu-id="a8ada-133">**Die Methode "kreatinstancefrompropertydata" der MicrosoftDNS \_ cnametype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a8ada-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_CNAMEType Class**</span></span>](microsoftdns-cnametype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="a8ada-134">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="a8ada-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





