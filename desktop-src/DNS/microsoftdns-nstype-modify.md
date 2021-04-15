---
title: Modify-Methode der MicrosoftDNS_NSType-Klasse
description: Die Modify-Methode aktualisiert einen Name Server (NS)-Ressourcen Daten Satz.
ms.assetid: da625231-cf4e-4526-b713-737e6b9f5831
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_NSType-Klasse
- DNS-MicrosoftDNS_NSType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_NSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3dd26b7c0f1c31ef3ea742f20f70df8646a087b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479401"
---
# <a name="modify-method-of-the-microsoftdns_nstype-class"></a><span data-ttu-id="69b0b-106">Modify-Methode der MicrosoftDNS- \_ nstype-Klasse</span><span class="sxs-lookup"><span data-stu-id="69b0b-106">Modify method of the MicrosoftDNS\_NSType class</span></span>

<span data-ttu-id="69b0b-107">Die **Modify** -Methode aktualisiert einen Name Server (NS)-Ressourcen Daten Satz.</span><span class="sxs-lookup"><span data-stu-id="69b0b-107">The **Modify** method updates a Name Server (NS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="69b0b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="69b0b-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              NSHost,
  [out, ref]     MicrosoftDNS_NSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="69b0b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="69b0b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69b0b-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="69b0b-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="69b0b-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="69b0b-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="69b0b-112">*NSHost* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="69b0b-112">*NSHost* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="69b0b-113">Autorisierender Host für die Domäne.</span><span class="sxs-lookup"><span data-stu-id="69b0b-113">Authoritative host for the domain.</span></span>

</dd> <dt>

<span data-ttu-id="69b0b-114">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="69b0b-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="69b0b-115">Verweis auf das geänderte Objekt.</span><span class="sxs-lookup"><span data-stu-id="69b0b-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69b0b-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="69b0b-116">Return value</span></span>

<span data-ttu-id="69b0b-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="69b0b-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="69b0b-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69b0b-118">Remarks</span></span>

<span data-ttu-id="69b0b-119">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="69b0b-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="69b0b-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69b0b-120">Requirements</span></span>



| <span data-ttu-id="69b0b-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69b0b-121">Requirement</span></span> | <span data-ttu-id="69b0b-122">Wert</span><span class="sxs-lookup"><span data-stu-id="69b0b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69b0b-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69b0b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="69b0b-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="69b0b-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="69b0b-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69b0b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="69b0b-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69b0b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="69b0b-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="69b0b-127">Namespace</span></span><br/>                | <span data-ttu-id="69b0b-128">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="69b0b-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="69b0b-129">MOF</span><span class="sxs-lookup"><span data-stu-id="69b0b-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69b0b-130"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="69b0b-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69b0b-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69b0b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69b0b-132">**MicrosoftDNS \_ ptrtype**</span><span class="sxs-lookup"><span data-stu-id="69b0b-132">**MicrosoftDNS\_PTRType**</span></span>](microsoftdns-ptrtype.md)
</dt> <dt>

[<span data-ttu-id="69b0b-133">**Die Methode "kreateinstancefrompropertydata" der Klasse "MicrosoftDNS \_ ptrtype"**</span><span class="sxs-lookup"><span data-stu-id="69b0b-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_PTRType Class**</span></span>](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="69b0b-134">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="69b0b-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





