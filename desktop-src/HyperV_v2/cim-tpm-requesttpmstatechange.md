---
description: Fordert an, dass der Status des TPM in den im requestedtpmstate-Parameter angegebenen Wert geändert wird.
ms.assetid: 7ad8bf4e-6263-45d5-8f33-fb842bbf1f1a
title: Requesttpmstatechange-Methode der CIM_TPM-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.RequestTPMStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 39bded1a43dd547780c3924f3af9c37cfc79aa1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959406"
---
# <a name="requesttpmstatechange-method-of-the-cim_tpm-class"></a><span data-ttu-id="936bf-103">Requesttpmstatechange-Methode der CIM \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="936bf-103">RequestTPMStateChange method of the CIM\_TPM class</span></span>

<span data-ttu-id="936bf-104">Fordert an, dass der Status des TPM in den im *requestedtpmstate* -Parameter angegebenen Wert geändert wird.</span><span class="sxs-lookup"><span data-stu-id="936bf-104">Requests that the state of the TPM be changed to the value specified in the *RequestedTPMState* parameter.</span></span> <span data-ttu-id="936bf-105">Wenn der Methodenaufruf erfolgreich abgeschlossen wurde, muss die **tpmstate** -Eigenschaft gleich dem **requestedtpmstate** -Parameter sein.</span><span class="sxs-lookup"><span data-stu-id="936bf-105">If the method invocation completes successfully, the **TPMState** property shall be equal to the **RequestedTPMState** parameter.</span></span> <span data-ttu-id="936bf-106">Wenn Sie die **requesttpmstatechange** -Methode mehrmals aufrufen, kann dies dazu führen, dass frühere Anforderungen überschrieben werden oder verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="936bf-106">Invoking the **RequestTPMStateChange** method multiple times could result in earlier requests being overwritten or lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="936bf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="936bf-107">Syntax</span></span>


```mof
uint32 RequestTPMStateChange(
  [in]  uint16              RequestedTPMState,
  [in]  string              AuthorizationToken,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="936bf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="936bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="936bf-109">*Requestedtpmstate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="936bf-109">*RequestedTPMState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="936bf-110">Der angeforderte TPM-Status.</span><span class="sxs-lookup"><span data-stu-id="936bf-110">The requested TPM states.</span></span>

<dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="936bf-111">**S1 aktiviert-aktiv** (2)</span><span class="sxs-lookup"><span data-stu-id="936bf-111">**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="936bf-112">**S2 deaktiviert-aktiv** (3)</span><span class="sxs-lookup"><span data-stu-id="936bf-112">**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="936bf-113">**S3 aktiviert-inaktiv** (4)</span><span class="sxs-lookup"><span data-stu-id="936bf-113">**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="936bf-114">**S4 deaktiviert-inaktiv** (5)</span><span class="sxs-lookup"><span data-stu-id="936bf-114">**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="936bf-115">**S5 aktiviert, aktiv/nicht im Besitz** (6)</span><span class="sxs-lookup"><span data-stu-id="936bf-115">**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="936bf-116">**S6 deaktiviert, aktiv/nicht im Besitz** (7)</span><span class="sxs-lookup"><span data-stu-id="936bf-116">**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="936bf-117">**S7 aktiviert, inaktiv** (8)</span><span class="sxs-lookup"><span data-stu-id="936bf-117">**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="936bf-118">**S8 deaktiviert, inaktiv-nicht im Besitz** (9)</span><span class="sxs-lookup"><span data-stu-id="936bf-118">**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="936bf-119">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="936bf-119">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="936bf-120">**Anbieter reserviert** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="936bf-120">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="936bf-121">*Authorizationtoken* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="936bf-121">*AuthorizationToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="936bf-122">Autorisierungs Token, das möglicherweise erforderlich ist, damit die Aktion wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="936bf-122">Authorization token that may be required for the action to take effect.</span></span> <span data-ttu-id="936bf-123">Der *authorizationtoken* -Parameter ist möglicherweise erforderlich, um eine physische Präsenz einzurichten, oder um die Besitzer Authentifizierung, das von TCG definierte Besitzer Autorisierungs Kennwort, zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="936bf-123">The *AuthorizationToken* parameter may be required to establish Physical Presence, or to pass the OwnerAuth, the TCG defined owner authorization password.</span></span> <span data-ttu-id="936bf-124">Im Fall von "Besitzer Authentifizierung" ist möglicherweise der CIM " \_ sharedcredential" mit dem Wert "CIM \_ sharedcredential. Secret" erforderlich, der nicht NULL ist.</span><span class="sxs-lookup"><span data-stu-id="936bf-124">In the case of OwnerAuth, the CIM\_SharedCredential with non-null value of the CIM\_SharedCredential.Secret may be required.</span></span> <span data-ttu-id="936bf-125">Die CIM \_ sharedcredential. algorithmuseigenschaft kann auch basierend auf der Eigenschaft CIM \_ tpmfunktionen. supportedpasswordalgorithms angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="936bf-125">The CIM\_SharedCredential.Algorithm property may also be specified based on the property CIM\_TPMCapabilities.SupportedPasswordAlgorithms.</span></span>

</dd> <dt>

<span data-ttu-id="936bf-126">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="936bf-126">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="936bf-127">Kann einen Verweis auf den erstellten [**CIM- \_ bettejob**](cim-concretejob.md) enthalten, um den durch den Methodenaufruf initiierten Zustandsübergang zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="936bf-127">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="936bf-128">*Timeoutperiod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="936bf-128">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="936bf-129">Ein Timeout Zeitraum, der die maximale Zeitspanne angibt, die der Client für den Übergang in den neuen Zustand erwartet.</span><span class="sxs-lookup"><span data-stu-id="936bf-129">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="936bf-130">Zum Angeben des *timeoutperiod* muss das Intervall Format verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="936bf-130">The interval format must be used to specify the *TimeoutPeriod*.</span></span> <span data-ttu-id="936bf-131">Der Wert 0 oder ein NULL-Parameter gibt an, dass der Client keine Zeitanforderungen für den Übergang hat.</span><span class="sxs-lookup"><span data-stu-id="936bf-131">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="936bf-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="936bf-132">Return value</span></span>

<span data-ttu-id="936bf-133">Bei Erfolg wird 0 oder 4096 zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="936bf-133">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="936bf-134">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="936bf-134">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="936bf-135">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="936bf-135">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="936bf-136">**Unbekannter oder nicht** angegebener Fehler (2)</span><span class="sxs-lookup"><span data-stu-id="936bf-136">**Unknown or Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="936bf-137">**Kann nicht innerhalb des Timeout Zeitraums** (3) beendet werden.</span><span class="sxs-lookup"><span data-stu-id="936bf-137">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="936bf-138">Fehler **(4** )</span><span class="sxs-lookup"><span data-stu-id="936bf-138">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="936bf-139">**Ungültiger Parameter** (5)</span><span class="sxs-lookup"><span data-stu-id="936bf-139">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="936bf-140">**In Gebrauch** (6)</span><span class="sxs-lookup"><span data-stu-id="936bf-140">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="936bf-141">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="936bf-141">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="936bf-142">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="936bf-142">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="936bf-143">**Ungültiger Status Übergang** (4097).</span><span class="sxs-lookup"><span data-stu-id="936bf-143">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="936bf-144">**Verwendung des timeout-Parameters wird nicht unterstützt** (4098)</span><span class="sxs-lookup"><span data-stu-id="936bf-144">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="936bf-145">**Ausgelastet** (4099)</span><span class="sxs-lookup"><span data-stu-id="936bf-145">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="936bf-146">**Reservierte Methode** (4100.32767)</span><span class="sxs-lookup"><span data-stu-id="936bf-146">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="936bf-147">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="936bf-147">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="936bf-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="936bf-148">Requirements</span></span>



| <span data-ttu-id="936bf-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="936bf-149">Requirement</span></span> | <span data-ttu-id="936bf-150">Wert</span><span class="sxs-lookup"><span data-stu-id="936bf-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="936bf-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="936bf-151">Minimum supported client</span></span><br/> | <span data-ttu-id="936bf-152">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="936bf-152">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="936bf-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="936bf-153">Minimum supported server</span></span><br/> | <span data-ttu-id="936bf-154">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="936bf-154">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="936bf-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="936bf-155">Namespace</span></span><br/>                | <span data-ttu-id="936bf-156">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="936bf-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="936bf-157">MOF</span><span class="sxs-lookup"><span data-stu-id="936bf-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="936bf-158"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="936bf-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="936bf-159">DLL</span><span class="sxs-lookup"><span data-stu-id="936bf-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="936bf-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="936bf-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="936bf-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="936bf-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="936bf-162">**CIM- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="936bf-162">**CIM\_TPM**</span></span>](cim-tpm.md)
</dt> </dl>

 

 




