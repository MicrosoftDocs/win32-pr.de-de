---
title: Modify-Methode der MicrosoftDNS_MXType-Klasse
description: Die Modify-Methode aktualisiert einen e-Mail-Austausch Ressourcen Daten Satz (Mr).
ms.assetid: 40267ac9-0392-4e08-a5d2-145ee9639c39
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_MXType-Klasse
- DNS-MicrosoftDNS_MXType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a665d0673e048eff684b4c985b54a1c57e030a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957143"
---
# <a name="modify-method-of-the-microsoftdns_mxtype-class"></a><span data-ttu-id="36e81-106">Modify-Methode der MicrosoftDNS- \_ mxtype-Klasse</span><span class="sxs-lookup"><span data-stu-id="36e81-106">Modify method of the MicrosoftDNS\_MXType class</span></span>

<span data-ttu-id="36e81-107">Die **Modify** -Methode aktualisiert einen e-Mail-Austausch Ressourcen Daten Satz (Mr).</span><span class="sxs-lookup"><span data-stu-id="36e81-107">The **Modify** method updates a Mail Exchanger (MR) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="36e81-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="36e81-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              MailExchange,
  [out, ref]     MicrosoftDNS_MXType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="36e81-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="36e81-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36e81-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="36e81-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="36e81-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="36e81-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="36e81-112">*Bevorzugen* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="36e81-112">*Preference* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="36e81-113">Die Einstellung, die diesem RR unter anderem beim gleichen Besitzer zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="36e81-113">Preference given to this RR among others at the same owner.</span></span> <span data-ttu-id="36e81-114">Niedrigere Werte werden bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="36e81-114">Lower values are preferred.</span></span>

</dd> <dt>

<span data-ttu-id="36e81-115">*Mailexchange* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="36e81-115">*MailExchange* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="36e81-116">FQDN, der einen Host angibt, der als e-Mail-Austausch für den Namen des Besitzers fungieren soll.</span><span class="sxs-lookup"><span data-stu-id="36e81-116">FQDN specifying a host willing to act as a mail exchange for the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="36e81-117">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="36e81-117">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="36e81-118">Verweis auf das geänderte Objekt.</span><span class="sxs-lookup"><span data-stu-id="36e81-118">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36e81-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="36e81-119">Return value</span></span>

<span data-ttu-id="36e81-120">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="36e81-120">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="36e81-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36e81-121">Remarks</span></span>

<span data-ttu-id="36e81-122">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="36e81-122">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="36e81-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36e81-123">Requirements</span></span>



| <span data-ttu-id="36e81-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36e81-124">Requirement</span></span> | <span data-ttu-id="36e81-125">Wert</span><span class="sxs-lookup"><span data-stu-id="36e81-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36e81-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36e81-126">Minimum supported client</span></span><br/> | <span data-ttu-id="36e81-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="36e81-127">None supported</span></span><br/>                                                              |
| <span data-ttu-id="36e81-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36e81-128">Minimum supported server</span></span><br/> | <span data-ttu-id="36e81-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36e81-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="36e81-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="36e81-130">Namespace</span></span><br/>                | <span data-ttu-id="36e81-131">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="36e81-131">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="36e81-132">MOF</span><span class="sxs-lookup"><span data-stu-id="36e81-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36e81-133"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="36e81-133"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36e81-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36e81-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36e81-135">**MicrosoftDNS- \_ mxtype**</span><span class="sxs-lookup"><span data-stu-id="36e81-135">**MicrosoftDNS\_MXType**</span></span>](microsoftdns-mxtype.md)
</dt> <dt>

[<span data-ttu-id="36e81-136">**Die Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ mxtype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="36e81-136">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MXType Class**</span></span>](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="36e81-137">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="36e81-137">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





