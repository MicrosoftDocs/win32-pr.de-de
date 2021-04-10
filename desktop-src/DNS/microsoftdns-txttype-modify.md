---
title: Modify-Methode der MicrosoftDNS_TXTType-Klasse
description: Die Modify-Methode aktualisiert einen Text (txt)-Ressourcen Daten Satz.
ms.assetid: af61057e-95be-4290-83da-a63f01ead476
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_TXTType-Klasse
- DNS-MicrosoftDNS_TXTType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 285dfb6d5323ca3775f981aecbf5a0170392cd3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103054"
---
# <a name="modify-method-of-the-microsoftdns_txttype-class"></a><span data-ttu-id="4a384-106">Modify-Methode der MicrosoftDNS \_ txttype-Klasse</span><span class="sxs-lookup"><span data-stu-id="4a384-106">Modify method of the MicrosoftDNS\_TXTType class</span></span>

<span data-ttu-id="4a384-107">Die **Modify** -Methode aktualisiert einen Text (txt)-Ressourcen Daten Satz.</span><span class="sxs-lookup"><span data-stu-id="4a384-107">The **Modify** method updates a Text (TXT) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a384-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a384-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               DescriptiveText,
  [out, ref]     MicrosoftDNS_TXTType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="4a384-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a384-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a384-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="4a384-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4a384-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4a384-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="4a384-112">*Deskriptivetext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a384-112">*DescriptiveText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a384-113">Beschreibender Text, die Semantik, von der abhängig von der Besitzer Domäne ist.</span><span class="sxs-lookup"><span data-stu-id="4a384-113">Descriptive text, the semantics of which depend on the owner domain.</span></span>

</dd> <dt>

<span data-ttu-id="4a384-114">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="4a384-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="4a384-115">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4a384-115">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a384-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a384-116">Return value</span></span>

<span data-ttu-id="4a384-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4a384-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a384-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a384-118">Remarks</span></span>

<span data-ttu-id="4a384-119">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="4a384-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a384-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a384-120">Requirements</span></span>



| <span data-ttu-id="4a384-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a384-121">Requirement</span></span> | <span data-ttu-id="4a384-122">Wert</span><span class="sxs-lookup"><span data-stu-id="4a384-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a384-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4a384-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4a384-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4a384-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4a384-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4a384-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4a384-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a384-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4a384-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="4a384-127">Namespace</span></span><br/>                | <span data-ttu-id="4a384-128">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="4a384-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="4a384-129">MOF</span><span class="sxs-lookup"><span data-stu-id="4a384-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a384-130"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4a384-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a384-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a384-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a384-132">**MicrosoftDNS- \_ txttype**</span><span class="sxs-lookup"><span data-stu-id="4a384-132">**MicrosoftDNS\_TXTType**</span></span>](microsoftdns-txttype.md)
</dt> <dt>

[<span data-ttu-id="4a384-133">**Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS- \_ Klasse "txttype"**</span><span class="sxs-lookup"><span data-stu-id="4a384-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_TXTType Class**</span></span>](microsoftdns-txttype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="4a384-134">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="4a384-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





