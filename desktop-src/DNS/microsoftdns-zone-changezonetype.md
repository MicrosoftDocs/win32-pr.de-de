---
title: Changezonetype-Methode der MicrosoftDNS_Zone-Klasse
description: Die changezonetype-Methode ändert den Typ einer Zone.
ms.assetid: a0a9f495-fdbb-4258-a313-ee9551da762f
keywords:
- Changezonetype-Methode (DNS)
- Changezonetype-Methode, DNS, MicrosoftDNS_Zone-Klasse
- MicrosoftDNS_Zone-Klasse DNS, changezonetype-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ChangeZoneType
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1611eda876532f32534e24257478b3a5986af3aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040486"
---
# <a name="changezonetype-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="86e19-106">Changezonetype-Methode der MicrosoftDNS- \_ Zonen Klasse</span><span class="sxs-lookup"><span data-stu-id="86e19-106">ChangeZoneType method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="86e19-107">Die **changezonetype** -Methode ändert den Typ einer Zone.</span><span class="sxs-lookup"><span data-stu-id="86e19-107">The **ChangeZoneType** method changes the type of a zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="86e19-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="86e19-108">Syntax</span></span>


```mof
void ChangeZoneType(
  [in]           uint32            ZoneType,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a><span data-ttu-id="86e19-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="86e19-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86e19-110">*Zonetype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86e19-110">*ZoneType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86e19-111">Zonentyp.</span><span class="sxs-lookup"><span data-stu-id="86e19-111">Type of zone.</span></span> <span data-ttu-id="86e19-112">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="86e19-112">Valid values are the following:</span></span>



| <span data-ttu-id="86e19-113">Wert</span><span class="sxs-lookup"><span data-stu-id="86e19-113">Value</span></span>                                                                        | <span data-ttu-id="86e19-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="86e19-114">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="86e19-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="86e19-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="86e19-116">Primäre Zone</span><span class="sxs-lookup"><span data-stu-id="86e19-116">Primary zone.</span></span><br/>   |
| <dl> <span data-ttu-id="86e19-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="86e19-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="86e19-118">Sekundäre Zone.</span><span class="sxs-lookup"><span data-stu-id="86e19-118">Secondary zone.</span></span><br/> |
| <dl> <span data-ttu-id="86e19-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="86e19-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="86e19-120">Stub-Zone.</span><span class="sxs-lookup"><span data-stu-id="86e19-120">Stub zone.</span></span><br/>      |
| <dl> <span data-ttu-id="86e19-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="86e19-121"><dt>3</dt></span></span> </dl> | <span data-ttu-id="86e19-122">Zonen Weiterleitung.</span><span class="sxs-lookup"><span data-stu-id="86e19-122">Zone forwarder.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="86e19-123">*DataFileName* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="86e19-123">*DataFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="86e19-124">Der Name der Datendatei, die der Zone zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="86e19-124">Name of the data file associated with the zone.</span></span>

</dd> <dt>

<span data-ttu-id="86e19-125">*Ipaddr* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="86e19-125">*IpAddr* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="86e19-126">Die IP-Adresse des Mater-DNS-Servers für die Zone.</span><span class="sxs-lookup"><span data-stu-id="86e19-126">IP address of the mater DNS Server for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="86e19-127">*Adminemailname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="86e19-127">*AdminEmailName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="86e19-128">E-Mail-Adresse des Administrators, der für die Zone zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="86e19-128">Email address of the administrator responsible for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="86e19-129">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="86e19-129">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="86e19-130">RR vom Typ **MicrosoftDNS \_ Zone**.</span><span class="sxs-lookup"><span data-stu-id="86e19-130">RR of type **MicrosoftDns\_Zone**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86e19-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86e19-131">Return value</span></span>

<span data-ttu-id="86e19-132">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="86e19-132">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="86e19-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86e19-133">Requirements</span></span>



| <span data-ttu-id="86e19-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86e19-134">Requirement</span></span> | <span data-ttu-id="86e19-135">Wert</span><span class="sxs-lookup"><span data-stu-id="86e19-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="86e19-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86e19-136">Minimum supported client</span></span><br/> | <span data-ttu-id="86e19-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="86e19-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="86e19-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86e19-138">Minimum supported server</span></span><br/> | <span data-ttu-id="86e19-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86e19-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="86e19-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="86e19-140">Namespace</span></span><br/>                | <span data-ttu-id="86e19-141">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="86e19-141">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="86e19-142">MOF</span><span class="sxs-lookup"><span data-stu-id="86e19-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86e19-143"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="86e19-143"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86e19-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86e19-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86e19-145">**MicrosoftDNS- \_ Zone**</span><span class="sxs-lookup"><span data-stu-id="86e19-145">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="86e19-146">**AgeAllRecords-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="86e19-146">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="86e19-147">**Die Methode "kreatezone" der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="86e19-147">**CreateZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-createzone.md)
</dt> <dt>

[<span data-ttu-id="86e19-148">**ForceRefresh-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="86e19-148">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="86e19-149">**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="86e19-149">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="86e19-150">**Pauzzone-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="86e19-150">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="86e19-151">**Reloadzone-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="86e19-151">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="86e19-152">**Resetsecon-Replikats-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="86e19-152">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="86e19-153">**Resumezone-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="86e19-153">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="86e19-154">**Updatefromds-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="86e19-154">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="86e19-155">**"Write Backzone"-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="86e19-155">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





