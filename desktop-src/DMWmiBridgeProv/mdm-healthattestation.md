---
title: MDM_HealthAttestation-Klasse
description: Die MDM \_ healthattestation-Klasse ermöglicht IT-Managern von Unternehmen, die Integrität verwalteter Geräte zu bewerten und Unternehmensrichtlinien Aktionen auszuführen.
ms.assetid: 64f40ccc-98f6-48d6-bcd4-793375e3dbfb
keywords:
- MDM_HealthAttestation-Klasse
- MDM_HealthAttestation-Klasse, beschrieben
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7f76af135e7eac09b3b104e924b26efbb359b256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476041"
---
# <a name="mdm_healthattestation-class"></a><span data-ttu-id="9d7fd-105">MDM \_ healthattestation-Klasse</span><span class="sxs-lookup"><span data-stu-id="9d7fd-105">MDM\_HealthAttestation class</span></span>

<span data-ttu-id="9d7fd-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9d7fd-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="9d7fd-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9d7fd-108">Die **MDM \_ healthattestation** -Klasse ermöglicht IT-Managern von Unternehmen, die Integrität verwalteter Geräte zu bewerten und Unternehmensrichtlinien Aktionen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-108">The **MDM\_HealthAttestation** class enables enterprise IT managers to assess the health of managed devices and take enterprise policy actions.</span></span>

<span data-ttu-id="9d7fd-109">Im folgenden finden Sie eine Liste der Funktionen, die vom healthattestation-CSP ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="9d7fd-109">The following is a list of functions performed by the HealthAttestation CSP:</span></span>

-   <span data-ttu-id="9d7fd-110">Sammelt Daten, die zum Überprüfen von Integritäts Zuständen von Geräten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-110">Collects data that is used in verifying a devices health states</span></span>
-   <span data-ttu-id="9d7fd-111">Weiterleitung der Daten an den Integritätsnachweisdienst (Health Attestation Service, HAS)</span><span class="sxs-lookup"><span data-stu-id="9d7fd-111">Forwards the data to the Health Attestation Service (HAS)</span></span>
-   <span data-ttu-id="9d7fd-112">Stellt das Integritäts Nachweis Zertifikat bereit, das von empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-112">Provisions the Health Attestation Certificate that it receives from HAS</span></span>
-   <span data-ttu-id="9d7fd-113">Bei der Anforderung leitet das Health Attestation-Zertifikat (von hat) und zugehörige Laufzeitinformationen zur Überprüfung an den MDM-Server weiter.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-113">Upon request, forwards the Health Attestation Certificate (received from HAS) and related runtime information to the MDM Server for verification</span></span>

<span data-ttu-id="9d7fd-114">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-114">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d7fd-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d7fd-115">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_HealthAttestation
{
  string  InstanceID;
  string  ParentID;
  sint32  Status;
  boolean ForceRetrieve;
  string  Certificate;
  string  Nonce;
  string  CorrelationID;
  sint32  TpmReadyStatus;
  sint32  MaxSupportedProtocolVersion;
  sint32  PreferredMaxProtocolVersion;
  sint32  CurrentProtocolVersion;
  string  HASEndpoint;
};
```

## <a name="members"></a><span data-ttu-id="9d7fd-116">Member</span><span class="sxs-lookup"><span data-stu-id="9d7fd-116">Members</span></span>

<span data-ttu-id="9d7fd-117">Die **MDM \_ healthattestation** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9d7fd-117">The **MDM\_HealthAttestation** class has these types of members:</span></span>

-   [<span data-ttu-id="9d7fd-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="9d7fd-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="9d7fd-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9d7fd-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9d7fd-120">Methoden</span><span class="sxs-lookup"><span data-stu-id="9d7fd-120">Methods</span></span>

<span data-ttu-id="9d7fd-121">Die **MDM \_ healthattestation** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-121">The **MDM\_HealthAttestation** class has these methods.</span></span>



| <span data-ttu-id="9d7fd-122">Methode</span><span class="sxs-lookup"><span data-stu-id="9d7fd-122">Method</span></span>                                                                 | <span data-ttu-id="9d7fd-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d7fd-123">Description</span></span>                                                                                  |
|:-----------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9d7fd-124">**Verifyhealthmethod**</span><span class="sxs-lookup"><span data-stu-id="9d7fd-124">**VerifyHealthMethod**</span></span>](mdm-healthattestation-verifyhealthmethod.md) | <span data-ttu-id="9d7fd-125">Methode, mit der das Gerät benachrichtigt wird, dass eine Integritäts Zertifikat Überprüfung vorbereitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-125">Method to notify the device to prepare a health certificate verification request.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9d7fd-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9d7fd-126">Properties</span></span>

<span data-ttu-id="9d7fd-127">Die **MDM \_ healthattestation** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-127">The **MDM\_HealthAttestation** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9d7fd-128">Certificate</span><span class="sxs-lookup"><span data-stu-id="9d7fd-128">Certificate</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d7fd-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9d7fd-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d7fd-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9d7fd-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9d7fd-131">**Qualifizierer: octetstring**</span><span class="sxs-lookup"><span data-stu-id="9d7fd-131">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d7fd-132">CorrelationID</span><span class="sxs-lookup"><span data-stu-id="9d7fd-132">CorrelationID</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d7fd-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9d7fd-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d7fd-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9d7fd-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9d7fd-135">**Currentprotocolversion**</span><span class="sxs-lookup"><span data-stu-id="9d7fd-135">**CurrentProtocolVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d7fd-136">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9d7fd-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d7fd-137">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9d7fd-137">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9d7fd-138">TBD</span><span class="sxs-lookup"><span data-stu-id="9d7fd-138">TBD</span></span>

</dd> <dt>

[<span data-ttu-id="9d7fd-139">Forceretrieve</span><span class="sxs-lookup"><span data-stu-id="9d7fd-139">ForceRetrieve</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d7fd-140">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="9d7fd-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9d7fd-141">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9d7fd-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d7fd-142">Hasendpoint</span><span class="sxs-lookup"><span data-stu-id="9d7fd-142">HASEndpoint</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d7fd-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9d7fd-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d7fd-144">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9d7fd-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9d7fd-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9d7fd-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d7fd-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9d7fd-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d7fd-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d7fd-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d7fd-148">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9d7fd-148">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9d7fd-149">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-149">Identifies the name of the parent node.</span></span> <span data-ttu-id="9d7fd-150">Für diese Klasse ist die Zeichenfolge "healthattestation".</span><span class="sxs-lookup"><span data-stu-id="9d7fd-150">For this class, the string is "HealthAttestation".</span></span>

</dd> <dt>

<span data-ttu-id="9d7fd-151">**Maxsupportedprotocolversion**</span><span class="sxs-lookup"><span data-stu-id="9d7fd-151">**MaxSupportedProtocolVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d7fd-152">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9d7fd-152">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d7fd-153">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9d7fd-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9d7fd-154">TBD</span><span class="sxs-lookup"><span data-stu-id="9d7fd-154">TBD</span></span>

</dd> <dt>

[<span data-ttu-id="9d7fd-155">Nonce</span><span class="sxs-lookup"><span data-stu-id="9d7fd-155">Nonce</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d7fd-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9d7fd-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d7fd-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9d7fd-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9d7fd-158">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9d7fd-158">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d7fd-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9d7fd-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d7fd-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d7fd-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d7fd-161">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9d7fd-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9d7fd-162">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="9d7fd-162">Describes the full path to the parent node.</span></span> <span data-ttu-id="9d7fd-163">Für diese Klasse ist die Zeichenfolge "./Vendor/msft/".</span><span class="sxs-lookup"><span data-stu-id="9d7fd-163">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

<span data-ttu-id="9d7fd-164">**Preferredmaxprotocolversion**</span><span class="sxs-lookup"><span data-stu-id="9d7fd-164">**PreferredMaxProtocolVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d7fd-165">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9d7fd-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d7fd-166">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9d7fd-166">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9d7fd-167">TBD</span><span class="sxs-lookup"><span data-stu-id="9d7fd-167">TBD</span></span>

</dd> <dt>

[<span data-ttu-id="9d7fd-168">Status</span><span class="sxs-lookup"><span data-stu-id="9d7fd-168">Status</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d7fd-169">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9d7fd-169">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d7fd-170">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9d7fd-170">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d7fd-171">TPM-Status</span><span class="sxs-lookup"><span data-stu-id="9d7fd-171">TpmReadyStatus</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d7fd-172">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9d7fd-172">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d7fd-173">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="9d7fd-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d7fd-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d7fd-174">Requirements</span></span>



| <span data-ttu-id="9d7fd-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d7fd-175">Requirement</span></span> | <span data-ttu-id="9d7fd-176">Wert</span><span class="sxs-lookup"><span data-stu-id="9d7fd-176">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d7fd-177">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d7fd-177">Minimum supported client</span></span><br/> | <span data-ttu-id="9d7fd-178">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d7fd-178">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9d7fd-179">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d7fd-179">Minimum supported server</span></span><br/> | <span data-ttu-id="9d7fd-180">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9d7fd-180">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9d7fd-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d7fd-181">Namespace</span></span><br/>                | <span data-ttu-id="9d7fd-182">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="9d7fd-182">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="9d7fd-183">MOF</span><span class="sxs-lookup"><span data-stu-id="9d7fd-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d7fd-184"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9d7fd-184"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d7fd-185">DLL</span><span class="sxs-lookup"><span data-stu-id="9d7fd-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d7fd-186"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d7fd-186"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d7fd-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d7fd-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d7fd-188">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="9d7fd-188">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

