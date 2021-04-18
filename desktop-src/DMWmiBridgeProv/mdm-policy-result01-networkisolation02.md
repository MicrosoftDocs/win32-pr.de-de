---
title: MDM_Policy_Result01_NetworkIsolation02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ NetworkIsolation02-Klasse stellt die verfügbaren Browser Richtlinien dar.
ms.assetid: f44f43fb-813b-4d40-a56c-0c497e004a8a
keywords:
- MDM_Policy_Result01_NetworkIsolation02-Klasse
- MDM_Policy_Result01_NetworkIsolation02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_NetworkIsolation02
- MDM_Policy_Result01_NetworkIsolation02.InstanceID
- MDM_Policy_Result01_NetworkIsolation02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5611d7e00ab0fa5210a657b55a3f2990fdf40880
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103454"
---
# <a name="mdm_policy_result01_networkisolation02-class"></a><span data-ttu-id="11a39-105">MDM- \_ Richtlinie \_ Result01 \_ NetworkIsolation02-Klasse</span><span class="sxs-lookup"><span data-stu-id="11a39-105">MDM\_Policy\_Result01\_NetworkIsolation02 class</span></span>

<span data-ttu-id="11a39-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="11a39-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="11a39-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="11a39-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="11a39-108">Die **MDM- \_ Richtlinie \_ Result01 \_ NetworkIsolation02** -Klasse stellt die verfügbaren Browser Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="11a39-108">The **MDM\_Policy\_Result01\_NetworkIsolation02** class represents the browser policies available.</span></span>

<span data-ttu-id="11a39-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="11a39-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="11a39-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="11a39-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_NetworkIsolation02
{
  string InstanceID;
  string ParentID;
  string EnterpriseIPRange;
  sint32 EnterpriseIPRangesAreAuthoritative;
  string EnterpriseNetworkDomainNames;
  string EnterpriseProxyServers;
  sint32 EnterpriseProxyServersAreAuthoritative;
  string EnterpriseCloudResources;
  string EnterpriseInternalProxyServers;
  string NeutralResources;
};
```

## <a name="members"></a><span data-ttu-id="11a39-111">Member</span><span class="sxs-lookup"><span data-stu-id="11a39-111">Members</span></span>

<span data-ttu-id="11a39-112">Die **MDM- \_ Richtlinie \_ Result01 \_ NetworkIsolation02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="11a39-112">The **MDM\_Policy\_Result01\_NetworkIsolation02** class has these types of members:</span></span>

-   [<span data-ttu-id="11a39-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11a39-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="11a39-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="11a39-114">Properties</span></span>

<span data-ttu-id="11a39-115">Die **MDM- \_ Richtlinie \_ Result01 \_ NetworkIsolation02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="11a39-115">The **MDM\_Policy\_Result01\_NetworkIsolation02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="11a39-116">EnterpriseCloudResources</span><span class="sxs-lookup"><span data-stu-id="11a39-116">EnterpriseCloudResources</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterprisecloudresources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a39-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11a39-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11a39-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="11a39-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="11a39-119">EnterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="11a39-119">EnterpriseInternalProxyServers</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseinternalproxyservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a39-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11a39-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11a39-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="11a39-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="11a39-122">EnterpriseIPRange</span><span class="sxs-lookup"><span data-stu-id="11a39-122">EnterpriseIPRange</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseiprange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a39-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11a39-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11a39-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="11a39-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="11a39-125">Enterpriseiprangesaretative</span><span class="sxs-lookup"><span data-stu-id="11a39-125">EnterpriseIPRangesAreAuthoritative</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseiprangesareauthoritative)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a39-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="11a39-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="11a39-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="11a39-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="11a39-128">EnterpriseNetworkDomainNames</span><span class="sxs-lookup"><span data-stu-id="11a39-128">EnterpriseNetworkDomainNames</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterprisenetworkdomainnames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a39-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11a39-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11a39-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="11a39-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="11a39-131">EnterpriseProxyServers</span><span class="sxs-lookup"><span data-stu-id="11a39-131">EnterpriseProxyServers</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseproxyservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a39-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11a39-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11a39-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="11a39-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="11a39-134">Enterpriseproxyserversaretative</span><span class="sxs-lookup"><span data-stu-id="11a39-134">EnterpriseProxyServersAreAuthoritative</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseproxyserversareauthoritative)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a39-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="11a39-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="11a39-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="11a39-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="11a39-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="11a39-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a39-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11a39-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11a39-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11a39-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11a39-140">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="11a39-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="11a39-141">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="11a39-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="11a39-142">Für diese Klasse ist die Zeichenfolge "networkisolation".</span><span class="sxs-lookup"><span data-stu-id="11a39-142">For this class, the string is "NetworkIsolation".</span></span>

</dd> <dt>

[<span data-ttu-id="11a39-143">Neutralresources</span><span class="sxs-lookup"><span data-stu-id="11a39-143">NeutralResources</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-neutralresources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a39-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11a39-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11a39-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="11a39-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="11a39-146">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="11a39-146">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a39-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="11a39-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11a39-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="11a39-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11a39-149">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="11a39-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="11a39-150">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="11a39-150">Describes the full path to the parent node.</span></span> <span data-ttu-id="11a39-151">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/result".</span><span class="sxs-lookup"><span data-stu-id="11a39-151">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11a39-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11a39-152">Requirements</span></span>



| <span data-ttu-id="11a39-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11a39-153">Requirement</span></span> | <span data-ttu-id="11a39-154">Wert</span><span class="sxs-lookup"><span data-stu-id="11a39-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11a39-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11a39-155">Minimum supported client</span></span><br/> | <span data-ttu-id="11a39-156">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11a39-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="11a39-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11a39-157">Minimum supported server</span></span><br/> | <span data-ttu-id="11a39-158">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="11a39-158">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="11a39-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="11a39-159">Namespace</span></span><br/>                | <span data-ttu-id="11a39-160">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="11a39-160">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="11a39-161">MOF</span><span class="sxs-lookup"><span data-stu-id="11a39-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11a39-162"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="11a39-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="11a39-163">DLL</span><span class="sxs-lookup"><span data-stu-id="11a39-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11a39-164"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11a39-164"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

