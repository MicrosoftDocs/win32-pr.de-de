---
title: Modify-Methode der MicrosoftDNS_WKSType-Klasse
description: Die Modify-Methode aktualisiert einen Well-Known Services (WKT)-Ressourcen Daten Satz.
ms.assetid: 3a9100eb-dc90-45bb-9739-14026da100fd
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_WKSType-Klasse
- DNS-MicrosoftDNS_WKSType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30f7cf58a231d93288a3cdc170fa857bb12687af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859038"
---
# <a name="modify-method-of-the-microsoftdns_wkstype-class"></a><span data-ttu-id="13d47-106">Modify-Methode der MicrosoftDNS- \_ Klasse "wkstype"</span><span class="sxs-lookup"><span data-stu-id="13d47-106">Modify method of the MicrosoftDNS\_WKSType class</span></span>

<span data-ttu-id="13d47-107">Die **Modify** -Methode aktualisiert einen Well-Known Services (WKT)-Ressourcen Daten Satz.</span><span class="sxs-lookup"><span data-stu-id="13d47-107">The **Modify** method updates a Well-Known Services (WKS) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="13d47-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="13d47-108">Syntax</span></span>


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               InternetAddress,
  [in, optional] uint8                IPProtocol,
  [in, optional] uint8                Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="13d47-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="13d47-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13d47-110">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="13d47-110">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="13d47-111">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="13d47-111">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="13d47-112">*Internetadresse* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="13d47-112">*InternetAddress* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="13d47-113">Internet-IP-Adresse für den Besitzer des Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="13d47-113">Internet IP address for the record's owner.</span></span>

</dd> <dt>

<span data-ttu-id="13d47-114">*Ipprotocol* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="13d47-114">*IPProtocol* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="13d47-115">Zeichenfolge, die das IP-Protokoll für diesen Datensatz darstellt.</span><span class="sxs-lookup"><span data-stu-id="13d47-115">String representing the IP protocol for this record.</span></span> <span data-ttu-id="13d47-116">Gültige Werte sind UDP oder TCP.</span><span class="sxs-lookup"><span data-stu-id="13d47-116">Valid values are UDP or TCP.</span></span>

</dd> <dt>

<span data-ttu-id="13d47-117">*Dienste* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="13d47-117">*Services* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="13d47-118">Eine Zeichenfolge, die alle Dienste enthält, die vom Wi-Datensatz (well known Service) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13d47-118">String containing all services used by the Well Known Service (WKS) record.</span></span>

</dd> <dt>

<span data-ttu-id="13d47-119">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="13d47-119">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="13d47-120">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="13d47-120">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13d47-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13d47-121">Return value</span></span>

<span data-ttu-id="13d47-122">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="13d47-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="13d47-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13d47-123">Remarks</span></span>

<span data-ttu-id="13d47-124">Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.</span><span class="sxs-lookup"><span data-stu-id="13d47-124">Any parameter not specified is left unchanged in the modified record.</span></span>

## <a name="requirements"></a><span data-ttu-id="13d47-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13d47-125">Requirements</span></span>



| <span data-ttu-id="13d47-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13d47-126">Requirement</span></span> | <span data-ttu-id="13d47-127">Wert</span><span class="sxs-lookup"><span data-stu-id="13d47-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13d47-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13d47-128">Minimum supported client</span></span><br/> | <span data-ttu-id="13d47-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="13d47-129">None supported</span></span><br/>                                                              |
| <span data-ttu-id="13d47-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13d47-130">Minimum supported server</span></span><br/> | <span data-ttu-id="13d47-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13d47-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="13d47-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="13d47-132">Namespace</span></span><br/>                | <span data-ttu-id="13d47-133">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="13d47-133">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="13d47-134">MOF</span><span class="sxs-lookup"><span data-stu-id="13d47-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13d47-135"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="13d47-135"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13d47-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13d47-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13d47-137">**MicrosoftDNS \_ wkstype**</span><span class="sxs-lookup"><span data-stu-id="13d47-137">**MicrosoftDNS\_WKSType**</span></span>](microsoftdns-wkstype.md)
</dt> <dt>

[<span data-ttu-id="13d47-138">**Methode "kreateinzustancefrompropertydata" der MicrosoftDNS- \_ Klasse "wkstype"**</span><span class="sxs-lookup"><span data-stu-id="13d47-138">**CreateInstanceFromPropertyData Method of the MicrosoftDNS\_WKSType Class**</span></span>](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[<span data-ttu-id="13d47-139">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="13d47-139">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





