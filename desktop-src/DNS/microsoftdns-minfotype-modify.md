---
title: Modify-Methode der MicrosoftDNS_MINFOType-Klasse
description: Die Modify-Methode aktualisiert einen Ressourcen Daten Satz für e-Mail-Informationen (MINFO).
ms.assetid: fbec0cd3-f735-44c6-b010-80f35cc33d98
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_MINFOType-Klasse
- DNS-MicrosoftDNS_MINFOType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b59d7d1231ed88e61a0ecf94cef50041ca772f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475882"
---
# <a name="modify-method-of-the-microsoftdns_minfotype-class"></a><span data-ttu-id="b8ffd-106">Modify-Methode der MicrosoftDNS- \_ minfotype-Klasse</span><span class="sxs-lookup"><span data-stu-id="b8ffd-106">Modify method of the MicrosoftDNS\_MINFOType class</span></span>

<span data-ttu-id="b8ffd-107">Die **Modify** -Methode aktualisiert einen Ressourcen Daten Satz für e-Mail-Informationen (MINFO).</span><span class="sxs-lookup"><span data-stu-id="b8ffd-107">The **Modify** method updates a Mail Information (MINFO) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8ffd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8ffd-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 ResponsibleMailbox,
  [in, optional] string                 ErrorMailbox,
  [out, ref]     MicrosoftDNS_MINFOType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="b8ffd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8ffd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8ffd-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b8ffd-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b8ffd-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b8ffd-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="b8ffd-112">" *Verantworblemailbox* \[ " in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b8ffd-112">*ResponsibleMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b8ffd-113">Der voll qualifizierte Name ist ein Postfach, das für die Mailingliste oder das Postfach zuständig ist, die im Besitzer Namen des Datensatzes angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="b8ffd-113">FQDN specifying a mailbox responsible for the mailing list or mailbox specified in the record's Owner Name.</span></span>

</dd> <dt>

<span data-ttu-id="b8ffd-114">*Errormailbox* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b8ffd-114">*ErrorMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b8ffd-115">FQDN, der ein Postfach für den Empfang von Fehlermeldungen in Bezug auf die Mailingliste oder das Postfach angibt, das durch den Besitzer Namen des MINFO-Datensatzes angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b8ffd-115">FQDN specifying a mailbox to receive error messages related to either the mailing list, or to the mailbox specified by the owner name of the MINFO record.</span></span>

</dd> <dt>

<span data-ttu-id="b8ffd-116">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="b8ffd-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="b8ffd-117">Verweis auf das geänderte Objekt.</span><span class="sxs-lookup"><span data-stu-id="b8ffd-117">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8ffd-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8ffd-118">Return value</span></span>

<span data-ttu-id="b8ffd-119">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b8ffd-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8ffd-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8ffd-120">Remarks</span></span>

<span data-ttu-id="b8ffd-121">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="b8ffd-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8ffd-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8ffd-122">Requirements</span></span>



| <span data-ttu-id="b8ffd-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8ffd-123">Requirement</span></span> | <span data-ttu-id="b8ffd-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b8ffd-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8ffd-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8ffd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b8ffd-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b8ffd-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b8ffd-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8ffd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b8ffd-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8ffd-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b8ffd-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="b8ffd-129">Namespace</span></span><br/>                | <span data-ttu-id="b8ffd-130">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="b8ffd-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="b8ffd-131">MOF</span><span class="sxs-lookup"><span data-stu-id="b8ffd-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8ffd-132"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b8ffd-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8ffd-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8ffd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8ffd-134">**MicrosoftDNS- \_ minfotype**</span><span class="sxs-lookup"><span data-stu-id="b8ffd-134">**MicrosoftDNS\_MINFOType**</span></span>](microsoftdns-minfotype.md)
</dt> <dt>

[<span data-ttu-id="b8ffd-135">**Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ minfotype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b8ffd-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MINFOType Class**</span></span>](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="b8ffd-136">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="b8ffd-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





