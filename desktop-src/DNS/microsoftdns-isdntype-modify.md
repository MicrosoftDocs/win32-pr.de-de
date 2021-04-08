---
title: Modify-Methode der MicrosoftDNS_ISDNType-Klasse
description: Die Modify-Methode aktualisiert einen ISDN-Ressourcen Daten Satz.
ms.assetid: 09e23853-ca92-43a3-8bd9-7de10eb5eddc
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_ISDNType-Klasse
- DNS-MicrosoftDNS_ISDNType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c369a6650c834ff9f35af6389c346daec86a954
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949445"
---
# <a name="modify-method-of-the-microsoftdns_isdntype-class"></a><span data-ttu-id="fac6e-106">Modify-Methode der MicrosoftDNS- \_ isdntype-Klasse</span><span class="sxs-lookup"><span data-stu-id="fac6e-106">Modify method of the MicrosoftDNS\_ISDNType class</span></span>

<span data-ttu-id="fac6e-107">Die **Modify** -Methode aktualisiert einen ISDN-Ressourcen Daten Satz.</span><span class="sxs-lookup"><span data-stu-id="fac6e-107">The **Modify** method updates an ISDN Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="fac6e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fac6e-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] string                ISDNNumber,
  [in, optional] string                SubAddress,
  [out, ref]     MicrosoftDNS_ISDNType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="fac6e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fac6e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fac6e-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="fac6e-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fac6e-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="fac6e-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="fac6e-112">*Isdnnumber* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="fac6e-112">*ISDNNumber* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fac6e-113">ISDN-Nummer und DDI für den Besitzer des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="fac6e-113">ISDN number and DDI of the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="fac6e-114">*Unter Adresse* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="fac6e-114">*SubAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fac6e-115">Die untergeordnete Adresse des Besitzers, sofern definiert.</span><span class="sxs-lookup"><span data-stu-id="fac6e-115">Subaddress of the owner, if defined.</span></span>

</dd> <dt>

<span data-ttu-id="fac6e-116">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="fac6e-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="fac6e-117">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fac6e-117">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fac6e-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fac6e-118">Return value</span></span>

<span data-ttu-id="fac6e-119">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fac6e-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fac6e-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fac6e-120">Remarks</span></span>

<span data-ttu-id="fac6e-121">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="fac6e-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="fac6e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fac6e-122">Requirements</span></span>



| <span data-ttu-id="fac6e-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fac6e-123">Requirement</span></span> | <span data-ttu-id="fac6e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="fac6e-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fac6e-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fac6e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fac6e-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fac6e-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="fac6e-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fac6e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fac6e-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fac6e-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fac6e-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="fac6e-129">Namespace</span></span><br/>                | <span data-ttu-id="fac6e-130">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="fac6e-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="fac6e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="fac6e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fac6e-132"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fac6e-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fac6e-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fac6e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fac6e-134">**MicrosoftDNS \_ isdntype**</span><span class="sxs-lookup"><span data-stu-id="fac6e-134">**MicrosoftDNS\_ISDNType**</span></span>](microsoftdns-isdntype.md)
</dt> <dt>

[<span data-ttu-id="fac6e-135">**Die Methode "kreateinstancefrompropertydata" der Klasse "MicrosoftDNS \_ isdntype"**</span><span class="sxs-lookup"><span data-stu-id="fac6e-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_ISDNType Class**</span></span>](microsoftdns-isdntype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="fac6e-136">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="fac6e-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





