---
title: Modify-Methode der MicrosoftDNS_MGType-Klasse
description: Die Modify-Methode aktualisiert einen e-Mail-Gruppen Ressourcen-Datensatz (mg).
ms.assetid: c7d42964-19fb-410d-a434-85af20754e20
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_MGType-Klasse
- DNS-MicrosoftDNS_MGType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 706502569687a3c035c943e0a9dcc04aa1732492
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104738"
---
# <a name="modify-method-of-the-microsoftdns_mgtype-class"></a><span data-ttu-id="5050c-106">Modify-Methode der MicrosoftDNS- \_ mgtype-Klasse</span><span class="sxs-lookup"><span data-stu-id="5050c-106">Modify method of the MicrosoftDNS\_MGType class</span></span>

<span data-ttu-id="5050c-107">Die **Modify** -Methode aktualisiert einen e-Mail-Gruppen Ressourcen-Datensatz (mg).</span><span class="sxs-lookup"><span data-stu-id="5050c-107">The **Modify** method updates a Mail Group (MG) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="5050c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5050c-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MGMailbox,
  [out, ref]     MicrosoftDNS_MGType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="5050c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5050c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5050c-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="5050c-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5050c-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="5050c-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="5050c-112">*Mgmailbox* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="5050c-112">*MGMailbox* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5050c-113">FQDN, der ein Postfach angibt, das Mitglied der durch den Besitzer Namen des Datensatzes angegebenen e-Mail-Gruppe ist.</span><span class="sxs-lookup"><span data-stu-id="5050c-113">FQDN specifying a mailbox that is a member of the mail group specified by the record's owner name.</span></span>

</dd> <dt>

<span data-ttu-id="5050c-114">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="5050c-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="5050c-115">Verweis auf das geänderte Objekt.</span><span class="sxs-lookup"><span data-stu-id="5050c-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5050c-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5050c-116">Return value</span></span>

<span data-ttu-id="5050c-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5050c-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5050c-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5050c-118">Remarks</span></span>

<span data-ttu-id="5050c-119">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="5050c-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="5050c-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5050c-120">Requirements</span></span>



| <span data-ttu-id="5050c-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5050c-121">Requirement</span></span> | <span data-ttu-id="5050c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="5050c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5050c-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5050c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5050c-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5050c-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="5050c-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5050c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5050c-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5050c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5050c-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="5050c-127">Namespace</span></span><br/>                | <span data-ttu-id="5050c-128">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="5050c-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="5050c-129">MOF</span><span class="sxs-lookup"><span data-stu-id="5050c-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5050c-130"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5050c-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5050c-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5050c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5050c-132">**MicrosoftDNS- \_ mgtype**</span><span class="sxs-lookup"><span data-stu-id="5050c-132">**MicrosoftDNS\_MGType**</span></span>](microsoftdns-mgtype.md)
</dt> <dt>

[<span data-ttu-id="5050c-133">**Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ mgtype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5050c-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MGType Class**</span></span>](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="5050c-134">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="5050c-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





