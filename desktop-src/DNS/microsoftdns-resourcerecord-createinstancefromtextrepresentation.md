---
title: Methode "kreateinzustancefromtextrepresentation" der MicrosoftDNS_ResourceRecord-Klasse
description: Die Methode "kreateinstancefromtextrepresentation" instanziiert ein MicrosoftDNS \_ resourcerecord-Objekt.
ms.assetid: 19600a9a-f75d-40ad-98e5-f81465d10f79
keywords:
- Methode "samateinzustancefromtextrepresentation" (DNS)
- Methode "-DNS", "MicrosoftDNS_ResourceRecord"-Klasse
- DNS-MicrosoftDNS_ResourceRecord Klasse, Methode "kreateinzustancefromtextrepresentation"
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a578d036180ecb1dc8a5e66bf853eec8845583f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040717"
---
# <a name="createinstancefromtextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a><span data-ttu-id="df170-106">Methode "kreateinzustancefromtextrepresentation" der MicrosoftDNS \_ resourcerecord-Klasse</span><span class="sxs-lookup"><span data-stu-id="df170-106">CreateInstanceFromTextRepresentation method of the MicrosoftDNS\_ResourceRecord class</span></span>

<span data-ttu-id="df170-107">Die Methode " **kreateinstancefromtextrepresentation** " instanziiert ein [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="df170-107">The **CreateInstanceFromTextRepresentation** method instantiates a [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="df170-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="df170-108">Syntax</span></span>


```mof
void CreateInstanceFromTextRepresentation(
  [in]       string                      DnsServerName,
  [in]       string                      ContainerName,
  [in]       string                      TextRepresentation,
  [out, ref] MicrosoftDNS_ResourceRecord &RR
);
```



## <a name="parameters"></a><span data-ttu-id="df170-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="df170-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df170-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df170-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df170-111">Der Name des DNS-Servers, auf dem die RR-Datei erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="df170-111">Name of the DNS Server on which the RR should be created.</span></span>

</dd> <dt>

<span data-ttu-id="df170-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df170-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df170-113">Der Name des Containers, in den das neue RR eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="df170-113">Name of the container into which the new RR should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="df170-114">*Textrepresentation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df170-114">*TextRepresentation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df170-115">Text Darstellung der zu erstellenden RR-Instanz.</span><span class="sxs-lookup"><span data-stu-id="df170-115">Text representation of the RR instance to be created.</span></span>

</dd> <dt>

<span data-ttu-id="df170-116">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="df170-116">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="df170-117">Verweis auf den instanziierten RR.</span><span class="sxs-lookup"><span data-stu-id="df170-117">Reference to the instantiated RR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df170-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df170-118">Return value</span></span>

<span data-ttu-id="df170-119">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="df170-119">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="df170-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df170-120">Requirements</span></span>



| <span data-ttu-id="df170-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df170-121">Requirement</span></span> | <span data-ttu-id="df170-122">Wert</span><span class="sxs-lookup"><span data-stu-id="df170-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df170-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="df170-123">Minimum supported client</span></span><br/> | <span data-ttu-id="df170-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="df170-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="df170-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="df170-125">Minimum supported server</span></span><br/> | <span data-ttu-id="df170-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df170-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="df170-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="df170-127">Namespace</span></span><br/>                | <span data-ttu-id="df170-128">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="df170-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="df170-129">MOF</span><span class="sxs-lookup"><span data-stu-id="df170-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df170-130"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="df170-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df170-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df170-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df170-132">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="df170-132">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="df170-133">**Getobjectbytextrepresentation-Methode der MicrosoftDNS \_ resourcerecord-Klasse**</span><span class="sxs-lookup"><span data-stu-id="df170-133">**GetObjectByTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





