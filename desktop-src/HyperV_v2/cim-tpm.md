---
description: Beschreibt ein Trusted Platform Module (TPM)-Gerät.
ms.assetid: c923106f-126e-4e7e-822a-2fb715bbbc26
title: CIM_TPM-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM
- CIM_TPM.TPMSpecMajorVersion
- CIM_TPM.TPMSpecMinorVersion
- CIM_TPM.TPMManafucturerMajorRevision
- CIM_TPM.TPMManufacturerMinorRevision
- CIM_TPM.TPMManufacturerInfo
- CIM_TPM.TPMManufacturerId
- CIM_TPM.TPMState
- CIM_TPM.TransitioningToTPMState
- CIM_TPM.AvailableRequestedTPMStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0f2d35d42e864a247ca042ec81813ff7d1ac5c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042074"
---
# <a name="cim_tpm-class"></a><span data-ttu-id="79813-103">CIM- \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="79813-103">CIM\_TPM class</span></span>

<span data-ttu-id="79813-104">Beschreibt ein Trusted Platform Module (TPM)-Gerät.</span><span class="sxs-lookup"><span data-stu-id="79813-104">Describes a Trusted Platform Module (TPM) device.</span></span>

## <a name="syntax"></a><span data-ttu-id="79813-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="79813-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.21.0"), UMLPackagePath("CIM::Device::TPM"), AMENDMENT]
class CIM_TPM : CIM_LogicalDevice
{
  uint32 TPMSpecMajorVersion;
  uint32 TPMSpecMinorVersion;
  uint32 TPMManafucturerMajorRevision;
  uint32 TPMManufacturerMinorRevision;
  string TPMManufacturerInfo;
  uint32 TPMManufacturerId;
  uint16 TPMState;
  uint16 TransitioningToTPMState = 12;
  uint16 AvailableRequestedTPMStates[];
};
```

## <a name="members"></a><span data-ttu-id="79813-106">Member</span><span class="sxs-lookup"><span data-stu-id="79813-106">Members</span></span>

<span data-ttu-id="79813-107">Die **CIM- \_ TPM** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="79813-107">The **CIM\_TPM** class has these types of members:</span></span>

-   [<span data-ttu-id="79813-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="79813-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="79813-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="79813-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="79813-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="79813-110">Methods</span></span>

<span data-ttu-id="79813-111">Die **CIM- \_ TPM** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="79813-111">The **CIM\_TPM** class has these methods.</span></span>



| <span data-ttu-id="79813-112">Methode</span><span class="sxs-lookup"><span data-stu-id="79813-112">Method</span></span>                                                         | <span data-ttu-id="79813-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79813-113">Description</span></span>                                                                                                             |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79813-114">**Changebesitzauth**</span><span class="sxs-lookup"><span data-stu-id="79813-114">**ChangeOwnerAuth**</span></span>](cim-tpm-changeownerauth.md)             | <span data-ttu-id="79813-115">Ändert die Besitzer Autorisierungs Anmelde Informationen eines TPM-Geräts.</span><span class="sxs-lookup"><span data-stu-id="79813-115">Changes the owner authorization credential of a TPM device.</span></span><br/>                                                  |
| [<span data-ttu-id="79813-116">**Requesttpmstatechange**</span><span class="sxs-lookup"><span data-stu-id="79813-116">**RequestTPMStateChange**</span></span>](cim-tpm-requesttpmstatechange.md) | <span data-ttu-id="79813-117">Fordert an, dass der Status des TPM in den im **requestedtpmstate** -Parameter angegebenen Wert geändert wird.</span><span class="sxs-lookup"><span data-stu-id="79813-117">Requests that the state of the TPM be changed to the value specified in the **RequestedTPMState** parameter.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="79813-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="79813-118">Properties</span></span>

<span data-ttu-id="79813-119">Die **CIM- \_ TPM** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="79813-119">The **CIM\_TPM** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="79813-120">**Availablerequestedtpmstates**</span><span class="sxs-lookup"><span data-stu-id="79813-120">**AvailableRequestedTPMStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79813-121">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="79813-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="79813-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="79813-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79813-123">Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ TPM**".**Requesttpmstatechange**, CIM \_ tpmfunktionen. requestedtpmstatesupported ")</span><span class="sxs-lookup"><span data-stu-id="79813-123">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_TPM**.**RequestTPMStateChange**, CIM\_TPMCapabilities.RequestedTPMStatesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="79813-124">Die möglichen Werte für den *requestedtpmstate* -Parameter der [**requesttpmstatechange**](cim-tpm-requesttpmstatechange.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="79813-124">The possible values for the *RequestedTPMState* parameter of the [**RequestTPMStateChange**](cim-tpm-requesttpmstatechange.md) method.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79813-125">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="79813-125">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="79813-126">**S1 aktiviert-aktiv** (2)</span><span class="sxs-lookup"><span data-stu-id="79813-126">**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="79813-127">**S2 deaktiviert-aktiv** (3)</span><span class="sxs-lookup"><span data-stu-id="79813-127">**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="79813-128">**S3 aktiviert-inaktiv** (4)</span><span class="sxs-lookup"><span data-stu-id="79813-128">**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="79813-129">**S4 deaktiviert-inaktiv** (5)</span><span class="sxs-lookup"><span data-stu-id="79813-129">**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="79813-130">**S5 aktiviert, aktiv/nicht im Besitz** (6)</span><span class="sxs-lookup"><span data-stu-id="79813-130">**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="79813-131">**S6 deaktiviert, aktiv/nicht im Besitz** (7)</span><span class="sxs-lookup"><span data-stu-id="79813-131">**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="79813-132">**S7 aktiviert, inaktiv** (8)</span><span class="sxs-lookup"><span data-stu-id="79813-132">**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="79813-133">**S8 deaktiviert, inaktiv-nicht im Besitz** (9)</span><span class="sxs-lookup"><span data-stu-id="79813-133">**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="79813-134">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="79813-134">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="79813-135">**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="79813-135">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79813-136">**Tpmmanafucturermajorrevision**</span><span class="sxs-lookup"><span data-stu-id="79813-136">**TPMManafucturerMajorRevision**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79813-137">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79813-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79813-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="79813-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79813-139">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM". TCG \| Part 2 v1dot2 \| section 5,3 \| Version \| revmajor ")</span><span class="sxs-lookup"><span data-stu-id="79813-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|revMajor")</span></span>
</dt> </dl>

<span data-ttu-id="79813-140">Die Haupt Revision des TPM des Herstellers.</span><span class="sxs-lookup"><span data-stu-id="79813-140">The manufacturer major revision of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="79813-141">**Tpmmanufacturerid**</span><span class="sxs-lookup"><span data-stu-id="79813-141">**TPMManufacturerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79813-142">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79813-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79813-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="79813-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79813-144">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM". TCG \| Part 2 v1dot2 \| section 21,6 \| TPM \_ Cap \_ Version \_ Info \| tpmvendorid ")</span><span class="sxs-lookup"><span data-stu-id="79813-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 21.6\|TPM\_CAP\_VERSION\_INFO\|tpmVendorID")</span></span>
</dt> </dl>

<span data-ttu-id="79813-145">Die TPM-Hersteller-ID.</span><span class="sxs-lookup"><span data-stu-id="79813-145">The TPM manufacturer ID.</span></span>

</dd> <dt>

<span data-ttu-id="79813-146">**Tpmmanufacturerinfo**</span><span class="sxs-lookup"><span data-stu-id="79813-146">**TPMManufacturerInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79813-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="79813-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79813-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="79813-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79813-149">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM". TCG \| Part 2 v 1.2. TCG \| section 21,6 \| TPM \_ Cap \_ Version \_ Info \| vendorspecific ")</span><span class="sxs-lookup"><span data-stu-id="79813-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1.2.TCG\|Section 21.6\|TPM\_CAP\_VERSION\_INFO\|vendorSpecific")</span></span>
</dt> </dl>

<span data-ttu-id="79813-150">Die zusätzlichen Informationen, die vom TPM-Hersteller definiert werden.</span><span class="sxs-lookup"><span data-stu-id="79813-150">The additional information defined by the TPM manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="79813-151">**Tpmmanufacturerminorrevision**</span><span class="sxs-lookup"><span data-stu-id="79813-151">**TPMManufacturerMinorRevision**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79813-152">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79813-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79813-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="79813-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79813-154">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM". TCG \| Part 2 v1dot2 \| Abschnitt 5,3 \| Version \| revminor ")</span><span class="sxs-lookup"><span data-stu-id="79813-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|revMinor")</span></span>
</dt> </dl>

<span data-ttu-id="79813-155">Die neben Version des TPM des Herstellers.</span><span class="sxs-lookup"><span data-stu-id="79813-155">The manufacturer minor revision of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="79813-156">**Tpmspecmajorversion**</span><span class="sxs-lookup"><span data-stu-id="79813-156">**TPMSpecMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79813-157">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79813-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79813-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="79813-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79813-159">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM". TCG \| Part 2 v1dot2 \| Abschnitt 5,3 \| Version \| Major "," TSS. TCG \| Level 1 v 1.2, \| Abschnitt 2.3.2.18 ")</span><span class="sxs-lookup"><span data-stu-id="79813-159">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|major", "TSS.TCG\|Level 1 v1.2\|Section 2.3.2.18")</span></span>
</dt> </dl>

<span data-ttu-id="79813-160">Die Hauptversion des TPM.</span><span class="sxs-lookup"><span data-stu-id="79813-160">The major version of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="79813-161">**Tpmspecminorversion**</span><span class="sxs-lookup"><span data-stu-id="79813-161">**TPMSpecMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79813-162">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79813-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79813-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="79813-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79813-164">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM". TCG \| Part 2 v1dot2 \| Abschnitt 5,3 \| Version \| Minor "," TSS. TCG \| Level 1 v 1.2, \| Abschnitt 2.3.2.18 ")</span><span class="sxs-lookup"><span data-stu-id="79813-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|minor", "TSS.TCG\|Level 1 v1.2\|Section 2.3.2.18")</span></span>
</dt> </dl>

<span data-ttu-id="79813-165">Die neben Version des TPM.</span><span class="sxs-lookup"><span data-stu-id="79813-165">The minor version of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="79813-166">**Tpmstate**</span><span class="sxs-lookup"><span data-stu-id="79813-166">**TPMState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79813-167">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79813-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79813-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="79813-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79813-169">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM". TCG \| Part 1 v1dot2 \| Abschnitt 9,4 "," TPM. TCG \| Part 2 v1dot2 \| section 7,1 \| TPM \_ permanente \_ Flags "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ TPM**".**Requesttpmstatechange**","**CIM \_ TPM**.**Transitioningtotpmstate**")</span><span class="sxs-lookup"><span data-stu-id="79813-169">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 1 v1dot2\|Section 9.4", "TPM.TCG\|Part 2 v1dot2\|Section 7.1\|TPM\_PERMANENT\_FLAGS"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_TPM**.**RequestTPMStateChange**", "**CIM\_TPM**.**TransitioningToTPMState**")</span></span>
</dt> </dl>

<span data-ttu-id="79813-170">Der Betriebsstatus des TPM.</span><span class="sxs-lookup"><span data-stu-id="79813-170">The operational state of the TPM.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79813-171">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="79813-171">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="79813-172">**S1 aktiviert-aktiv** (2)</span><span class="sxs-lookup"><span data-stu-id="79813-172">**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="79813-173">**S2 deaktiviert-aktiv** (3)</span><span class="sxs-lookup"><span data-stu-id="79813-173">**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="79813-174">**S3 aktiviert-inaktiv** (4)</span><span class="sxs-lookup"><span data-stu-id="79813-174">**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="79813-175">**S4 deaktiviert-inaktiv** (5)</span><span class="sxs-lookup"><span data-stu-id="79813-175">**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="79813-176">**S5 aktiviert, aktiv/nicht im Besitz** (6)</span><span class="sxs-lookup"><span data-stu-id="79813-176">**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="79813-177">**S6 deaktiviert, aktiv/nicht im Besitz** (7)</span><span class="sxs-lookup"><span data-stu-id="79813-177">**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="79813-178">**S7 aktiviert, inaktiv** (8)</span><span class="sxs-lookup"><span data-stu-id="79813-178">**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="79813-179">**S8 deaktiviert, inaktiv-nicht im Besitz** (9)</span><span class="sxs-lookup"><span data-stu-id="79813-179">**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="79813-180">**Nicht zutreffend** (10)</span><span class="sxs-lookup"><span data-stu-id="79813-180">**Not Applicable** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="79813-181">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="79813-181">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="79813-182">**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="79813-182">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79813-183">**Transitioningtotpmstate**</span><span class="sxs-lookup"><span data-stu-id="79813-183">**TransitioningToTPMState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79813-184">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79813-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79813-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="79813-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79813-186">Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ TPM**".**Requesttpmstatechange**","**CIM \_ TPM**.**Tpmstate**")</span><span class="sxs-lookup"><span data-stu-id="79813-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_TPM**.**RequestTPMStateChange**", "**CIM\_TPM**.**TPMState**")</span></span>
</dt> </dl>

<span data-ttu-id="79813-187">Der Zielzustand, in den das TPM übergeht.</span><span class="sxs-lookup"><span data-stu-id="79813-187">The target state to which the TPM is transitioning.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79813-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="79813-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="79813-189"><span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>**S1 aktiviert-aktiv** (2)</span><span class="sxs-lookup"><span data-stu-id="79813-189"><span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="79813-190"><span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>**S2 deaktiviert-aktiv** (3)</span><span class="sxs-lookup"><span data-stu-id="79813-190"><span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="79813-191"><span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>**S3 aktiviert-inaktiv** (4)</span><span class="sxs-lookup"><span data-stu-id="79813-191"><span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="79813-192"><span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>**S4 deaktiviert-inaktiv** (5)</span><span class="sxs-lookup"><span data-stu-id="79813-192"><span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="79813-193"><span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>**S5 aktiviert, aktiv/nicht im Besitz** (6)</span><span class="sxs-lookup"><span data-stu-id="79813-193"><span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="79813-194"><span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>**S6 deaktiviert, aktiv/nicht im Besitz** (7)</span><span class="sxs-lookup"><span data-stu-id="79813-194"><span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="79813-195"><span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>**S7 aktiviert, inaktiv** (8)</span><span class="sxs-lookup"><span data-stu-id="79813-195"><span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="79813-196"><span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>**S8 deaktiviert, inaktiv-nicht im Besitz** (9)</span><span class="sxs-lookup"><span data-stu-id="79813-196"><span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="79813-197"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (10)</span><span class="sxs-lookup"><span data-stu-id="79813-197"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="79813-198"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**Keine Änderung** (11)</span><span class="sxs-lookup"><span data-stu-id="79813-198"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**No Change** (11)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="79813-199">(12)</span><span class="sxs-lookup"><span data-stu-id="79813-199">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="79813-200"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="79813-200"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="79813-201"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="79813-201"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="79813-202"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="79813-202"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="79813-203">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79813-203">Requirements</span></span>



| <span data-ttu-id="79813-204">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79813-204">Requirement</span></span> | <span data-ttu-id="79813-205">Wert</span><span class="sxs-lookup"><span data-stu-id="79813-205">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79813-206">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79813-206">Minimum supported client</span></span><br/> | <span data-ttu-id="79813-207">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79813-207">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="79813-208">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79813-208">Minimum supported server</span></span><br/> | <span data-ttu-id="79813-209">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="79813-209">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="79813-210">Namespace</span><span class="sxs-lookup"><span data-stu-id="79813-210">Namespace</span></span><br/>                | <span data-ttu-id="79813-211">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="79813-211">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="79813-212">MOF</span><span class="sxs-lookup"><span data-stu-id="79813-212">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79813-213"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="79813-213"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="79813-214">DLL</span><span class="sxs-lookup"><span data-stu-id="79813-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79813-215"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="79813-215"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="79813-216">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79813-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79813-217">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="79813-217">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

