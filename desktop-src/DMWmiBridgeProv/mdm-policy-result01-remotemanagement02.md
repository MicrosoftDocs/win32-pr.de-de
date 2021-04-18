---
title: MDM_Policy_Result01_RemoteManagement02-Klasse
description: Die Result01 RemoteManagement02-Klasse der MDM- \_ Richtlinie \_ \_ stellt die Remote Verwaltungsrichtlinien dar.
ms.assetid: f6eb96ff-a40e-4602-a812-786d1a89bf12
keywords:
- MDM_Policy_Result01_RemoteManagement02-Klasse
- MDM_Policy_Result01_RemoteManagement02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_RemoteManagement02
- MDM_Policy_Result01_RemoteManagement02.InstanceID
- MDM_Policy_Result01_RemoteManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0a60228e39c8e1d6604534c8bd052ec7d40105e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475318"
---
# <a name="mdm_policy_result01_remotemanagement02-class"></a><span data-ttu-id="6b6c0-105">MDM- \_ Richtlinie \_ Result01 \_ RemoteManagement02-Klasse</span><span class="sxs-lookup"><span data-stu-id="6b6c0-105">MDM\_Policy\_Result01\_RemoteManagement02 class</span></span>

<span data-ttu-id="6b6c0-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="6b6c0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6b6c0-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="6b6c0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6b6c0-108">Die Result01 RemoteManagement02-Klasse der MDM- \_ Richtlinie \_ \_ stellt die Remote Verwaltungsrichtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="6b6c0-108">The MDM\_Policy\_Result01\_RemoteManagement02 class represents the remote management policies.</span></span>

<span data-ttu-id="6b6c0-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="6b6c0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b6c0-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b6c0-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_RemoteManagement02
{
  string InstanceID;
  string ParentID;
  string AllowBasicAuthentication_Client;
  string AllowBasicAuthentication_Service;
  string AllowCredSSPAuthenticationClient;
  string AllowCredSSPAuthenticationService;
  string AllowRemoteServerManagement;
  string AllowUnencryptedTraffic_Client;
  string AllowUnencryptedTraffic_Service;
  string DisallowDigestAuthentication;
  string DisallowNegotiateAuthenticationClient;
  string DisallowNegotiateAuthenticationService;
  string DisallowStoringOfRunAsCredentials;
  string SpecifyChannelBindingTokenHardeningLevel;
  string TrustedHosts;
  string TurnOnCompatibilityHTTPListener;
  string TurnOnCompatibilityHTTPSListener;
};
```

## <a name="members"></a><span data-ttu-id="6b6c0-111">Member</span><span class="sxs-lookup"><span data-stu-id="6b6c0-111">Members</span></span>

<span data-ttu-id="6b6c0-112">Die **MDM- \_ Richtlinie \_ Result01 \_ RemoteManagement02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6b6c0-112">The **MDM\_Policy\_Result01\_RemoteManagement02** class has these types of members:</span></span>

-   [<span data-ttu-id="6b6c0-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6b6c0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6b6c0-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6b6c0-114">Properties</span></span>

<span data-ttu-id="6b6c0-115">Die **MDM- \_ Richtlinie \_ Result01 \_ RemoteManagement02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6b6c0-115">The **MDM\_Policy\_Result01\_RemoteManagement02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6b6c0-116">Allowbasicauthentication- \_ Client</span><span class="sxs-lookup"><span data-stu-id="6b6c0-116">AllowBasicAuthentication\_Client</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowbasicauthentication-client)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b6c0-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b6c0-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b6c0-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6b6c0-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6b6c0-119">Allowbasicauthentication- \_ Dienst</span><span class="sxs-lookup"><span data-stu-id="6b6c0-119">AllowBasicAuthentication\_Service</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowbasicauthentication-service)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b6c0-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b6c0-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b6c0-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6b6c0-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6b6c0-122">Allowkredsspauthenticationclient</span><span class="sxs-lookup"><span data-stu-id="6b6c0-122">AllowCredSSPAuthenticationClient</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowcredsspauthenticationclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b6c0-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b6c0-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b6c0-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6b6c0-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6b6c0-125">Allowkredsspauthenticationservice</span><span class="sxs-lookup"><span data-stu-id="6b6c0-125">AllowCredSSPAuthenticationService</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowcredsspauthenticationservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b6c0-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b6c0-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b6c0-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6b6c0-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6b6c0-128">Allowremoteservermanagement</span><span class="sxs-lookup"><span data-stu-id="6b6c0-128">AllowRemoteServerManagement</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowremoteservermanagement)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b6c0-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b6c0-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b6c0-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6b6c0-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6b6c0-131">"Zugewunverschlüsseltedtraffic"- \_ Client</span><span class="sxs-lookup"><span data-stu-id="6b6c0-131">AllowUnencryptedTraffic\_Client</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowunencryptedtraffic-client)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b6c0-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b6c0-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b6c0-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6b6c0-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6b6c0-134">Dienst "zugewunverschlüsseltedtraffic" \_</span><span class="sxs-lookup"><span data-stu-id="6b6c0-134">AllowUnencryptedTraffic\_Service</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowunencryptedtraffic-service)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b6c0-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b6c0-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b6c0-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6b6c0-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6b6c0-137">Disallowdigestauthentication</span><span class="sxs-lookup"><span data-stu-id="6b6c0-137">DisallowDigestAuthentication</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallowdigestauthentication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b6c0-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b6c0-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b6c0-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6b6c0-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6b6c0-140">Disallowaushandateauthenticationclient</span><span class="sxs-lookup"><span data-stu-id="6b6c0-140">DisallowNegotiateAuthenticationClient</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallownegotiateauthenticationclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b6c0-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b6c0-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b6c0-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6b6c0-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6b6c0-143">Disallowaushandateauthenticationservice</span><span class="sxs-lookup"><span data-stu-id="6b6c0-143">DisallowNegotiateAuthenticationService</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallownegotiateauthenticationservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b6c0-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b6c0-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b6c0-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6b6c0-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6b6c0-146">Disallowstoringofrunasanmelde Informationen</span><span class="sxs-lookup"><span data-stu-id="6b6c0-146">DisallowStoringOfRunAsCredentials</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallowstoringofrunascredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b6c0-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b6c0-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b6c0-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6b6c0-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6b6c0-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6b6c0-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b6c0-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b6c0-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b6c0-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b6c0-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b6c0-152">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6b6c0-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6b6c0-153">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6b6c0-153">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b6c0-154">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b6c0-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b6c0-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b6c0-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b6c0-156">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6b6c0-156">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6b6c0-157">Specifychannelbindingdekenhardeninglevel</span><span class="sxs-lookup"><span data-stu-id="6b6c0-157">SpecifyChannelBindingTokenHardeningLevel</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-specifychannelbindingtokenhardeninglevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b6c0-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b6c0-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b6c0-159">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6b6c0-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6b6c0-160">TrustedHosts</span><span class="sxs-lookup"><span data-stu-id="6b6c0-160">TrustedHosts</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-trustedhosts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b6c0-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b6c0-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b6c0-162">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6b6c0-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6b6c0-163">Turnoncompatibilityhttplistener</span><span class="sxs-lookup"><span data-stu-id="6b6c0-163">TurnOnCompatibilityHTTPListener</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-turnoncompatibilityhttplistener)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b6c0-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b6c0-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b6c0-165">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6b6c0-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6b6c0-166">Turnoncompatibilityhttpslistener</span><span class="sxs-lookup"><span data-stu-id="6b6c0-166">TurnOnCompatibilityHTTPSListener</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-turnoncompatibilityhttpslistener)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b6c0-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6b6c0-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b6c0-168">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6b6c0-168">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6b6c0-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b6c0-169">Requirements</span></span>



| <span data-ttu-id="6b6c0-170">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b6c0-170">Requirement</span></span> | <span data-ttu-id="6b6c0-171">Wert</span><span class="sxs-lookup"><span data-stu-id="6b6c0-171">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b6c0-172">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b6c0-172">Minimum supported client</span></span><br/> | <span data-ttu-id="6b6c0-173">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b6c0-173">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6b6c0-174">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b6c0-174">Minimum supported server</span></span><br/> | <span data-ttu-id="6b6c0-175">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6b6c0-175">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6b6c0-176">Namespace</span><span class="sxs-lookup"><span data-stu-id="6b6c0-176">Namespace</span></span><br/>                | <span data-ttu-id="6b6c0-177">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="6b6c0-177">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="6b6c0-178">MOF</span><span class="sxs-lookup"><span data-stu-id="6b6c0-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b6c0-179"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6b6c0-179"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b6c0-180">DLL</span><span class="sxs-lookup"><span data-stu-id="6b6c0-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b6c0-181"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b6c0-181"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

