---
title: Resetsecon-Replikats-Methode der MicrosoftDNS_Zone-Klasse
description: Die resetsecon-Methode setzt die IP-Adressen für sekundäre DNS-Server in der Zone zurück.
ms.assetid: b9a47714-f180-40cf-831a-f59e804a4ca2
keywords:
- Resetsecon-Methode (DNS)
- Resetsecon-Methode (DNS), MicrosoftDNS_Zone-Klasse
- DNS-MicrosoftDNS_Zone Klasse, resetseconreplikat-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ResetSecondaries
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a78d65b2153782c38d6d91d34f642860e896ed1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956787"
---
# <a name="resetsecondaries-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="f6433-106">Resetsecon-Replikats-Methode der MicrosoftDNS- \_ Zonen Klasse</span><span class="sxs-lookup"><span data-stu-id="f6433-106">ResetSecondaries method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="f6433-107">Die **resetsecon-** Methode setzt die IP-Adressen für sekundäre DNS-Server in der Zone zurück.</span><span class="sxs-lookup"><span data-stu-id="f6433-107">The **ResetSecondaries** method resets the IP addresses for secondary DNS Servers in the zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6433-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6433-108">Syntax</span></span>


```mof
void ResetSecondaries(
  [in]       string            SecondaryServers[],
  [in]       uint32            SecureSecondaries,
  [in]       string            NotifyServers[],
  [in]       uint32            Notify,
  [out, ref] MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a><span data-ttu-id="f6433-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6433-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6433-110">*Secondaryservers* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6433-110">*SecondaryServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6433-111">Array von IP-Adressen für sekundäre DNS-Server.</span><span class="sxs-lookup"><span data-stu-id="f6433-111">Array of IP addresses for secondary DNS Servers.</span></span>

</dd> <dt>

<span data-ttu-id="f6433-112">*Securesecon-* \[ Replikate in\]</span><span class="sxs-lookup"><span data-stu-id="f6433-112">*SecureSecondaries* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6433-113">Gibt die anzuwendende Sicherheit an und muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="f6433-113">Specifies the security to be applied and must be one of the following:</span></span>

-   <span data-ttu-id="f6433-114">Zone \_ secsecure \_ No \_ Security</span><span class="sxs-lookup"><span data-stu-id="f6433-114">ZONE\_SECSECURE\_NO\_SECURITY</span></span>
-   <span data-ttu-id="f6433-115">\_nur Zonen secsecure \_ NS \_</span><span class="sxs-lookup"><span data-stu-id="f6433-115">ZONE\_SECSECURE\_NS\_ONLY</span></span>
-   <span data-ttu-id="f6433-116">nur Zonen- \_ secsecure- \_ Liste \_</span><span class="sxs-lookup"><span data-stu-id="f6433-116">ZONE\_SECSECURE\_LIST\_ONLY</span></span>
-   <span data-ttu-id="f6433-117">Zone \_ secsecure \_ No \_ XFR</span><span class="sxs-lookup"><span data-stu-id="f6433-117">ZONE\_SECSECURE\_NO\_XFR</span></span>

</dd> <dt>

<span data-ttu-id="f6433-118">*Notifyservers* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6433-118">*NotifyServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6433-119">IP-Adresse der DNS-Server, die benachrichtigt werden sollen, wenn die Zone geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f6433-119">IP address of DNS Servers to be notified when the zone changes.</span></span>

</dd> <dt>

<span data-ttu-id="f6433-120">*Benachrichtigen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6433-120">*Notify* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6433-121">Benachrichtigungs Einstellung und muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="f6433-121">Notification setting and must be one of the following:</span></span>

-   <span data-ttu-id="f6433-122">Benachrichtigung über Zonen \_ Benachrichtigung \_</span><span class="sxs-lookup"><span data-stu-id="f6433-122">ZONE\_NOTIFY\_OFF</span></span>
-   <span data-ttu-id="f6433-123">Zonen \_ Benachrichtigung für \_ alle \_ sekundären Datenbanken</span><span class="sxs-lookup"><span data-stu-id="f6433-123">ZONE\_NOTIFY\_ALL\_SECONDARIES</span></span>
-   <span data-ttu-id="f6433-124">\_nur Zonen Benachrichtigungs \_ Liste \_</span><span class="sxs-lookup"><span data-stu-id="f6433-124">ZONE\_NOTIFY\_LIST\_ONLY</span></span>

</dd> <dt>

<span data-ttu-id="f6433-125">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="f6433-125">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f6433-126">RR vom Typ [**MicrosoftDNS \_ Zone**](microsoftdns-zone.md).</span><span class="sxs-lookup"><span data-stu-id="f6433-126">RR of type [**MicrosoftDNS\_Zone**](microsoftdns-zone.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6433-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6433-127">Return value</span></span>

<span data-ttu-id="f6433-128">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f6433-128">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6433-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6433-129">Requirements</span></span>



| <span data-ttu-id="f6433-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6433-130">Requirement</span></span> | <span data-ttu-id="f6433-131">Wert</span><span class="sxs-lookup"><span data-stu-id="f6433-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6433-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f6433-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f6433-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f6433-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f6433-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f6433-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f6433-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f6433-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f6433-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="f6433-136">Namespace</span></span><br/>                | <span data-ttu-id="f6433-137">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="f6433-137">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="f6433-138">MOF</span><span class="sxs-lookup"><span data-stu-id="f6433-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6433-139"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f6433-139"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6433-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6433-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6433-141">**MicrosoftDNS- \_ Zone**</span><span class="sxs-lookup"><span data-stu-id="f6433-141">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="f6433-142">**AgeAllRecords-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="f6433-142">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="f6433-143">**Changezonetype-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="f6433-143">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="f6433-144">**Die Methode "kreatezone" der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="f6433-144">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="f6433-145">**ForceRefresh-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="f6433-145">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="f6433-146">**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="f6433-146">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="f6433-147">**Pauzzone-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="f6433-147">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="f6433-148">**Reloadzone-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="f6433-148">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="f6433-149">**Resumezone-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="f6433-149">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="f6433-150">**Updatefromds-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="f6433-150">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="f6433-151">**"Write Backzone"-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="f6433-151">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





