---
title: Modify-Methode der MicrosoftDNS_MBType-Klasse
description: Die Modify-Methode aktualisiert einen Post Fach Ressourcen Daten Satz (MB).
ms.assetid: ee76031c-ac1b-4ebb-9fb2-3b64553867cc
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_MBType-Klasse
- DNS-MicrosoftDNS_MBType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 135d6f0fcb0faf5c1e8da152798863c8cecc8641
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741992"
---
# <a name="modify-method-of-the-microsoftdns_mbtype-class"></a><span data-ttu-id="fb8fd-106">Modify-Methode der MicrosoftDNS- \_ Klasse von mbtype</span><span class="sxs-lookup"><span data-stu-id="fb8fd-106">Modify method of the MicrosoftDNS\_MBType class</span></span>

<span data-ttu-id="fb8fd-107">Die **Modify** -Methode aktualisiert einen Post Fach Ressourcen Daten Satz (MB).</span><span class="sxs-lookup"><span data-stu-id="fb8fd-107">The **Modify** method updates a Mailbox (MB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb8fd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb8fd-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in]           string              MBHost,
  [out, ref]     MicrosoftDNS_MBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="fb8fd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb8fd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb8fd-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="fb8fd-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fb8fd-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="fb8fd-112">*Mbhost* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb8fd-112">*MBHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb8fd-113">Zeichenfolge, die den Post Fach Hostnamen für den MB-Datensatz darstellt.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-113">String representing the mailbox host name for the MB record.</span></span>

</dd> <dt>

<span data-ttu-id="fb8fd-114">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="fb8fd-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="fb8fd-115">Verweis auf das geänderte Objekt.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb8fd-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb8fd-116">Return value</span></span>

<span data-ttu-id="fb8fd-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb8fd-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb8fd-118">Remarks</span></span>

<span data-ttu-id="fb8fd-119">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="fb8fd-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb8fd-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb8fd-120">Requirements</span></span>



| <span data-ttu-id="fb8fd-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb8fd-121">Requirement</span></span> | <span data-ttu-id="fb8fd-122">Wert</span><span class="sxs-lookup"><span data-stu-id="fb8fd-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb8fd-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb8fd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fb8fd-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fb8fd-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="fb8fd-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb8fd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fb8fd-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb8fd-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fb8fd-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="fb8fd-127">Namespace</span></span><br/>                | <span data-ttu-id="fb8fd-128">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="fb8fd-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="fb8fd-129">MOF</span><span class="sxs-lookup"><span data-stu-id="fb8fd-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb8fd-130"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fb8fd-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb8fd-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb8fd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb8fd-132">**MicrosoftDNS \_ mbtype**</span><span class="sxs-lookup"><span data-stu-id="fb8fd-132">**MicrosoftDNS\_MBType**</span></span>](microsoftdns-mbtype.md)
</dt> <dt>

[<span data-ttu-id="fb8fd-133">**Die Methode "kreateinstancefrompropertydata" der Klasse "MicrosoftDNS \_ mbtype"**</span><span class="sxs-lookup"><span data-stu-id="fb8fd-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MBType Class**</span></span>](microsoftdns-mbtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="fb8fd-134">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="fb8fd-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





