---
title: Modify-Methode der MicrosoftDNS_RPType-Klasse
description: Die Modify-Methode aktualisiert einen Ressourcen Daten Satz für Verantwortliche Personen (RP).
ms.assetid: a779b905-922c-42ff-b3d9-318b3a848230
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_RPType-Klasse
- DNS-MicrosoftDNS_RPType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ec575424e6e26c79f8d6a27e62732cad6ddc57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858991"
---
# <a name="modify-method-of-the-microsoftdns_rptype-class"></a><span data-ttu-id="48b00-106">Modify-Methode der MicrosoftDNS- \_ rptype-Klasse</span><span class="sxs-lookup"><span data-stu-id="48b00-106">Modify method of the MicrosoftDNS\_RPType class</span></span>

<span data-ttu-id="48b00-107">Die **Modify** -Methode aktualisiert einen Ressourcen Daten Satz für Verantwortliche Personen (RP).</span><span class="sxs-lookup"><span data-stu-id="48b00-107">The **Modify** method updates a Responsible Person (RP) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="48b00-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="48b00-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              RPMailbox,
  [in, optional] string              TXTDomainName,
  [out, ref]     MicrosoftDNS_RPType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="48b00-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="48b00-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48b00-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="48b00-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="48b00-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="48b00-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="48b00-112">*Rpmailbox* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="48b00-112">*RPMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="48b00-113">Vollständiger vollständiger vollständiger Name des Postfachs.</span><span class="sxs-lookup"><span data-stu-id="48b00-113">FQDN specifying the mailbox for the responsible person.</span></span>

</dd> <dt>

<span data-ttu-id="48b00-114">*TxtDomainName* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="48b00-114">*TXTDomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="48b00-115">Der voll qualifizierte Daten Satz, für den txt-Ressourcen Einträge vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="48b00-115">FQDN for which TXT Resource Records exist.</span></span>

</dd> <dt>

<span data-ttu-id="48b00-116">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="48b00-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="48b00-117">Verweis auf das geänderte Objekt.</span><span class="sxs-lookup"><span data-stu-id="48b00-117">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48b00-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48b00-118">Return value</span></span>

<span data-ttu-id="48b00-119">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="48b00-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="48b00-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48b00-120">Remarks</span></span>

<span data-ttu-id="48b00-121">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="48b00-121">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="48b00-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48b00-122">Requirements</span></span>



| <span data-ttu-id="48b00-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48b00-123">Requirement</span></span> | <span data-ttu-id="48b00-124">Wert</span><span class="sxs-lookup"><span data-stu-id="48b00-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="48b00-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48b00-125">Minimum supported client</span></span><br/> | <span data-ttu-id="48b00-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="48b00-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="48b00-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48b00-127">Minimum supported server</span></span><br/> | <span data-ttu-id="48b00-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48b00-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="48b00-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="48b00-129">Namespace</span></span><br/>                | <span data-ttu-id="48b00-130">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="48b00-130">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="48b00-131">MOF</span><span class="sxs-lookup"><span data-stu-id="48b00-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48b00-132"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="48b00-132"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48b00-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48b00-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48b00-134">**MicrosoftDNS- \_ rptype**</span><span class="sxs-lookup"><span data-stu-id="48b00-134">**MicrosoftDNS\_RPType**</span></span>](microsoftdns-rptype.md)
</dt> <dt>

[<span data-ttu-id="48b00-135">**Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ rptype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="48b00-135">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_RPType Class**</span></span>](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="48b00-136">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="48b00-136">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





