---
title: Modify-Methode der MicrosoftDNS_AAAAType-Klasse
description: Die Modify-Methode aktualisiert einen Ressourcen Daten Satz der IPv6-Adresse (AAAA).
ms.assetid: d58f8a88-8473-4b26-89f0-237d2457f00b
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_AAAAType-Klasse
- DNS-MicrosoftDNS_AAAAType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc216233fe3d41e4f1e31fe0d471e766c4dc8476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858906"
---
# <a name="modify-method-of-the-microsoftdns_aaaatype-class"></a><span data-ttu-id="47ade-106">Modify-Methode der MicrosoftDNS \_ aaaatype-Klasse</span><span class="sxs-lookup"><span data-stu-id="47ade-106">Modify method of the MicrosoftDNS\_AAAAType class</span></span>

<span data-ttu-id="47ade-107">Die **Modify** -Methode aktualisiert einen Ressourcen Daten Satz der IPv6-Adresse (AAAA).</span><span class="sxs-lookup"><span data-stu-id="47ade-107">The **Modify** method updates an IPv6 address (AAAA) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="47ade-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="47ade-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] string                IPv6Address,
  [out, ref]     MicrosoftDNS_AAAAType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="47ade-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="47ade-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47ade-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="47ade-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="47ade-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="47ade-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="47ade-112">*IPv6Address* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="47ade-112">*IPv6Address* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="47ade-113">IPv6-Adresse für den Host.</span><span class="sxs-lookup"><span data-stu-id="47ade-113">IPv6 address for the host.</span></span>

</dd> <dt>

<span data-ttu-id="47ade-114">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="47ade-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="47ade-115">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="47ade-115">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47ade-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47ade-116">Return value</span></span>

<span data-ttu-id="47ade-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="47ade-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="47ade-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47ade-118">Remarks</span></span>

<span data-ttu-id="47ade-119">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="47ade-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="47ade-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47ade-120">Requirements</span></span>



| <span data-ttu-id="47ade-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47ade-121">Requirement</span></span> | <span data-ttu-id="47ade-122">Wert</span><span class="sxs-lookup"><span data-stu-id="47ade-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47ade-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="47ade-123">Minimum supported client</span></span><br/> | <span data-ttu-id="47ade-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="47ade-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="47ade-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="47ade-125">Minimum supported server</span></span><br/> | <span data-ttu-id="47ade-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47ade-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="47ade-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="47ade-127">Namespace</span></span><br/>                | <span data-ttu-id="47ade-128">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="47ade-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="47ade-129">MOF</span><span class="sxs-lookup"><span data-stu-id="47ade-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47ade-130"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="47ade-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47ade-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47ade-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47ade-132">**MicrosoftDNS \_ aaaatype**</span><span class="sxs-lookup"><span data-stu-id="47ade-132">**MicrosoftDNS\_AAAAType**</span></span>](microsoftdns-aaaatype.md)
</dt> <dt>

[<span data-ttu-id="47ade-133">**Methode "kreateinzustancefrompropertydata" der Klasse "MicrosoftDNS \_ aaaatype"**</span><span class="sxs-lookup"><span data-stu-id="47ade-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_AAAAType Class**</span></span>](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="47ade-134">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="47ade-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





