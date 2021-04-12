---
title: Modify-Methode der MicrosoftDNS_MDType-Klasse
description: Die Modify-Methode aktualisiert einen Mail-Agent für die Domäne (MD)-Ressourcen Daten Satz.
ms.assetid: d14c8ada-d715-489f-9956-a940b94006e5
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_MDType-Klasse
- DNS-MicrosoftDNS_MDType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ed5e3a8d7f819447d256ba3bce31f4eaa6986a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103610"
---
# <a name="modify-method-of-the-microsoftdns_mdtype-class"></a><span data-ttu-id="9772f-106">Modify-Methode der MicrosoftDNS- \_ mdtype-Klasse</span><span class="sxs-lookup"><span data-stu-id="9772f-106">Modify method of the MicrosoftDNS\_MDType class</span></span>

<span data-ttu-id="9772f-107">Die **Modify** -Methode aktualisiert einen Mail-Agent für die Domäne (MD)-Ressourcen Daten Satz.</span><span class="sxs-lookup"><span data-stu-id="9772f-107">The **Modify** method updates a Mail Agent for Domain (MD) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="9772f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9772f-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MDHost,
  [out, ref]     MicrosoftDNS_MDType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="9772f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9772f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9772f-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="9772f-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9772f-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="9772f-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="9772f-112">*Mdhost* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="9772f-112">*MDHost* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9772f-113">Zeichenfolge, die den Mail Übermittlungs Host darstellt.</span><span class="sxs-lookup"><span data-stu-id="9772f-113">String representing the mail delivery host.</span></span>

</dd> <dt>

<span data-ttu-id="9772f-114">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="9772f-114">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="9772f-115">Verweis auf das geänderte Objekt.</span><span class="sxs-lookup"><span data-stu-id="9772f-115">Reference to the modified object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9772f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9772f-116">Return value</span></span>

<span data-ttu-id="9772f-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9772f-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9772f-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9772f-118">Remarks</span></span>

<span data-ttu-id="9772f-119">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="9772f-119">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="9772f-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9772f-120">Requirements</span></span>



| <span data-ttu-id="9772f-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9772f-121">Requirement</span></span> | <span data-ttu-id="9772f-122">Wert</span><span class="sxs-lookup"><span data-stu-id="9772f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9772f-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9772f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9772f-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9772f-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9772f-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9772f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9772f-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9772f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9772f-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="9772f-127">Namespace</span></span><br/>                | <span data-ttu-id="9772f-128">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="9772f-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="9772f-129">MOF</span><span class="sxs-lookup"><span data-stu-id="9772f-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9772f-130"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9772f-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9772f-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9772f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9772f-132">**MicrosoftDNS- \_ mdtype**</span><span class="sxs-lookup"><span data-stu-id="9772f-132">**MicrosoftDNS\_MDType**</span></span>](microsoftdns-mdtype.md)
</dt> <dt>

[<span data-ttu-id="9772f-133">**Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ mdtype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9772f-133">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_MDType Class**</span></span>](microsoftdns-mdtype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="9772f-134">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="9772f-134">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





