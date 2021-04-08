---
title: MDM_PassportForWork_PINComplexity03-Klasse
description: Die MDM \_ passportforwork \_ PINComplexity03-Klasse definiert die PIN-Komplexität für die Anmelde Informationen für Windows Hello for Business.
ms.assetid: 83dcf859-03da-4508-b809-bafd24dc8bd4
keywords:
- MDM_PassportForWork_PINComplexity03-Klasse
- MDM_PassportForWork_PINComplexity03-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_PassportForWork_PINComplexity03
- MDM_PassportForWork_PINComplexity03.InstanceID
- MDM_PassportForWork_PINComplexity03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a9d01cd152935a1daa0a9b0721ea27129e21934
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949685"
---
# <a name="mdm_passportforwork_pincomplexity03-class"></a><span data-ttu-id="948d8-105">MDM \_ passportforwork \_ PINComplexity03-Klasse</span><span class="sxs-lookup"><span data-stu-id="948d8-105">MDM\_PassportForWork\_PINComplexity03 class</span></span>

<span data-ttu-id="948d8-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="948d8-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="948d8-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="948d8-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="948d8-108">Die **MDM \_ passportforwork \_ PINComplexity03** -Klasse definiert die PIN-Komplexität für die Anmelde Informationen für Windows Hello for Business.</span><span class="sxs-lookup"><span data-stu-id="948d8-108">The **MDM\_PassportForWork\_PINComplexity03** class defines the PIN complexity for the logon credentials for Windows Hello for Business.</span></span>

<span data-ttu-id="948d8-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="948d8-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="948d8-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="948d8-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_PINComplexity03
{
  string InstanceID;
  string ParentID;
  sint32 MinimumPINLength;
  sint32 MaximumPINLength;
  sint32 UppercaseLetters;
  sint32 LowercaseLetters;
  sint32 SpecialCharacters;
  sint32 Digits;
  sint32 History;
  sint32 Expiration;
};
```

## <a name="members"></a><span data-ttu-id="948d8-111">Member</span><span class="sxs-lookup"><span data-stu-id="948d8-111">Members</span></span>

<span data-ttu-id="948d8-112">Die **MDM \_ passportforwork \_ PINComplexity03** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="948d8-112">The **MDM\_PassportForWork\_PINComplexity03** class has these types of members:</span></span>

-   [<span data-ttu-id="948d8-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="948d8-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="948d8-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="948d8-114">Properties</span></span>

<span data-ttu-id="948d8-115">Die **MDM \_ passportforwork \_ PINComplexity03** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="948d8-115">The **MDM\_PassportForWork\_PINComplexity03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="948d8-116">Treffern</span><span class="sxs-lookup"><span data-stu-id="948d8-116">Digits</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-digits)
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d8-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="948d8-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="948d8-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="948d8-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="948d8-119">Ablauf</span><span class="sxs-lookup"><span data-stu-id="948d8-119">Expiration</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-expiration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d8-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="948d8-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="948d8-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="948d8-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="948d8-122">History</span><span class="sxs-lookup"><span data-stu-id="948d8-122">History</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-history)
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d8-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="948d8-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="948d8-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="948d8-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="948d8-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="948d8-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d8-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="948d8-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="948d8-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="948d8-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="948d8-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="948d8-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="948d8-129">Stamm Knoten für PIN-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="948d8-129">Root node for PIN policies.</span></span>

</dd> <dt>

[<span data-ttu-id="948d8-130">Lowercaseletters</span><span class="sxs-lookup"><span data-stu-id="948d8-130">LowercaseLetters</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-lowercaseletters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d8-131">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="948d8-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="948d8-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="948d8-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="948d8-133">Maximumpinlength</span><span class="sxs-lookup"><span data-stu-id="948d8-133">MaximumPINLength</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-maximumpinlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d8-134">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="948d8-134">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="948d8-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="948d8-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="948d8-136">Minimumpinlength</span><span class="sxs-lookup"><span data-stu-id="948d8-136">MinimumPINLength</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-minimumpinlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d8-137">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="948d8-137">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="948d8-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="948d8-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="948d8-139">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="948d8-139">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d8-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="948d8-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="948d8-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="948d8-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="948d8-142">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="948d8-142">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="948d8-143">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="948d8-143">Describes the full path to the parent node.</span></span> <span data-ttu-id="948d8-144">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/PassPortForWork/*tenantid*/Policies".</span><span class="sxs-lookup"><span data-stu-id="948d8-144">For this class, the string is "./Vendor/MSFT/PassPortForWork/*TenantID*/Policies"</span></span>

</dd> <dt>

[<span data-ttu-id="948d8-145">Specialcharacter</span><span class="sxs-lookup"><span data-stu-id="948d8-145">SpecialCharacters</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-specialcharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d8-146">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="948d8-146">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="948d8-147">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="948d8-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="948d8-148">Uppercaseletters</span><span class="sxs-lookup"><span data-stu-id="948d8-148">UppercaseLetters</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-uppercaseletters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="948d8-149">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="948d8-149">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="948d8-150">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="948d8-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="948d8-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="948d8-151">Requirements</span></span>



| <span data-ttu-id="948d8-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="948d8-152">Requirement</span></span> | <span data-ttu-id="948d8-153">Wert</span><span class="sxs-lookup"><span data-stu-id="948d8-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="948d8-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="948d8-154">Minimum supported client</span></span><br/> | <span data-ttu-id="948d8-155">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="948d8-155">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="948d8-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="948d8-156">Minimum supported server</span></span><br/> | <span data-ttu-id="948d8-157">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="948d8-157">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="948d8-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="948d8-158">Namespace</span></span><br/>                | <span data-ttu-id="948d8-159">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="948d8-159">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="948d8-160">MOF</span><span class="sxs-lookup"><span data-stu-id="948d8-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="948d8-161"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="948d8-161"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="948d8-162">DLL</span><span class="sxs-lookup"><span data-stu-id="948d8-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="948d8-163"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="948d8-163"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="948d8-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="948d8-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="948d8-165">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="948d8-165">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

