---
title: Die Methode "kreatezone" der MicrosoftDNS_Zone-Klasse
description: Die Methode "kreatezone" erstellt eine DNS-Zone.
ms.assetid: 55756284-20ef-4d38-a8d9-357f53a6fa4d
keywords:
- Methode der Methode "kreatezone"
- Methode der Methoden-DNS, MicrosoftDNS_Zone-Klasse
- DNS-MicrosoftDNS_Zone Klasse, Methode "kreatezone"
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.CreateZone
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7e3780db9036e0fd7c87d91c769c3c6f5c6aaf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040784"
---
# <a name="createzone-method-of-the-microsoftdns_zone-class"></a><span data-ttu-id="73d4a-106">Die Methode "kreatezone" der MicrosoftDNS- \_ Zonen Klasse</span><span class="sxs-lookup"><span data-stu-id="73d4a-106">CreateZone method of the MicrosoftDNS\_Zone class</span></span>

<span data-ttu-id="73d4a-107">Die Methode " **kreatezone** " erstellt eine DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="73d4a-107">The **CreateZone** method creates a DNS zone.</span></span>

## <a name="syntax"></a><span data-ttu-id="73d4a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="73d4a-108">Syntax</span></span>


```mof
void CreateZone(
  [in]           string            ZoneName,
  [in]           uint32            ZoneType,
  [in]           boolean           DsIntegrated,
  [in, optional] string            DataFileName,
  [in, optional] string            IpAddr[],
  [in, optional] string            AdminEmailName,
  [out, ref]     MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a><span data-ttu-id="73d4a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="73d4a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73d4a-110">*Zonenname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73d4a-110">*ZoneName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73d4a-111">Eine Zeichenfolge, die den Namen der Zone darstellt.</span><span class="sxs-lookup"><span data-stu-id="73d4a-111">String representing the name of the zone.</span></span>

</dd> <dt>

<span data-ttu-id="73d4a-112">*Zonetype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73d4a-112">*ZoneType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73d4a-113">Zonentyp.</span><span class="sxs-lookup"><span data-stu-id="73d4a-113">Type of zone.</span></span> <span data-ttu-id="73d4a-114">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="73d4a-114">Valid values are the following:</span></span>



| <span data-ttu-id="73d4a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="73d4a-115">Value</span></span>                                                                        | <span data-ttu-id="73d4a-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="73d4a-116">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="73d4a-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="73d4a-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="73d4a-118">AD integriert.</span><span class="sxs-lookup"><span data-stu-id="73d4a-118">AD integrated.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="73d4a-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="73d4a-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="73d4a-120">Sekundäre Zone.</span><span class="sxs-lookup"><span data-stu-id="73d4a-120">Secondary zone.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="73d4a-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="73d4a-121"><dt>3</dt></span></span> </dl> | <span data-ttu-id="73d4a-122">Stub-Zone.</span><span class="sxs-lookup"><span data-stu-id="73d4a-122">Stub zone.</span></span><br/> <span data-ttu-id="73d4a-123">**Windows Server 2003:** Dieser Zonentyp wird in Windows Server 2003 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="73d4a-123">**Windows Server 2003:** This zone type is introduced in Windows Server 2003.</span></span><br/>      |
| <dl> <span data-ttu-id="73d4a-124"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="73d4a-124"><dt>4</dt></span></span> </dl> | <span data-ttu-id="73d4a-125">Zonen Weiterleitung.</span><span class="sxs-lookup"><span data-stu-id="73d4a-125">Zone forwarder.</span></span><br/> <span data-ttu-id="73d4a-126">**Windows Server 2003:** Dieser Zonentyp wird in Windows Server 2003 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="73d4a-126">**Windows Server 2003:** This zone type is introduced in Windows Server 2003.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="73d4a-127">*Dsintegriert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73d4a-127">*DsIntegrated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73d4a-128">Gibt an, ob Zonendaten in der Active Directory oder in Dateien gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="73d4a-128">Indicates whether zone data is stored in the Active Directory or in files.</span></span> <span data-ttu-id="73d4a-129">Wenn der Wert true ist, werden die Daten in der Active Directory gespeichert. Wenn der Wert false ist, werden die Daten in Dateien gespeichert.</span><span class="sxs-lookup"><span data-stu-id="73d4a-129">If TRUE, the data is stored in the Active Directory; if FALSE, the data is stored in files.</span></span>

</dd> <dt>

<span data-ttu-id="73d4a-130">*DataFileName* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="73d4a-130">*DataFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="73d4a-131">Der Name der Datendatei, die der Zone zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="73d4a-131">Name of the data file associated with the zone.</span></span>

</dd> <dt>

<span data-ttu-id="73d4a-132">*Ipaddr* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="73d4a-132">*IpAddr* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="73d4a-133">Die IP-Adresse des DNS-Master Servers für die Zone.</span><span class="sxs-lookup"><span data-stu-id="73d4a-133">IP address of the master DNS Server for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="73d4a-134">*Adminemailname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="73d4a-134">*AdminEmailName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="73d4a-135">E-Mail-Adresse des Administrators, der für die Zone zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="73d4a-135">Email address of the administrator responsible for the zone.</span></span>

</dd> <dt>

<span data-ttu-id="73d4a-136">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="73d4a-136">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="73d4a-137">RR vom Typ **MicrosoftDNS \_ Zone**.</span><span class="sxs-lookup"><span data-stu-id="73d4a-137">RR of type **MicrosoftDns\_Zone**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73d4a-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="73d4a-138">Return value</span></span>

<span data-ttu-id="73d4a-139">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="73d4a-139">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="73d4a-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73d4a-140">Requirements</span></span>



| <span data-ttu-id="73d4a-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73d4a-141">Requirement</span></span> | <span data-ttu-id="73d4a-142">Wert</span><span class="sxs-lookup"><span data-stu-id="73d4a-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73d4a-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73d4a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="73d4a-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="73d4a-144">None supported</span></span><br/>                                                              |
| <span data-ttu-id="73d4a-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73d4a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="73d4a-146">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73d4a-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="73d4a-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="73d4a-147">Namespace</span></span><br/>                | <span data-ttu-id="73d4a-148">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="73d4a-148">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="73d4a-149">MOF</span><span class="sxs-lookup"><span data-stu-id="73d4a-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73d4a-150"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="73d4a-150"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73d4a-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73d4a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73d4a-152">**MicrosoftDNS- \_ Zone**</span><span class="sxs-lookup"><span data-stu-id="73d4a-152">**MicrosoftDNS\_Zone**</span></span>](microsoftdns-zone.md)
</dt> <dt>

[<span data-ttu-id="73d4a-153">**AgeAllRecords-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="73d4a-153">**AgeAllRecords Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[<span data-ttu-id="73d4a-154">**Changezonetype-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="73d4a-154">**ChangeZoneType Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[<span data-ttu-id="73d4a-155">**ForceRefresh-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="73d4a-155">**ForceRefresh Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[<span data-ttu-id="73d4a-156">**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="73d4a-156">**GetDistinguishedName Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[<span data-ttu-id="73d4a-157">**Pauzzone-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="73d4a-157">**PauseZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-pausezone.md)
</dt> <dt>

[<span data-ttu-id="73d4a-158">**Reloadzone-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="73d4a-158">**ReloadZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[<span data-ttu-id="73d4a-159">**Resetsecon-Replikats-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="73d4a-159">**ResetSecondaries Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resetsecondaries.md)
</dt> <dt>

[<span data-ttu-id="73d4a-160">**Resumezone-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="73d4a-160">**ResumeZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-resumezone.md)
</dt> <dt>

[<span data-ttu-id="73d4a-161">**Updatefromds-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="73d4a-161">**UpdateFromDS Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[<span data-ttu-id="73d4a-162">**"Write Backzone"-Methode der MicrosoftDNS- \_ Zonen Klasse**</span><span class="sxs-lookup"><span data-stu-id="73d4a-162">**WriteBackZone Method of the MicrosoftDNS\_Zone Class**</span></span>](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





