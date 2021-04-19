---
title: NAP-Typkonstanten (naptypes. h)
description: Die folgenden NAP-Konstanten sind definiert.
ms.assetid: 2727487c-8c6a-4cd9-b6d8-253191a7d7f6
topic_type:
- apiref
api_name:
- maxSoHAttributeCount
- maxSoHAttributeSize
- minNetworkSoHSize
- maxNetworkSoHSize
- maxDwordCountPerSoHAttribute
- maxIpv4CountPerSoHAttribute
- maxIpv6CountPerSoHAttribute
- maxStringLength
- maxStringLengthInBytes
- maxSystemHealthEntityCount
- SystemHealthEntityCount
- maxEnforcerCount
- EnforcementEntityCount
- maxPrivateDataSize
- maxConnectionCountPerEnforcer
- maxCachedSoHCount
- freshSoHRequest
- shaFixup
- failureCategoryCount
- ComponentTypeEnforcementClientSoH
- ComponentTypeEnforcementClientRp
- defaultProtocolMaxSize
- maxProtocolMaxSize
- minProtocolMaxSize
- ProtocolMaxSize
api_location:
- NapTypes.h
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85692a7ccc9cbb602a34da714a5eeb488ea5c4a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346522"
---
# <a name="nap-type-constants"></a><span data-ttu-id="fc63c-103">NAP-Typkonstanten</span><span class="sxs-lookup"><span data-stu-id="fc63c-103">NAP Type Constants</span></span>

> [!Note]  
> <span data-ttu-id="fc63c-104">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fc63c-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="fc63c-105">Die folgenden NAP-Konstanten sind definiert.</span><span class="sxs-lookup"><span data-stu-id="fc63c-105">The following NAP constants are defined.</span></span>

<span data-ttu-id="fc63c-106">Die folgenden NAP-Konstanten werden in "naptypes. h" definiert:</span><span class="sxs-lookup"><span data-stu-id="fc63c-106">The following NAP constants are defined in NapTypes.h:</span></span>

<dl> <dt>

<span data-ttu-id="fc63c-107"><span id="maxSoHAttributeCount"></span><span id="maxsohattributecount"></span><span id="MAXSOHATTRIBUTECOUNT"></span>**maxsohattributecount**</span><span class="sxs-lookup"><span data-stu-id="fc63c-107"><span id="maxSoHAttributeCount"></span><span id="maxsohattributecount"></span><span id="MAXSOHATTRIBUTECOUNT"></span>**maxSoHAttributeCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-108">0x64</span><span class="sxs-lookup"><span data-stu-id="fc63c-108">0x64</span></span>
</dt> <dt>



<span data-ttu-id="fc63c-109">Die maximale Anzahl von [**sohattribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) -TLV-Objekten (Type-Length-Value), die einem [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fc63c-109">The maximum number of [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) type-length-value (TLV) objects associated with an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc63c-110"><span id="maxSoHAttributeSize"></span><span id="maxsohattributesize"></span><span id="MAXSOHATTRIBUTESIZE"></span>**maxsohattributesize**</span><span class="sxs-lookup"><span data-stu-id="fc63c-110"><span id="maxSoHAttributeSize"></span><span id="maxsohattributesize"></span><span id="MAXSOHATTRIBUTESIZE"></span>**maxSoHAttributeSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-111">0xfa0</span><span class="sxs-lookup"><span data-stu-id="fc63c-111">0xFA0</span></span>
</dt> <dt>



<span data-ttu-id="fc63c-112">Die maximale Größe (in Bytes) eines [**sohattribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) -Objekts, das einem [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)-Paket (Statement of Health) zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fc63c-112">The maximum size, in bytes, of a [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) object associated with a statement of health ([**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc63c-113"><span id="minNetworkSoHSize"></span><span id="minnetworksohsize"></span><span id="MINNETWORKSOHSIZE"></span>**minnetworksohsize**</span><span class="sxs-lookup"><span data-stu-id="fc63c-113"><span id="minNetworkSoHSize"></span><span id="minnetworksohsize"></span><span id="MINNETWORKSOHSIZE"></span>**minNetworkSoHSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-114">0xc</span><span class="sxs-lookup"><span data-stu-id="fc63c-114">0xC</span></span>
</dt> <dt>



<span data-ttu-id="fc63c-115">Die minimale Größe eines [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Pakets in Byte.</span><span class="sxs-lookup"><span data-stu-id="fc63c-115">The minimum size, in bytes, of an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc63c-116"><span id="maxNetworkSoHSize"></span><span id="maxnetworksohsize"></span><span id="MAXNETWORKSOHSIZE"></span>**maxnetworksohsize**</span><span class="sxs-lookup"><span data-stu-id="fc63c-116"><span id="maxNetworkSoHSize"></span><span id="maxnetworksohsize"></span><span id="MAXNETWORKSOHSIZE"></span>**maxNetworkSoHSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-117">0xfa0</span><span class="sxs-lookup"><span data-stu-id="fc63c-117">0xFA0</span></span>
</dt> <dt>



<span data-ttu-id="fc63c-118">Die maximale Größe eines [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Pakets in Byte.</span><span class="sxs-lookup"><span data-stu-id="fc63c-118">The maximum size, in bytes, of an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc63c-119"><span id="maxDwordCountPerSoHAttribute"></span><span id="maxdwordcountpersohattribute"></span><span id="MAXDWORDCOUNTPERSOHATTRIBUTE"></span>**maxdwordzählpersohattribute**</span><span class="sxs-lookup"><span data-stu-id="fc63c-119"><span id="maxDwordCountPerSoHAttribute"></span><span id="maxdwordcountpersohattribute"></span><span id="MAXDWORDCOUNTPERSOHATTRIBUTE"></span>**maxDwordCountPerSoHAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-120">maxsohattributesize/sizeof (DWORD)</span><span class="sxs-lookup"><span data-stu-id="fc63c-120">maxSoHAttributeSize / sizeof(DWORD)</span></span>
</dt> <dt>



<span data-ttu-id="fc63c-121">Die maximale Anzahl von DWORD-Werten, die einem [**sohattribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fc63c-121">The maximum number of DWORD values associated with an [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc63c-122"><span id="maxIpv4CountPerSoHAttribute"></span><span id="maxipv4countpersohattribute"></span><span id="MAXIPV4COUNTPERSOHATTRIBUTE"></span>**maxIpv4CountPerSoHAttribute**</span><span class="sxs-lookup"><span data-stu-id="fc63c-122"><span id="maxIpv4CountPerSoHAttribute"></span><span id="maxipv4countpersohattribute"></span><span id="MAXIPV4COUNTPERSOHATTRIBUTE"></span>**maxIpv4CountPerSoHAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-123">maxsohattributesize/0x4</span><span class="sxs-lookup"><span data-stu-id="fc63c-123">maxSoHAttributeSize / 0x4</span></span>
</dt> <dt>



<span data-ttu-id="fc63c-124">Die maximale Anzahl von IPv4-Adressen, die einem [**sohattribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fc63c-124">The maximum number of IPv4 addresses associated with an [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc63c-125"><span id="maxIpv6CountPerSoHAttribute"></span><span id="maxipv6countpersohattribute"></span><span id="MAXIPV6COUNTPERSOHATTRIBUTE"></span>**maxIpv6CountPerSoHAttribute**</span><span class="sxs-lookup"><span data-stu-id="fc63c-125"><span id="maxIpv6CountPerSoHAttribute"></span><span id="maxipv6countpersohattribute"></span><span id="MAXIPV6COUNTPERSOHATTRIBUTE"></span>**maxIpv6CountPerSoHAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-126">maxsohattributesize/0x10</span><span class="sxs-lookup"><span data-stu-id="fc63c-126">maxSoHAttributeSize / 0x10</span></span>
</dt> <dt>



<span data-ttu-id="fc63c-127">Die maximale Anzahl von IPv6-Adressen, die einem [**sohattribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fc63c-127">The maximum number of IPv6 addresses associated with an [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc63c-128"><span id="maxStringLength"></span><span id="maxstringlength"></span><span id="MAXSTRINGLENGTH"></span>**maxstringlength**</span><span class="sxs-lookup"><span data-stu-id="fc63c-128"><span id="maxStringLength"></span><span id="maxstringlength"></span><span id="MAXSTRINGLENGTH"></span>**maxStringLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-129">0x400</span><span class="sxs-lookup"><span data-stu-id="fc63c-129">0x400</span></span>
</dt> <dt>



<span data-ttu-id="fc63c-130">Die maximale Länge einer Zeichenfolge, die von der [**countedstring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) -Struktur angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fc63c-130">The maximum length of a string specified by the [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc63c-131"><span id="maxStringLengthInBytes"></span><span id="maxstringlengthinbytes"></span><span id="MAXSTRINGLENGTHINBYTES"></span>**maxstringlengthinbytes**</span><span class="sxs-lookup"><span data-stu-id="fc63c-131"><span id="maxStringLengthInBytes"></span><span id="maxstringlengthinbytes"></span><span id="MAXSTRINGLENGTHINBYTES"></span>**maxStringLengthInBytes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-132">(maxstringlength + 1) \* sizeof (WChar)</span><span class="sxs-lookup"><span data-stu-id="fc63c-132">(maxStringLength + 1) \* sizeof(WCHAR)</span></span>
</dt> <dt>



<span data-ttu-id="fc63c-133">Die maximale Länge einer Zeichenfolge in Bytes, die von der [**countedstring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) -Struktur angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fc63c-133">The maximum length, in bytes, of a string specified by the [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc63c-134"><span id="maxSystemHealthEntityCount"></span><span id="maxsystemhealthentitycount"></span><span id="MAXSYSTEMHEALTHENTITYCOUNT"></span>**maxsystemhealthentitycount**</span><span class="sxs-lookup"><span data-stu-id="fc63c-134"><span id="maxSystemHealthEntityCount"></span><span id="maxsystemhealthentitycount"></span><span id="MAXSYSTEMHEALTHENTITYCOUNT"></span>**maxSystemHealthEntityCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-135">0x14</span><span class="sxs-lookup"><span data-stu-id="fc63c-135">0x14</span></span>
</dt> <dt>



<span data-ttu-id="fc63c-136">Die maximale Anzahl von Systemintegritäts-Entitäten, z. b. SHVs und SHAs.</span><span class="sxs-lookup"><span data-stu-id="fc63c-136">The maximum number of system health entities, such as SHVs and SHAs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc63c-137"><span id="SystemHealthEntityCount"></span><span id="systemhealthentitycount"></span><span id="SYSTEMHEALTHENTITYCOUNT"></span>**Systemhealthentitycount**</span><span class="sxs-lookup"><span data-stu-id="fc63c-137"><span id="SystemHealthEntityCount"></span><span id="systemhealthentitycount"></span><span id="SYSTEMHEALTHENTITYCOUNT"></span>**SystemHealthEntityCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-138">\[Bereich (0, maxsystemhealthentitycount)\]</span><span class="sxs-lookup"><span data-stu-id="fc63c-138">\[range(0, maxSystemHealthEntityCount)\]</span></span> 
</dt> <dt>



<span data-ttu-id="fc63c-139">Der Bereich möglicher Werte für die Anzahl der Systemintegritäts-Entitäten.</span><span class="sxs-lookup"><span data-stu-id="fc63c-139">The range of possible values for the number of system health entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc63c-140"><span id="maxEnforcerCount"></span><span id="maxenforcercount"></span><span id="MAXENFORCERCOUNT"></span>**maxenforcercount**</span><span class="sxs-lookup"><span data-stu-id="fc63c-140"><span id="maxEnforcerCount"></span><span id="maxenforcercount"></span><span id="MAXENFORCERCOUNT"></span>**maxEnforcerCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-141">0x14</span><span class="sxs-lookup"><span data-stu-id="fc63c-141">0x14</span></span>
</dt> <dt>



<span data-ttu-id="fc63c-142">Die maximale Anzahl von Erzwingungs Entitäten, z. b. qecs.</span><span class="sxs-lookup"><span data-stu-id="fc63c-142">The maximum number of enforcement entities, such as QECs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc63c-143"><span id="EnforcementEntityCount"></span><span id="enforcemententitycount"></span><span id="ENFORCEMENTENTITYCOUNT"></span>**Enforcemententitycount**</span><span class="sxs-lookup"><span data-stu-id="fc63c-143"><span id="EnforcementEntityCount"></span><span id="enforcemententitycount"></span><span id="ENFORCEMENTENTITYCOUNT"></span>**EnforcementEntityCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-144">\[Bereich (0, maxenforcercount)\]</span><span class="sxs-lookup"><span data-stu-id="fc63c-144">\[range(0, maxEnforcerCount)\]</span></span>
</dt> <dt>



<span data-ttu-id="fc63c-145">Der Bereich möglicher Werte für die Anzahl von Erzwingungs Entitäten.</span><span class="sxs-lookup"><span data-stu-id="fc63c-145">The range of possible values for the number of enforcement entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc63c-146"><span id="maxPrivateDataSize"></span><span id="maxprivatedatasize"></span><span id="MAXPRIVATEDATASIZE"></span>**maxprivatedatasize**</span><span class="sxs-lookup"><span data-stu-id="fc63c-146"><span id="maxPrivateDataSize"></span><span id="maxprivatedatasize"></span><span id="MAXPRIVATEDATASIZE"></span>**maxPrivateDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-147">0xc8</span><span class="sxs-lookup"><span data-stu-id="fc63c-147">0xC8</span></span>
</dt> <dt>



<span data-ttu-id="fc63c-148">Die maximale Größe einer [**PRIVATEDATA**](/windows/win32/api/naptypes/ns-naptypes-privatedata) -Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="fc63c-148">The maximum size, in bytes, of a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc63c-149"><span id="maxConnectionCountPerEnforcer"></span><span id="maxconnectioncountperenforcer"></span><span id="MAXCONNECTIONCOUNTPERENFORCER"></span>**maxconnectioncountrytperenforcer**</span><span class="sxs-lookup"><span data-stu-id="fc63c-149"><span id="maxConnectionCountPerEnforcer"></span><span id="maxconnectioncountperenforcer"></span><span id="MAXCONNECTIONCOUNTPERENFORCER"></span>**maxConnectionCountPerEnforcer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-150">0x14</span><span class="sxs-lookup"><span data-stu-id="fc63c-150">0x14</span></span>
</dt> <dt>



<span data-ttu-id="fc63c-151">Die maximale Anzahl von [**inapenforcementclientconnection**](inapenforcementclientconnection.md) -Objekten, die einer Erzwingungs Entität zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fc63c-151">The maximum number of [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) objects associated with an enforcement entity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc63c-152"><span id="maxCachedSoHCount"></span><span id="maxcachedsohcount"></span><span id="MAXCACHEDSOHCOUNT"></span>**maxcachedsohcount**</span><span class="sxs-lookup"><span data-stu-id="fc63c-152"><span id="maxCachedSoHCount"></span><span id="maxcachedsohcount"></span><span id="MAXCACHEDSOHCOUNT"></span>**maxCachedSoHCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-153">maxsystemhealthentitycount \* maxenforcercount \* maxconnectiongräfin-perenforcer</span><span class="sxs-lookup"><span data-stu-id="fc63c-153">maxSystemHealthEntityCount \* maxEnforcerCount \* maxConnectionCountPerEnforcer</span></span>
</dt> <dt>



<span data-ttu-id="fc63c-154">Die maximale Anzahl von zwischengespeicherten SoH-Verbindungen für alle Systemintegritäts-und Erzwingungs Entitäten.</span><span class="sxs-lookup"><span data-stu-id="fc63c-154">The maximum number of cached SoH connections for all system health and enforcement entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc63c-155"><span id="freshSoHRequest"></span><span id="freshsohrequest"></span><span id="FRESHSOHREQUEST"></span>**freshsohrequest**</span><span class="sxs-lookup"><span data-stu-id="fc63c-155"><span id="freshSoHRequest"></span><span id="freshsohrequest"></span><span id="FRESHSOHREQUEST"></span>**freshSoHRequest**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-156">0x1</span><span class="sxs-lookup"><span data-stu-id="fc63c-156">0x1</span></span>
</dt> <dt>



<span data-ttu-id="fc63c-157">Gibt an, dass ein [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh)-Wert auf eine neue Anforderung und nicht auf eine zwischengespeicherte Anforderung zurückzuführen ist.</span><span class="sxs-lookup"><span data-stu-id="fc63c-157">Specifies that an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh)is due to a new request, not a cached request.</span></span> <span data-ttu-id="fc63c-158">Dieses Flag wird vom NAP-Agent auf einem [**inapenforcementclientconnection**](inapenforcementclientconnection.md) -Objekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="fc63c-158">This flag is used by the NAP agent on an [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc63c-159"><span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span>**shafixup**</span><span class="sxs-lookup"><span data-stu-id="fc63c-159"><span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span>**shaFixup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-160">0x1</span><span class="sxs-lookup"><span data-stu-id="fc63c-160">0x1</span></span>
</dt> <dt>



<span data-ttu-id="fc63c-161">Gibt an, dass ein Problem behoben werden muss.</span><span class="sxs-lookup"><span data-stu-id="fc63c-161">Specifies that fix-up is required.</span></span> <span data-ttu-id="fc63c-162">Dieses Flag wird von einem SHA verwendet.</span><span class="sxs-lookup"><span data-stu-id="fc63c-162">This flag is used by a SHA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc63c-163"><span id="failureCategoryCount"></span><span id="failurecategorycount"></span><span id="FAILURECATEGORYCOUNT"></span>**failurecategorycount**</span><span class="sxs-lookup"><span data-stu-id="fc63c-163"><span id="failureCategoryCount"></span><span id="failurecategorycount"></span><span id="FAILURECATEGORYCOUNT"></span>**failureCategoryCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-164">0x5</span><span class="sxs-lookup"><span data-stu-id="fc63c-164">0x5</span></span>
</dt> <dt>



<span data-ttu-id="fc63c-165">Die Anzahl der Fehlerkategorien, die in einer [**failurecategorymapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) -Struktur enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="fc63c-165">The number of failure categories contained within a [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc63c-166"><span id="ComponentTypeEnforcementClientSoH"></span><span id="componenttypeenforcementclientsoh"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTSOH"></span>**Componenttypeenforcementclientsoh**</span><span class="sxs-lookup"><span data-stu-id="fc63c-166"><span id="ComponentTypeEnforcementClientSoH"></span><span id="componenttypeenforcementclientsoh"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTSOH"></span>**ComponentTypeEnforcementClientSoH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-167">0x1</span><span class="sxs-lookup"><span data-stu-id="fc63c-167">0x1</span></span>
</dt> <dt>



<span data-ttu-id="fc63c-168">Bei der Komponente handelt es sich um einen Quarantäne Erzwingungs Client (QEC), der während der Verbindungs Authentifizierung ein [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket in-Band sendet.</span><span class="sxs-lookup"><span data-stu-id="fc63c-168">The component is a quarantine enforcement client (QEC) that sends an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet in-band during connection authentication.</span></span>

> [!Note]  
> <span data-ttu-id="fc63c-169">Dieser Wert wird von SHAs und SHVs nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fc63c-169">This value is not used by SHAs and SHVs.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc63c-170"><span id="ComponentTypeEnforcementClientRp"></span><span id="componenttypeenforcementclientrp"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTRP"></span>**Componenttypeenforcementclientrp**</span><span class="sxs-lookup"><span data-stu-id="fc63c-170"><span id="ComponentTypeEnforcementClientRp"></span><span id="componenttypeenforcementclientrp"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTRP"></span>**ComponentTypeEnforcementClientRp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-171">0x2</span><span class="sxs-lookup"><span data-stu-id="fc63c-171">0x2</span></span>
</dt> <dt>



<span data-ttu-id="fc63c-172">Die Komponente ist ein QEC, das [**inapcertrelyingparty**](inapcertrelyingparty.md) implementiert und mit dem Integritäts Zertifikat Server (HCS) interagieren muss, damit ein Integritäts Zertifikat abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="fc63c-172">The component is a QEC that implements [**INapCertRelyingParty**](inapcertrelyingparty.md) and must interact with the Health Certificate Server (HCS) in order to obtain a health certificate.</span></span>

> [!Note]  
> <span data-ttu-id="fc63c-173">Dieser Wert wird von SHAs und SHVs nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fc63c-173">This value is not used by SHAs and SHVs.</span></span>

 


</dt> </dl> </dd> </dl>

<span data-ttu-id="fc63c-174">Die folgenden NAP-Konstanten werden in "napforcementclient. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="fc63c-174">The following NAP constants are defined in NapEnforcementClient.h.</span></span>

<dl> <dt>

<span data-ttu-id="fc63c-175"><span id="defaultProtocolMaxSize"></span><span id="defaultprotocolmaxsize"></span><span id="DEFAULTPROTOCOLMAXSIZE"></span>**defaultprotocolmaxsize**</span><span class="sxs-lookup"><span data-stu-id="fc63c-175"><span id="defaultProtocolMaxSize"></span><span id="defaultprotocolmaxsize"></span><span id="DEFAULTPROTOCOLMAXSIZE"></span>**defaultProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-176">0x0fa0</span><span class="sxs-lookup"><span data-stu-id="fc63c-176">0x0FA0</span></span>
</dt> <dt>



<span data-ttu-id="fc63c-177">Die maximale Standardgröße eines SoH-Pakets in Byte.</span><span class="sxs-lookup"><span data-stu-id="fc63c-177">The default maximum size, in bytes, of an SoH packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc63c-178"><span id="maxProtocolMaxSize"></span><span id="maxprotocolmaxsize"></span><span id="MAXPROTOCOLMAXSIZE"></span>**maxprotocolmaxsize**</span><span class="sxs-lookup"><span data-stu-id="fc63c-178"><span id="maxProtocolMaxSize"></span><span id="maxprotocolmaxsize"></span><span id="MAXPROTOCOLMAXSIZE"></span>**maxProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-179">0xFFFF</span><span class="sxs-lookup"><span data-stu-id="fc63c-179">0xFFFF</span></span>
</dt> <dt>



<span data-ttu-id="fc63c-180">Die maximal mögliche Größe eines SoH-Pakets in Bytes.</span><span class="sxs-lookup"><span data-stu-id="fc63c-180">The maximum possible size, in bytes, of an SoH packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc63c-181"><span id="minProtocolMaxSize"></span><span id="minprotocolmaxsize"></span><span id="MINPROTOCOLMAXSIZE"></span>**minprotocolmaxsize**</span><span class="sxs-lookup"><span data-stu-id="fc63c-181"><span id="minProtocolMaxSize"></span><span id="minprotocolmaxsize"></span><span id="MINPROTOCOLMAXSIZE"></span>**minProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-182">0x012c</span><span class="sxs-lookup"><span data-stu-id="fc63c-182">0x012C</span></span>
</dt> <dt>



<span data-ttu-id="fc63c-183">Die kleinste mögliche maximale Größe eines SoH-Pakets in Byte.</span><span class="sxs-lookup"><span data-stu-id="fc63c-183">The smallest possible maximum size, in bytes, of an SoH packet.</span></span> <span data-ttu-id="fc63c-184">Die tatsächliche Größe des SoH-Pakets kann kleiner als **minprotocolmaxsize** sein.</span><span class="sxs-lookup"><span data-stu-id="fc63c-184">The actual size of the SoH packet may be smaller than **minProtocolMaxSize**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fc63c-185"><span id="ProtocolMaxSize"></span><span id="protocolmaxsize"></span><span id="PROTOCOLMAXSIZE"></span>**Protocolmaxsize**</span><span class="sxs-lookup"><span data-stu-id="fc63c-185"><span id="ProtocolMaxSize"></span><span id="protocolmaxsize"></span><span id="PROTOCOLMAXSIZE"></span>**ProtocolMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc63c-186">Bereich (minprotocolmaxsize, maxprotocolmaxsize)</span><span class="sxs-lookup"><span data-stu-id="fc63c-186">range(minProtocolMaxSize, maxProtocolMaxSize)</span></span>
</dt> <dt>



<span data-ttu-id="fc63c-187">Der Bereich möglicher Werte für die maximale Größe eines SoH-Pakets.</span><span class="sxs-lookup"><span data-stu-id="fc63c-187">The range of possible values for the maximum size of a SoH packet.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fc63c-188">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc63c-188">Requirements</span></span>



| <span data-ttu-id="fc63c-189">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc63c-189">Requirement</span></span> | <span data-ttu-id="fc63c-190">Wert</span><span class="sxs-lookup"><span data-stu-id="fc63c-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc63c-191">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fc63c-191">Minimum supported client</span></span><br/> | <span data-ttu-id="fc63c-192">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc63c-192">Windows Vista \[desktop apps only\]</span></span><br/>                                                                                                                      |
| <span data-ttu-id="fc63c-193">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fc63c-193">Minimum supported server</span></span><br/> | <span data-ttu-id="fc63c-194">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc63c-194">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                |
| <span data-ttu-id="fc63c-195">Header</span><span class="sxs-lookup"><span data-stu-id="fc63c-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc63c-196"><dt>Naptypes. h; </dt> <dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc63c-196"><dt>NapTypes.h; </dt> <dt>NapEnforcementClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc63c-197">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc63c-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc63c-198">**NAP-Konstanten**</span><span class="sxs-lookup"><span data-stu-id="fc63c-198">**NAP Constants**</span></span>](nap-constants.md)
</dt> </dl>

 

 





