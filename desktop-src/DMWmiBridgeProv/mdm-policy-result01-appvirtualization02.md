---
title: MDM_Policy_Result01_AppVirtualization02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ AppVirtualization02-Klasse stellt die verfügbaren anwendungsvirtualisierungsrichtlinien dar.
ms.assetid: fc28646f-f4b9-4648-a22d-b90d32ff888f
keywords:
- MDM_Policy_Result01_AppVirtualization02-Klasse
- MDM_Policy_Result01_AppVirtualization02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_AppVirtualization02
- MDM_Policy_Result01_AppVirtualization02.InstanceID
- MDM_Policy_Result01_AppVirtualization02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968c4718d7978bdf6770bdf8f828e6ef268cd32d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477283"
---
# <a name="mdm_policy_result01_appvirtualization02-class"></a><span data-ttu-id="41462-105">MDM- \_ Richtlinie \_ Result01 \_ AppVirtualization02-Klasse</span><span class="sxs-lookup"><span data-stu-id="41462-105">MDM\_Policy\_Result01\_AppVirtualization02 class</span></span>

<span data-ttu-id="41462-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="41462-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="41462-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="41462-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="41462-108">Die MDM- \_ Richtlinie \_ Result01 \_ AppVirtualization02-Klasse stellt die verfügbaren anwendungsvirtualisierungsrichtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="41462-108">The MDM\_Policy\_Result01\_AppVirtualization02 class represents the available app virtualization policies.</span></span>

<span data-ttu-id="41462-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="41462-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="41462-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="41462-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_AppVirtualization02
{
  string InstanceID;
  string ParentID;
  string AllowAppVClient;
  string AllowDynamicVirtualization;
  string AllowPackageCleanup;
  string AllowPackageScripts;
  string AllowPublishingRefreshUX;
  string AllowReportingServer;
  string AllowRoamingFileExclusions;
  string AllowRoamingRegistryExclusions;
  string AllowStreamingAutoload;
  string ClientCoexistenceAllowMigrationmode;
  string IntegrationAllowRootGlobal;
  string IntegrationAllowRootUser;
  string PublishingAllowServer1;
  string PublishingAllowServer2;
  string PublishingAllowServer3;
  string PublishingAllowServer4;
  string PublishingAllowServer5;
  string StreamingAllowCertificateFilterForClient_SSL;
  string StreamingAllowHighCostLaunch;
  string StreamingAllowLocationProvider;
  string StreamingAllowPackageInstallationRoot;
  string StreamingAllowPackageSourceRoot;
  string StreamingAllowReestablishmentInterval;
  string StreamingAllowReestablishmentRetries;
  string StreamingSharedContentStoreMode;
  string StreamingSupportBranchCache;
  string StreamingVerifyCertificateRevocationList;
  string VirtualComponentsAllowList;
};
```

## <a name="members"></a><span data-ttu-id="41462-111">Member</span><span class="sxs-lookup"><span data-stu-id="41462-111">Members</span></span>

<span data-ttu-id="41462-112">Die **MDM- \_ Richtlinie \_ Result01 \_ AppVirtualization02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="41462-112">The **MDM\_Policy\_Result01\_AppVirtualization02** class has these types of members:</span></span>

-   [<span data-ttu-id="41462-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41462-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="41462-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41462-114">Properties</span></span>

<span data-ttu-id="41462-115">Die **MDM- \_ Richtlinie \_ Result01 \_ AppVirtualization02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="41462-115">The **MDM\_Policy\_Result01\_AppVirtualization02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="41462-116">Allowappvclient</span><span class="sxs-lookup"><span data-stu-id="41462-116">AllowAppVClient</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowappvclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-119">Allowdynamicvirtualization</span><span class="sxs-lookup"><span data-stu-id="41462-119">AllowDynamicVirtualization</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowdynamicvirtualization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-122">Allowpackagecleanup</span><span class="sxs-lookup"><span data-stu-id="41462-122">AllowPackageCleanup</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpackagecleanup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-125">Allowpackagescripts</span><span class="sxs-lookup"><span data-stu-id="41462-125">AllowPackageScripts</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpackagescripts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-128">Allowpublishingrefreshux</span><span class="sxs-lookup"><span data-stu-id="41462-128">AllowPublishingRefreshUX</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpublishingrefreshux)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-131">"Zuordnung"</span><span class="sxs-lookup"><span data-stu-id="41462-131">AllowReportingServer</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowreportingserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-134">Allowroamingfileausschlüsse</span><span class="sxs-lookup"><span data-stu-id="41462-134">AllowRoamingFileExclusions</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowroamingfileexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-137">Allowroamingregistryausschlüsse</span><span class="sxs-lookup"><span data-stu-id="41462-137">AllowRoamingRegistryExclusions</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowroamingregistryexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-140">Allowstreamingautoload</span><span class="sxs-lookup"><span data-stu-id="41462-140">AllowStreamingAutoload</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowstreamingautoload)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-143">Clientcoexistenceallowmigrationmode</span><span class="sxs-lookup"><span data-stu-id="41462-143">ClientCoexistenceAllowMigrationmode</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-clientcoexistenceallowmigrationmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="41462-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="41462-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41462-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41462-149">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="41462-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-150">Integrationallowrootglobal</span><span class="sxs-lookup"><span data-stu-id="41462-150">IntegrationAllowRootGlobal</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-integrationallowrootglobal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-152">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-153">Integrationallowrootuser</span><span class="sxs-lookup"><span data-stu-id="41462-153">IntegrationAllowRootUser</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-integrationallowrootuser)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-154">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-155">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="41462-156">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="41462-156">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="41462-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41462-159">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="41462-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-160">PublishingAllowServer1</span><span class="sxs-lookup"><span data-stu-id="41462-160">PublishingAllowServer1</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver1)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-162">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-163">PublishingAllowServer2</span><span class="sxs-lookup"><span data-stu-id="41462-163">PublishingAllowServer2</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver2)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-165">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-166">PublishingAllowServer3</span><span class="sxs-lookup"><span data-stu-id="41462-166">PublishingAllowServer3</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-168">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-168">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-169">PublishingAllowServer4</span><span class="sxs-lookup"><span data-stu-id="41462-169">PublishingAllowServer4</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver4)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-170">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-171">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-171">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-172">PublishingAllowServer5</span><span class="sxs-lookup"><span data-stu-id="41462-172">PublishingAllowServer5</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver5)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-173">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-174">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-174">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-175">Streamingallowcertificatefilterforclient- \_ SSL</span><span class="sxs-lookup"><span data-stu-id="41462-175">StreamingAllowCertificateFilterForClient\_SSL</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowcertificatefilterforclient-ssl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-176">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-177">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-177">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-178">Streamingzuweisung whighcostlaunch</span><span class="sxs-lookup"><span data-stu-id="41462-178">StreamingAllowHighCostLaunch</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowhighcostlaunch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-179">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-180">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-180">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-181">Streamingallowlocationprovider</span><span class="sxs-lookup"><span data-stu-id="41462-181">StreamingAllowLocationProvider</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowlocationprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-182">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-183">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-183">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-184">Streamingallowpackageingestallationroot</span><span class="sxs-lookup"><span data-stu-id="41462-184">StreamingAllowPackageInstallationRoot</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowpackageinstallationroot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-185">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-186">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-186">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-187">Streamingallowpackagesourceroot</span><span class="sxs-lookup"><span data-stu-id="41462-187">StreamingAllowPackageSourceRoot</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowpackagesourceroot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-188">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-189">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-189">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-190">Streamingzuordnung</span><span class="sxs-lookup"><span data-stu-id="41462-190">StreamingAllowReestablishmentInterval</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowreestablishmentinterval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-191">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-192">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-192">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-193">Streamingzufügungen</span><span class="sxs-lookup"><span data-stu-id="41462-193">StreamingAllowReestablishmentRetries</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowreestablishmentretries)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-194">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-195">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-195">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-196">Streamingsharedcontentstoremode</span><span class="sxs-lookup"><span data-stu-id="41462-196">StreamingSharedContentStoreMode</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingsharedcontentstoremode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-197">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-198">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-198">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-199">Streamingsupportbranchcache</span><span class="sxs-lookup"><span data-stu-id="41462-199">StreamingSupportBranchCache</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingsupportbranchcache)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-200">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-201">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-201">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-202">Streamingverifycertificaterevocationlist</span><span class="sxs-lookup"><span data-stu-id="41462-202">StreamingVerifyCertificateRevocationList</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingverifycertificaterevocationlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-203">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-204">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-204">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="41462-205">Virtualcomponentsallowlist</span><span class="sxs-lookup"><span data-stu-id="41462-205">VirtualComponentsAllowList</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-virtualcomponentsallowlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="41462-206">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="41462-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41462-207">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="41462-207">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41462-208">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41462-208">Requirements</span></span>



| <span data-ttu-id="41462-209">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41462-209">Requirement</span></span> | <span data-ttu-id="41462-210">Wert</span><span class="sxs-lookup"><span data-stu-id="41462-210">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41462-211">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41462-211">Minimum supported client</span></span><br/> | <span data-ttu-id="41462-212">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41462-212">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="41462-213">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41462-213">Minimum supported server</span></span><br/> | <span data-ttu-id="41462-214">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="41462-214">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="41462-215">Namespace</span><span class="sxs-lookup"><span data-stu-id="41462-215">Namespace</span></span><br/>                | <span data-ttu-id="41462-216">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="41462-216">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="41462-217">MOF</span><span class="sxs-lookup"><span data-stu-id="41462-217">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41462-218"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="41462-218"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="41462-219">DLL</span><span class="sxs-lookup"><span data-stu-id="41462-219">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41462-220"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41462-220"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

