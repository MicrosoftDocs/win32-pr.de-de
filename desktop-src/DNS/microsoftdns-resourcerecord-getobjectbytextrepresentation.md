---
title: Getobjectbytextrepresentation-Methode der MicrosoftDNS_ResourceRecord-Klasse
description: Die getobjectbytextrepresentation-Methode ruft eine vorhandene Instanz der MicrosoftDNS \_ resourcerecord-Klasse ab.
ms.assetid: d25e10de-81fa-4220-b2b8-d9a65298b629
keywords:
- Getobjectbytextrepresentation-Methode (DNS)
- Getobjectbytextrepresentation-Methode (DNS), MicrosoftDNS_ResourceRecord-Klasse
- MicrosoftDNS_ResourceRecord-Klasse DNS, getobjectbytextrepresentation-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aea2588a70ff4bdab89eae58b65715152d6c7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477277"
---
# <a name="getobjectbytextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a><span data-ttu-id="c5adb-106">Getobjectbytextrepresentation-Methode der MicrosoftDNS \_ resourcerecord-Klasse</span><span class="sxs-lookup"><span data-stu-id="c5adb-106">GetObjectByTextRepresentation method of the MicrosoftDNS\_ResourceRecord class</span></span>

<span data-ttu-id="c5adb-107">Die **getobjectbytextrepresentation** -Methode ruft eine vorhandene Instanz der [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) -Klasse ab.</span><span class="sxs-lookup"><span data-stu-id="c5adb-107">The **GetObjectByTextRepresentation** method retrieves an existing instance of the [**MicrosoftDNS\_ResourceRecord**](microsoftdns-resourcerecord.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5adb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5adb-108">Syntax</span></span>


```mof
void GetObjectByTextRepresentation(
  [in]  string                      DnsServerName,
  [in]  string                      ContainerName,
  [in]  string                      TextRepresentation,
  [out] MicrosoftDns_ResourceRecord RR
);
```



## <a name="parameters"></a><span data-ttu-id="c5adb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5adb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5adb-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5adb-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5adb-111">Der Name des DNS-Servers, von dem die RR-Datei abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c5adb-111">Name of the DNS Server from which the RR should be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="c5adb-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5adb-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5adb-113">Der Name des Containers, von dem die RR abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c5adb-113">Name of the container from which the RR should be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="c5adb-114">*Textrepresentation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5adb-114">*TextRepresentation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5adb-115">Text Darstellung des zu abzurufenden RR-Werts.</span><span class="sxs-lookup"><span data-stu-id="c5adb-115">Text representation of the RR to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="c5adb-116">*RR* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c5adb-116">*RR* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5adb-117">Verweis auf den instanziierten RR.</span><span class="sxs-lookup"><span data-stu-id="c5adb-117">Reference to the instantiated RR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5adb-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5adb-118">Return value</span></span>

<span data-ttu-id="c5adb-119">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c5adb-119">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5adb-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5adb-120">Requirements</span></span>



| <span data-ttu-id="c5adb-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5adb-121">Requirement</span></span> | <span data-ttu-id="c5adb-122">Wert</span><span class="sxs-lookup"><span data-stu-id="c5adb-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5adb-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5adb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c5adb-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c5adb-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c5adb-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5adb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c5adb-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5adb-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c5adb-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5adb-127">Namespace</span></span><br/>                | <span data-ttu-id="c5adb-128">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="c5adb-128">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="c5adb-129">MOF</span><span class="sxs-lookup"><span data-stu-id="c5adb-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5adb-130"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c5adb-130"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5adb-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5adb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5adb-132">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="c5adb-132">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> <dt>

[<span data-ttu-id="c5adb-133">**Methode "kreateinzustancefromtextrepresentation" der MicrosoftDNS \_ resourcerecord-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c5adb-133">**CreateInstanceFromTextRepresentation Method of the MicrosoftDNS\_ResourceRecord Class**</span></span>](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> </dl>

 

 





