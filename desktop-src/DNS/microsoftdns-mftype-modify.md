---
title: Modify-Methode der MicrosoftDNS_MFType-Klasse
description: Die Modify-Methode aktualisiert einen e-Mail-Weiterleitungs-Agent für eine Domänen Ressource (MF).
ms.assetid: b4bc43a5-6f43-487d-ad6c-3e01d5b2b6b8
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_MFType-Klasse
- DNS-MicrosoftDNS_MFType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0a363290580c7cecf47dbe00c6dd7895d23dbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477841"
---
# <a name="modify-method-of-the-microsoftdns_mftype-class"></a><span data-ttu-id="8a0ab-106">Modify-Methode der MicrosoftDNS \_ mftype-Klasse</span><span class="sxs-lookup"><span data-stu-id="8a0ab-106">Modify method of the MicrosoftDNS\_MFType class</span></span>

<span data-ttu-id="8a0ab-107">Die **Modify** -Methode aktualisiert einen e-Mail-Weiterleitungs-Agent für eine Domänen Ressource (MF).</span><span class="sxs-lookup"><span data-stu-id="8a0ab-107">The **Modify** method updates a Mail Forwarding Agent for Domain (MF) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a0ab-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a0ab-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MFHost,
  [out, ref]     MicrosoftDNS_MFType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="8a0ab-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a0ab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a0ab-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8a0ab-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a0ab-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="8a0ab-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="8a0ab-112">*MF-Host* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8a0ab-112">*MFHost* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a0ab-113">Der Name des Hosts, der den postweiterleitungs-Agent bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8a0ab-113">Name of the host that provides the mail forwarding agent.</span></span>

</dd> <dt>

<span data-ttu-id="8a0ab-114">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="8a0ab-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8a0ab-115">Verweis auf das geänderte Objekt.</span><span class="sxs-lookup"><span data-stu-id="8a0ab-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a0ab-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a0ab-116">Return value</span></span>

<span data-ttu-id="8a0ab-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8a0ab-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a0ab-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a0ab-118">Remarks</span></span>

<span data-ttu-id="8a0ab-119">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="8a0ab-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a0ab-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a0ab-120">Requirements</span></span>



| <span data-ttu-id="8a0ab-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a0ab-121">Requirement</span></span> | <span data-ttu-id="8a0ab-122">Wert</span><span class="sxs-lookup"><span data-stu-id="8a0ab-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a0ab-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8a0ab-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8a0ab-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8a0ab-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8a0ab-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8a0ab-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8a0ab-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8a0ab-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8a0ab-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="8a0ab-127">Namespace</span></span><br/>                | <span data-ttu-id="8a0ab-128">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="8a0ab-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="8a0ab-129">MOF</span><span class="sxs-lookup"><span data-stu-id="8a0ab-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a0ab-130"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8a0ab-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a0ab-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a0ab-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a0ab-132">**MicrosoftDNS- \_ mftype**</span><span class="sxs-lookup"><span data-stu-id="8a0ab-132">**MicrosoftDNS\_MFType**</span></span>](microsoftdns-mftype.md)
</dt> <dt>

[<span data-ttu-id="8a0ab-133">**Methode "kreateinzustancefrompropertydata" der MicrosoftDNS- \_ Klasse "mftype"**</span><span class="sxs-lookup"><span data-stu-id="8a0ab-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MFType Class**</span></span>](microsoftdns-mftype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="8a0ab-134">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="8a0ab-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





