---
title: MDM_Policy_Result01_Accounts02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ Accounts02-Klasse stellt Richtlinien für Konten dar.
ms.assetid: 581d63de-6ea8-4c4a-8b94-06228ed07371
keywords:
- MDM_Policy_Result01_Accounts02-Klasse
- MDM_Policy_Result01_Accounts02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Accounts02
- MDM_Policy_Result01_Accounts02.InstanceID
- MDM_Policy_Result01_Accounts02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e5c240f9cd4d3703122c0ea051f35ec8326e2df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741665"
---
# <a name="mdm_policy_result01_accounts02-class"></a><span data-ttu-id="ca73b-105">MDM- \_ Richtlinie \_ Result01 \_ Accounts02-Klasse</span><span class="sxs-lookup"><span data-stu-id="ca73b-105">MDM\_Policy\_Result01\_Accounts02 class</span></span>

<span data-ttu-id="ca73b-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="ca73b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ca73b-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="ca73b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ca73b-108">Die **MDM- \_ Richtlinie \_ Result01 \_ Accounts02** -Klasse stellt Richtlinien für Konten dar.</span><span class="sxs-lookup"><span data-stu-id="ca73b-108">The **MDM\_Policy\_Result01\_Accounts02** class represents policies related to accounts.</span></span>

<span data-ttu-id="ca73b-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="ca73b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca73b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca73b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Accounts02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMicrosoftAccountConnection;
  sint32 AllowMicrosoftAccountSignInAssistant;
  sint32 AllowAddingNonMicrosoftAccountsManually;
  string DomainNamesForEmailSync;
};
```

## <a name="members"></a><span data-ttu-id="ca73b-111">Member</span><span class="sxs-lookup"><span data-stu-id="ca73b-111">Members</span></span>

<span data-ttu-id="ca73b-112">Die **MDM- \_ Richtlinie \_ Result01 \_ Accounts02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ca73b-112">The **MDM\_Policy\_Result01\_Accounts02** class has these types of members:</span></span>

-   [<span data-ttu-id="ca73b-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ca73b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ca73b-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ca73b-114">Properties</span></span>

<span data-ttu-id="ca73b-115">Die **MDM- \_ Richtlinie \_ Result01 \_ Accounts02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ca73b-115">The **MDM\_Policy\_Result01\_Accounts02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ca73b-116">Allowaddingnonmicrosoftaccounungsmanuell</span><span class="sxs-lookup"><span data-stu-id="ca73b-116">AllowAddingNonMicrosoftAccountsManually</span></span>](/windows/client-management/mdm/policy-csp-accounts#accounts-allowaddingnonmicrosoftaccountsmanually)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca73b-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca73b-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca73b-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ca73b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca73b-119">Allowmicrosoftaccountconnection</span><span class="sxs-lookup"><span data-stu-id="ca73b-119">AllowMicrosoftAccountConnection</span></span>](/windows/client-management/mdm/policy-csp-accounts#accounts-allowmicrosoftaccountconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca73b-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca73b-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca73b-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ca73b-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ca73b-122">Allowmicrosoftaccountsigninassistant</span><span class="sxs-lookup"><span data-stu-id="ca73b-122">AllowMicrosoftAccountSignInAssistant</span></span>](/windows/client-management/mdm/policy-csp-accounts#accounts-allowmicrosoftaccountsigninassistant)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca73b-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ca73b-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca73b-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ca73b-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ca73b-125">Domainnamesforemailsync</span><span class="sxs-lookup"><span data-stu-id="ca73b-125">DomainNamesForEmailSync</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca73b-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ca73b-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca73b-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ca73b-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ca73b-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ca73b-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca73b-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ca73b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca73b-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ca73b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca73b-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ca73b-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ca73b-132">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="ca73b-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="ca73b-133">Bei dieser Klasse ist die Zeichenfolge "Accounts".</span><span class="sxs-lookup"><span data-stu-id="ca73b-133">For this class, the string is "Accounts".</span></span>

</dd> <dt>

<span data-ttu-id="ca73b-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ca73b-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca73b-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ca73b-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca73b-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ca73b-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca73b-137">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ca73b-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ca73b-138">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="ca73b-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="ca73b-139">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/result".</span><span class="sxs-lookup"><span data-stu-id="ca73b-139">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca73b-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca73b-140">Requirements</span></span>



| <span data-ttu-id="ca73b-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca73b-141">Requirement</span></span> | <span data-ttu-id="ca73b-142">Wert</span><span class="sxs-lookup"><span data-stu-id="ca73b-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca73b-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ca73b-143">Minimum supported client</span></span><br/> | <span data-ttu-id="ca73b-144">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ca73b-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ca73b-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ca73b-145">Minimum supported server</span></span><br/> | <span data-ttu-id="ca73b-146">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ca73b-146">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ca73b-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="ca73b-147">Namespace</span></span><br/>                | <span data-ttu-id="ca73b-148">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="ca73b-148">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="ca73b-149">MOF</span><span class="sxs-lookup"><span data-stu-id="ca73b-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca73b-150"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ca73b-150"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca73b-151">DLL</span><span class="sxs-lookup"><span data-stu-id="ca73b-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca73b-152"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca73b-152"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca73b-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca73b-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca73b-154">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="ca73b-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

