---
title: Modify-Methode der MicrosoftDNS_X25Type-Klasse
description: Die Modify-Methode aktualisiert einen X. 25 (x25)-Ressourcen Daten Satz.
ms.assetid: 2d82d67e-ae29-4ded-86fe-7db0ef5ed74f
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_X25Type-Klasse
- DNS-MicrosoftDNS_X25Type Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_X25Type.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10db2fa770d3da8487a712e631c41fdd4256bf7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104409"
---
# <a name="modify-method-of-the-microsoftdns_x25type-class"></a><span data-ttu-id="92b0c-106">Modify-Methode der MicrosoftDNS \_ X25Type-Klasse</span><span class="sxs-lookup"><span data-stu-id="92b0c-106">Modify method of the MicrosoftDNS\_X25Type class</span></span>

<span data-ttu-id="92b0c-107">Die **Modify** -Methode aktualisiert einen X. 25 (x25)-Ressourcen Daten Satz.</span><span class="sxs-lookup"><span data-stu-id="92b0c-107">The **Modify** method updates an X.25 (X25) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="92b0c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="92b0c-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] string               PSDNAddress,
  [out, ref]     MicrosoftDNS_X25Type &RR
);
```



## <a name="parameters"></a><span data-ttu-id="92b0c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="92b0c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92b0c-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="92b0c-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="92b0c-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="92b0c-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="92b0c-112">*Psdnaddress* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="92b0c-112">*PSDNAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="92b0c-113">PSDN-Adresse des Besitzers der RR.</span><span class="sxs-lookup"><span data-stu-id="92b0c-113">PSDN address of the owner of the RR.</span></span>

</dd> <dt>

<span data-ttu-id="92b0c-114">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="92b0c-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="92b0c-115">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="92b0c-115">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92b0c-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="92b0c-116">Return value</span></span>

<span data-ttu-id="92b0c-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="92b0c-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="92b0c-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92b0c-118">Remarks</span></span>

<span data-ttu-id="92b0c-119">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="92b0c-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="92b0c-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92b0c-120">Requirements</span></span>



| <span data-ttu-id="92b0c-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92b0c-121">Requirement</span></span> | <span data-ttu-id="92b0c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="92b0c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="92b0c-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="92b0c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="92b0c-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="92b0c-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="92b0c-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="92b0c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="92b0c-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="92b0c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="92b0c-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="92b0c-127">Namespace</span></span><br/>                | <span data-ttu-id="92b0c-128">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="92b0c-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="92b0c-129">MOF</span><span class="sxs-lookup"><span data-stu-id="92b0c-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92b0c-130"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="92b0c-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92b0c-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92b0c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92b0c-132">**MicrosoftDNS \_ X25Type**</span><span class="sxs-lookup"><span data-stu-id="92b0c-132">**MicrosoftDNS\_X25Type**</span></span>](microsoftdns-x25type.md)
</dt> <dt>

[<span data-ttu-id="92b0c-133">**Die Methode "kreateinzustancefrompropertydata" der X25Type-Klasse von MicrosoftDNS \_**</span><span class="sxs-lookup"><span data-stu-id="92b0c-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_X25Type Class**</span></span>](microsoftdns-x25type-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="92b0c-134">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="92b0c-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





