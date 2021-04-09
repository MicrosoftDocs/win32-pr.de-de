---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_AFSDBType-Klasse
description: Die Methode "kreateinstancefrompropertydata" instanziiert einen Ressourcen Eintrag für den Andrew File System Database Server (AFSDB).
ms.assetid: 2cd0434d-0c18-468f-95f3-7a77375596a3
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_AFSDBType
- DNS-MicrosoftDNS_AFSDBType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04efd6e18ef4267d9887252f91e8a215fcf3ee88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956478"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_afsdbtype-class"></a><span data-ttu-id="24ede-106">Die Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ afsdbtype-Klasse</span><span class="sxs-lookup"><span data-stu-id="24ede-106">CreateInstanceFromPropertyData method of the MicrosoftDNS\_AFSDBType class</span></span>

<span data-ttu-id="24ede-107">Die Methode " **kreateinstancefrompropertydata** " instanziiert einen Ressourcen Eintrag für den Andrew File System Database Server (AFSDB).</span><span class="sxs-lookup"><span data-stu-id="24ede-107">The **CreateInstanceFromPropertyData** method instantiates an Andrew File System Database Server (AFSDB) Resource Record.</span></span>

## <a name="syntax"></a><span data-ttu-id="24ede-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="24ede-108">Syntax</span></span>


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           uint16                 Subtype,
  [in]           string                 ServerName,
  [out, ref]     MicrosoftDNS_AFSDBType &RR
);
```



## <a name="parameters"></a><span data-ttu-id="24ede-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="24ede-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24ede-110">*Dnsservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24ede-110">*DnsServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24ede-111">Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.</span><span class="sxs-lookup"><span data-stu-id="24ede-111">FQDN or IP address of the DNS Server that contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="24ede-112">*Containername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24ede-112">*ContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24ede-113">Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.</span><span class="sxs-lookup"><span data-stu-id="24ede-113">Name of the Container for the Zone, Cache, or RootHints instance which contains this RR.</span></span>

</dd> <dt>

<span data-ttu-id="24ede-114">Besitzer *Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24ede-114">*OwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24ede-115">Der Besitzer Name für die RR.</span><span class="sxs-lookup"><span data-stu-id="24ede-115">Owner name for the RR.</span></span>

</dd> <dt>

<span data-ttu-id="24ede-116">*Recordclass* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="24ede-116">*RecordClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="24ede-117">Die Klasse von RR.</span><span class="sxs-lookup"><span data-stu-id="24ede-117">Class of the RR.</span></span> <span data-ttu-id="24ede-118">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="24ede-118">Default value is 1.</span></span> <span data-ttu-id="24ede-119">Die folgenden Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="24ede-119">The following values are valid.</span></span>



| <span data-ttu-id="24ede-120">Wert</span><span class="sxs-lookup"><span data-stu-id="24ede-120">Value</span></span>                                                                                                | <span data-ttu-id="24ede-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="24ede-121">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <span data-ttu-id="24ede-122"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="24ede-122"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="24ede-123">IN (Internet)</span><span class="sxs-lookup"><span data-stu-id="24ede-123">IN (Internet)</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="24ede-124"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="24ede-124"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="24ede-125">CS (CSNET)</span><span class="sxs-lookup"><span data-stu-id="24ede-125">CS (CSNET)</span></span><br/>    |
| <span id="3"></span><dl> <span data-ttu-id="24ede-126"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="24ede-126"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="24ede-127">CH (Chaos)</span><span class="sxs-lookup"><span data-stu-id="24ede-127">CH (CHAOS)</span></span><br/>    |
| <span id="4"></span><dl> <span data-ttu-id="24ede-128"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="24ede-128"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="24ede-129">HS (Hesiod)</span><span class="sxs-lookup"><span data-stu-id="24ede-129">HS (Hesiod)</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="24ede-130">Gültigkeitsdauer  \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="24ede-130">*TTL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="24ede-131">Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="24ede-131">Time, in seconds, that the RR can be cached by a DNS resolver.</span></span>

</dd> <dt>

<span data-ttu-id="24ede-132">*Untertyp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24ede-132">*Subtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24ede-133">Der Untertyp des Host-AFS-Servers.</span><span class="sxs-lookup"><span data-stu-id="24ede-133">Subtype of the host AFS server.</span></span> <span data-ttu-id="24ede-134">Für den Untertyp 1 (Wert = 1) verfügt der Host über einen mespeicherort-Server der Version 3,0 für die benannte AFS-Zelle.</span><span class="sxs-lookup"><span data-stu-id="24ede-134">For subtype 1 (value=1), the host has an AFS version 3.0 Volume Location Server for the named AFS cell.</span></span> <span data-ttu-id="24ede-135">Im Fall von Untertyp 2 (Wert = 2) verfügt der Host über einen authentifizierten Namen Server, der den Zellen Stammverzeichnis-Knoten für die benannte DCE/NCA-Zelle enthält.</span><span class="sxs-lookup"><span data-stu-id="24ede-135">In the case of subtype 2 (value=2), the host has an authenticated name server holding the cell-root directory node for the named DCE/NCA cell.</span></span>

</dd> <dt>

<span data-ttu-id="24ede-136">*Servername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24ede-136">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24ede-137">Ein voll qualifizierter Host, der einen Host mit einem Server für die im Besitzer Namen angegebene AFS-Zelle angibt.</span><span class="sxs-lookup"><span data-stu-id="24ede-137">FQDN specifying a host that has a server for the AFS cell specified in the owner name.</span></span>

</dd> <dt>

<span data-ttu-id="24ede-138">*RR* \[ Out, Ref\]</span><span class="sxs-lookup"><span data-stu-id="24ede-138">*RR* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="24ede-139">Verweis auf das neue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="24ede-139">Reference to the new object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24ede-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24ede-140">Return value</span></span>

<span data-ttu-id="24ede-141">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="24ede-141">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="24ede-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24ede-142">Requirements</span></span>



| <span data-ttu-id="24ede-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24ede-143">Requirement</span></span> | <span data-ttu-id="24ede-144">Wert</span><span class="sxs-lookup"><span data-stu-id="24ede-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="24ede-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="24ede-145">Minimum supported client</span></span><br/> | <span data-ttu-id="24ede-146">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="24ede-146">None supported</span></span><br/>                                                              |
| <span data-ttu-id="24ede-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="24ede-147">Minimum supported server</span></span><br/> | <span data-ttu-id="24ede-148">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="24ede-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="24ede-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="24ede-149">Namespace</span></span><br/>                | <span data-ttu-id="24ede-150">\\MicrosoftDNS-Stamm</span><span class="sxs-lookup"><span data-stu-id="24ede-150">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="24ede-151">MOF</span><span class="sxs-lookup"><span data-stu-id="24ede-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24ede-152"><dt>Dnsprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="24ede-152"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24ede-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24ede-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24ede-154">**MicrosoftDNS \_ afsdbtype**</span><span class="sxs-lookup"><span data-stu-id="24ede-154">**MicrosoftDNS\_AFSDBType**</span></span>](microsoftdns-afsdbtype.md)
</dt> <dt>

[<span data-ttu-id="24ede-155">**Modify-Methode der MicrosoftDNS \_ afsdbtype-Klasse**</span><span class="sxs-lookup"><span data-stu-id="24ede-155">**Modify Method of the MicrosoftDNS\_AFSDBType Class**</span></span>](microsoftdns-afsdbtype-modify.md)
</dt> <dt>

[<span data-ttu-id="24ede-156">**MicrosoftDNS \_ resourcerecord**</span><span class="sxs-lookup"><span data-stu-id="24ede-156">**MicrosoftDNS\_ResourceRecord**</span></span>](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





