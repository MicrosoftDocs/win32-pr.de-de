---
title: AgeAllRecords-Methode der MicrosoftDNS_Zone-Klasse
description: Die AgeAllRecords-Methode ermöglicht die Alterung einiger oder aller nicht-NS-und nicht-SOA-Datensätze in einer Zone.
ms.assetid: 0e0df1ab-6c7c-4bc4-b292-8f89095970eb
keywords:
- AgeAllRecords-Methode (DNS)
- AgeAllRecords-Methode, DNS, MicrosoftDNS_Zone-Klasse
- MicrosoftDNS_Zone-Klasse DNS, AgeAllRecords-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.AgeAllRecords
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c70a1435f96091070b2aee4ed7f079e5a6529a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478477"
---
# <a name="ageallrecords-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="ea20e-106">AgeAllRecords-Methode der MicrosoftDNS- \_ Zonen Klasse</span><span class="sxs-lookup"><span data-stu-id="ea20e-106">AgeAllRecords method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="ea20e-107">Die **AgeAllRecords** -Methode ermöglicht die Alterung einiger oder aller nicht-NS-und nicht-SOA-Datensätze in einer Zone.</span><span class="sxs-lookup"><span data-stu-id="ea20e-107">The **AgeAllRecords** method enables aging for some or all non-NS and non-SOA records in a zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea20e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea20e-108">Syntax</span></span>


```mof
uint32 AgeAllRecords(
  [in, optional] string  NodeName,
  [in, optional] boolean ApplyToSubtree
);
```



## <a name="parameters"></a><span data-ttu-id="ea20e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea20e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea20e-110">*NodeName* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ea20e-110">*NodeName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ea20e-111">Der Name des zu Age enden Knotens.</span><span class="sxs-lookup"><span data-stu-id="ea20e-111">Name of the node to age.</span></span>

</dd> <dt>

<span data-ttu-id="ea20e-112">*ApplyTo subtree* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ea20e-112">*ApplyToSubtree* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ea20e-113">Gibt an, ob die Alterung auf alle Datensätze in der Teilstruktur angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea20e-113">Specifies whether aging should apply to all records in the subtree.</span></span> <span data-ttu-id="ea20e-114">Legen Sie diese Einstellung auf true fest, um das Aging auf alle Datensätze in der Teilstruktur anzuwenden, beginnend mit nodename.</span><span class="sxs-lookup"><span data-stu-id="ea20e-114">Set to TRUE to apply aging to all records in the subtree, beginning with NodeName.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea20e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea20e-115">Return value</span></span>

<span data-ttu-id="ea20e-116">Fehler \_ Erfolg gibt an, dass die Alterung erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="ea20e-116">ERROR\_SUCCESS indicates the aging was successfully completed.</span></span> <span data-ttu-id="ea20e-117">Jeder andere Wert ist ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="ea20e-117">Any other value is an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea20e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea20e-118">Remarks</span></span>

<span data-ttu-id="ea20e-119">Wenn *NodeName* nicht angegeben wird, unterliegen alle Datensätze der Alterung und der Löschung.</span><span class="sxs-lookup"><span data-stu-id="ea20e-119">If *NodeName* is not specified, all records will be subject to aging and scavenging.</span></span>

<span data-ttu-id="ea20e-120">Wenn *NodeName* angegeben wird und *applytsubtree* nicht angegeben oder auf 0 (null) festgelegt ist, werden die Datensätze an dem angegebenen Knoten in den Alterungs-und absteigenden Knoten unterteilt.</span><span class="sxs-lookup"><span data-stu-id="ea20e-120">If *NodeName* is specified and *ApplyToSubtree* is not specified or set to zero, records at the specified node will be subjected to aging and scavenging.</span></span>

<span data-ttu-id="ea20e-121">Wenn *NodeName* angegeben wird und *ApplyTo Teilstruktur* auf 1 festgelegt ist, werden alle Datensätze der Teilstruktur, beginnend bei *NodeName* , in den Alterungs-und absteigenden Datensätze unterteilt.</span><span class="sxs-lookup"><span data-stu-id="ea20e-121">If *NodeName* is specified and *ApplyToSubtree* is set to 1, all records of the subtree starting at *NodeName* will be subjected to aging and scavenging.</span></span> <span data-ttu-id="ea20e-122">Der Zeitstempel wird auf die aktuelle Zeit für alle nicht-NS-und nicht-SOA-RRS mit den von den Eingabe Parametern identifizierten Besitzer Namen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ea20e-122">The time stamp is set to the current time for all non-NS and non-SOA RRs with the owner name(s) identified by the input parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea20e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea20e-123">Requirements</span></span>



| <span data-ttu-id="ea20e-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea20e-124">Requirement</span></span> | <span data-ttu-id="ea20e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="ea20e-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea20e-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea20e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ea20e-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ea20e-127">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ea20e-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea20e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ea20e-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea20e-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ea20e-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="ea20e-130">Namespace</span></span><br/>                | <span data-ttu-id="ea20e-131">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="ea20e-131">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="ea20e-132">MOF</span><span class="sxs-lookup"><span data-stu-id="ea20e-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea20e-133"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ea20e-133"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea20e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea20e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea20e-135">**MicrosoftDNS- \_ Zone**</span><span class="sxs-lookup"><span data-stu-id="ea20e-135">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="ea20e-136">**Changezonetype-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="ea20e-136">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="ea20e-137">**Die Methode "kreatezone" der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="ea20e-137">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="ea20e-138">**ForceRefresh-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="ea20e-138">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="ea20e-139">**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="ea20e-139">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="ea20e-140">**Pauzzone-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="ea20e-140">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="ea20e-141">**Reloadzone-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="ea20e-141">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="ea20e-142">**Resetsecon-Replikats-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="ea20e-142">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="ea20e-143">**Resumezone-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="ea20e-143">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="ea20e-144">**Updatefromds-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="ea20e-144">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="ea20e-145">**"Write Backzone"-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="ea20e-145">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





