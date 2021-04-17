---
title: Modify-Methode der MicrosoftDNS_MRType-Klasse
description: Die Modify-Methode aktualisiert einen Ressourcen Daten Satz für Post Fach Umbenennungen (Mr).
ms.assetid: eb833735-d485-4603-9976-305244537acd
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_MRType-Klasse
- DNS-MicrosoftDNS_MRType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 996692301e8446b3fd67e20eca036cd085e83b03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476593"
---
# <a name="modify-method-of-the-microsoftdns_mrtype-class"></a><span data-ttu-id="00cd0-106">Modify-Methode der MicrosoftDNS- \_ mrtype-Klasse</span><span class="sxs-lookup"><span data-stu-id="00cd0-106">Modify method of the MicrosoftDNS\_MRType class</span></span>

<span data-ttu-id="00cd0-107">Die **Modify** -Methode aktualisiert einen Ressourcen Daten Satz für Post Fach Umbenennungen (Mr).</span><span class="sxs-lookup"><span data-stu-id="00cd0-107">The **Modify** method updates a Mailbox Rename (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="00cd0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="00cd0-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in]           string              MRMailbox,
  [out, ref]     MicrosoftDNS_MRType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="00cd0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="00cd0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00cd0-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="00cd0-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="00cd0-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="00cd0-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="00cd0-112">*Mrmailbox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00cd0-112">*MRMailbox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00cd0-113">Der voll qualifizierte Name des Postfachs, bei dem es sich um den ordnungsgemäßen Umbenennen des im Namen des Datensatzes angegebenen Postfachs handelt</span><span class="sxs-lookup"><span data-stu-id="00cd0-113">FQDN specifying a mailbox that is the proper rename of the mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="00cd0-114">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="00cd0-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="00cd0-115">Verweis auf das geänderte Objekt.</span><span class="sxs-lookup"><span data-stu-id="00cd0-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00cd0-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00cd0-116">Return value</span></span>

<span data-ttu-id="00cd0-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="00cd0-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="00cd0-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00cd0-118">Remarks</span></span>

<span data-ttu-id="00cd0-119">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="00cd0-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="00cd0-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00cd0-120">Requirements</span></span>



| <span data-ttu-id="00cd0-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00cd0-121">Requirement</span></span> | <span data-ttu-id="00cd0-122">Wert</span><span class="sxs-lookup"><span data-stu-id="00cd0-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00cd0-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00cd0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="00cd0-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="00cd0-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="00cd0-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00cd0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="00cd0-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00cd0-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="00cd0-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="00cd0-127">Namespace</span></span><br/>                | <span data-ttu-id="00cd0-128">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="00cd0-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="00cd0-129">MOF</span><span class="sxs-lookup"><span data-stu-id="00cd0-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00cd0-130"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="00cd0-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00cd0-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00cd0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00cd0-132">**MicrosoftDNS- \_ mrtype**</span><span class="sxs-lookup"><span data-stu-id="00cd0-132">**MicrosoftDNS\_MRType**</span></span>](microsoftdns-mrtype.md)
</dt> <dt>

[<span data-ttu-id="00cd0-133">**Methode "kreateinstancefrompropertydata" der Klasse "MicrosoftDNS \_ mrtype"**</span><span class="sxs-lookup"><span data-stu-id="00cd0-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MRType Class**</span></span>](microsoftdns-mrtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="00cd0-134">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="00cd0-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





