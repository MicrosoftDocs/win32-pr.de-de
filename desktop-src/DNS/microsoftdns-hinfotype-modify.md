---
title: Modify-Methode der MicrosoftDNS_HINFOType-Klasse
description: Die Modify-Methode aktualisiert einen hinfo-Ressourcen Daten Satz (Host Information).
ms.assetid: 8f8148f3-804f-4f99-8e79-606cd3cea660
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_HINFOType-Klasse
- DNS-MicrosoftDNS_HINFOType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29a01eb94d82d080142d3496bab5f7f0b9acac8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741545"
---
# <a name="modify-method-of-the-microsoftdns_hinfotype-class"></a><span data-ttu-id="26717-106">Modify-Methode der MicrosoftDNS- \_ hinfotype-Klasse</span><span class="sxs-lookup"><span data-stu-id="26717-106">Modify method of the MicrosoftDNS\_HINFOType class</span></span>

<span data-ttu-id="26717-107">Die **Modify** -Methode aktualisiert einen hinfo-Ressourcen Daten Satz (Host Information).</span><span class="sxs-lookup"><span data-stu-id="26717-107">The **Modify** method updates a Host Information (HINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="26717-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="26717-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 CPU,
  [in, optional] string                 OS,
  [out, ref]     MicrosoftDNS_HINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="26717-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="26717-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26717-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="26717-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="26717-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="26717-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="26717-112">*CPU* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="26717-112">*CPU* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="26717-113">Der CPU-Typ des Daten Satz Besitzers.</span><span class="sxs-lookup"><span data-stu-id="26717-113">CPU type of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="26717-114">*Betriebssystem* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="26717-114">*OS* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="26717-115">Das Betriebssystem des Daten Satz Besitzers.</span><span class="sxs-lookup"><span data-stu-id="26717-115">Operating system of the record owner.</span></span>

</dd> <dt>

<span data-ttu-id="26717-116">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="26717-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="26717-117">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="26717-117">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26717-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26717-118">Return value</span></span>

<span data-ttu-id="26717-119">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="26717-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="26717-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26717-120">Remarks</span></span>

<span data-ttu-id="26717-121">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="26717-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="26717-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26717-122">Requirements</span></span>



| <span data-ttu-id="26717-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26717-123">Requirement</span></span> | <span data-ttu-id="26717-124">Wert</span><span class="sxs-lookup"><span data-stu-id="26717-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26717-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26717-125">Minimum supported client</span></span><br/> | <span data-ttu-id="26717-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="26717-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="26717-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26717-127">Minimum supported server</span></span><br/> | <span data-ttu-id="26717-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26717-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="26717-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="26717-129">Namespace</span></span><br/>                | <span data-ttu-id="26717-130">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="26717-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="26717-131">MOF</span><span class="sxs-lookup"><span data-stu-id="26717-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26717-132"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="26717-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26717-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26717-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26717-134">**MicrosoftDNS \_ hinfotype**</span><span class="sxs-lookup"><span data-stu-id="26717-134">**MicrosoftDNS\_HINFOType**</span></span>](microsoftdns-hinfotype.md)
</dt> <dt>

[<span data-ttu-id="26717-135">**Methode "kreateinstancefrompropertydata" der "hinfotype"-Klasse von MicrosoftDNS \_**</span><span class="sxs-lookup"><span data-stu-id="26717-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_HINFOType Class**</span></span>](microsoftdns-hinfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="26717-136">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="26717-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





