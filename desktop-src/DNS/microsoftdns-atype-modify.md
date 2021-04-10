---
title: Modify-Methode der MicrosoftDNS_AType-Klasse
description: Die Modify-Methode aktualisiert die Gültigkeitsdauer und die IP-Adresse eines Ressourcen Datensatzes für die Host Adresse (a).
ms.assetid: fe01549d-7135-499d-a5a5-cd31ea106f53
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_AType-Klasse
- DNS-MicrosoftDNS_AType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ffda093ed843cfd655711100321c9876120519c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040619"
---
# <a name="modify-method-of-the-microsoftdns_atype-class"></a><span data-ttu-id="3324a-106">Modify-Methode der MicrosoftDNS- \_ atyp-Klasse</span><span class="sxs-lookup"><span data-stu-id="3324a-106">Modify method of the MicrosoftDNS\_AType class</span></span>

<span data-ttu-id="3324a-107">Die **Modify** -Methode aktualisiert die Gültigkeitsdauer und die IP-Adresse eines Ressourcen Datensatzes für die Host Adresse (a).</span><span class="sxs-lookup"><span data-stu-id="3324a-107">The **Modify** method updates the TTL and IP address of a host Address (A) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="3324a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3324a-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32             TTL,
  [in, optional] string             IPAddress,
  [out, ref]     MicrosoftDNS_AType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="3324a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3324a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3324a-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3324a-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3324a-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="3324a-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="3324a-112">*IPAddress* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3324a-112">*IPAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3324a-113">Zeichenfolge, die die IP-Adresse des Hosts darstellt.</span><span class="sxs-lookup"><span data-stu-id="3324a-113">String representing the IP address of the host.</span></span>

</dd> <dt>

<span data-ttu-id="3324a-114">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="3324a-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="3324a-115">Verweis auf das geänderte Objekt.</span><span class="sxs-lookup"><span data-stu-id="3324a-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3324a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3324a-116">Return value</span></span>

<span data-ttu-id="3324a-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3324a-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3324a-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3324a-118">Remarks</span></span>

<span data-ttu-id="3324a-119">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="3324a-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="3324a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3324a-120">Requirements</span></span>



| <span data-ttu-id="3324a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3324a-121">Requirement</span></span> | <span data-ttu-id="3324a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="3324a-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3324a-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3324a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3324a-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3324a-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3324a-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3324a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3324a-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3324a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3324a-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="3324a-127">Namespace</span></span><br/>                | <span data-ttu-id="3324a-128">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="3324a-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="3324a-129">MOF</span><span class="sxs-lookup"><span data-stu-id="3324a-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3324a-130"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3324a-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3324a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3324a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3324a-132">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="3324a-132">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="3324a-133">**Methode "kreateinzustancefrompropertydata" der Klasse "MicrosoftDNS \_ aType"**</span><span class="sxs-lookup"><span data-stu-id="3324a-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AType Class**</span></span>](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> </dl>

 

 





