---
title: Modify-Methode der MicrosoftDNS_PTRType-Klasse
description: Die Modify-Methode aktualisiert einen Zeiger (PTR)-Ressourcen Daten Satz.
ms.assetid: 801a6bc9-e384-4912-a73a-6b04a1655002
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_PTRType-Klasse
- DNS-MicrosoftDNS_PTRType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 840bf100ea5cdbbb606837e90d8fa9fcebab57fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956623"
---
# <a name="modify-method-of-the-microsoftdns_ptrtype-class"></a><span data-ttu-id="8e1a5-106">Modify-Methode der MicrosoftDNS \_ ptrtype-Klasse</span><span class="sxs-lookup"><span data-stu-id="8e1a5-106">Modify method of the MicrosoftDNS\_PTRType class</span></span>

<span data-ttu-id="8e1a5-107">Die **Modify** -Methode aktualisiert einen Zeiger (PTR)-Ressourcen Daten Satz.</span><span class="sxs-lookup"><span data-stu-id="8e1a5-107">The **Modify** method updates a Pointer (PTR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e1a5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e1a5-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] string               PTRDomainName,
  [out, ref]     MicrosoftDNS_PTRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="8e1a5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e1a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e1a5-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8e1a5-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1a5-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="8e1a5-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="8e1a5-112">*Ptrdomainname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8e1a5-112">*PTRDomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1a5-113">Die Domänen Namen Adresse des PTR-Einsatzes.</span><span class="sxs-lookup"><span data-stu-id="8e1a5-113">Domain name address of the PTR record.</span></span>

</dd> <dt>

<span data-ttu-id="8e1a5-114">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="8e1a5-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8e1a5-115">Verweis auf das geänderte Objekt.</span><span class="sxs-lookup"><span data-stu-id="8e1a5-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e1a5-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e1a5-116">Return value</span></span>

<span data-ttu-id="8e1a5-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8e1a5-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e1a5-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e1a5-118">Remarks</span></span>

<span data-ttu-id="8e1a5-119">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="8e1a5-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e1a5-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e1a5-120">Requirements</span></span>



| <span data-ttu-id="8e1a5-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e1a5-121">Requirement</span></span> | <span data-ttu-id="8e1a5-122">Wert</span><span class="sxs-lookup"><span data-stu-id="8e1a5-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e1a5-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e1a5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8e1a5-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8e1a5-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8e1a5-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e1a5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8e1a5-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e1a5-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8e1a5-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="8e1a5-127">Namespace</span></span><br/>                | <span data-ttu-id="8e1a5-128">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="8e1a5-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="8e1a5-129">MOF</span><span class="sxs-lookup"><span data-stu-id="8e1a5-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e1a5-130"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8e1a5-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e1a5-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e1a5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e1a5-132">**MicrosoftDNS \_ ptrtype**</span><span class="sxs-lookup"><span data-stu-id="8e1a5-132">**MicrosoftDNS\_PTRType**</span></span>](microsoftdns-ptrtype.md)
</dt> <dt>

[<span data-ttu-id="8e1a5-133">**Die Methode "kreateinstancefrompropertydata" der Klasse "MicrosoftDNS \_ ptrtype"**</span><span class="sxs-lookup"><span data-stu-id="8e1a5-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="8e1a5-134">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="8e1a5-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





