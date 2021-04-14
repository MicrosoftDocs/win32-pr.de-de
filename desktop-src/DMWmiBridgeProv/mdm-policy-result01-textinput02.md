---
title: MDM_Policy_Result01_TextInput02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ TextInput02-Klasse stellt die verfügbaren Texteingabe Richtlinien dar.
ms.assetid: d0ab2d69-6d43-410e-936a-cb87a521d5f3
keywords:
- MDM_Policy_Result01_TextInput02-Klasse
- MDM_Policy_Result01_TextInput02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_TextInput02
- MDM_Policy_Result01_TextInput02.InstanceID
- MDM_Policy_Result01_TextInput02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a0c02c2afe70f3e7122de0c3d888c42ac179317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476263"
---
# <a name="mdm_policy_result01_textinput02-class"></a><span data-ttu-id="ed0b5-105">MDM- \_ Richtlinie \_ Result01 \_ TextInput02-Klasse</span><span class="sxs-lookup"><span data-stu-id="ed0b5-105">MDM\_Policy\_Result01\_TextInput02 class</span></span>

<span data-ttu-id="ed0b5-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="ed0b5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ed0b5-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="ed0b5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ed0b5-108">Die **MDM- \_ Richtlinie \_ Result01 \_ TextInput02** -Klasse stellt die verfügbaren Texteingabe Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="ed0b5-108">The **MDM\_Policy\_Result01\_TextInput02** class represents the text input policies available.</span></span>

<span data-ttu-id="ed0b5-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="ed0b5-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed0b5-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed0b5-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_TextInput02
{
  string InstanceID;
  string ParentID;
  sint32 AllowIMENetworkAccess;
  sint32 AllowIMELogging;
  sint32 AllowJapaneseNonPublishingStandardGlyph;
  sint32 AllowJapaneseIVSCharacters;
  sint32 AllowJapaneseUserDictionary;
  sint32 AllowKeyboardTextSuggestions;
  sint32 AllowJapaneseIMESurrogatePairCharacters;
  sint32 ExcludeJapaneseIMEExceptShiftJIS;
  sint32 ExcludeJapaneseIMEExceptJIS0208;
  sint32 ExcludeJapaneseIMEExceptJIS0208andEUDC;
  sint32 AllowLanguageFeaturesUninstall;
  sint32 AllowInputPanel;
};
```

## <a name="members"></a><span data-ttu-id="ed0b5-111">Member</span><span class="sxs-lookup"><span data-stu-id="ed0b5-111">Members</span></span>

<span data-ttu-id="ed0b5-112">Die **MDM- \_ Richtlinie \_ Result01 \_ TextInput02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ed0b5-112">The **MDM\_Policy\_Result01\_TextInput02** class has these types of members:</span></span>

-   [<span data-ttu-id="ed0b5-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ed0b5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ed0b5-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ed0b5-114">Properties</span></span>

<span data-ttu-id="ed0b5-115">Die **MDM- \_ Richtlinie \_ Result01 \_ TextInput02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ed0b5-115">The **MDM\_Policy\_Result01\_TextInput02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ed0b5-116">Zuordnung</span><span class="sxs-lookup"><span data-stu-id="ed0b5-116">AllowIMELogging</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowimelogging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed0b5-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ed0b5-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed0b5-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ed0b5-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed0b5-119">AllowIMENetworkAccess</span><span class="sxs-lookup"><span data-stu-id="ed0b5-119">AllowIMENetworkAccess</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowimenetworkaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed0b5-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ed0b5-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed0b5-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ed0b5-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed0b5-122">AllowInputPanel</span><span class="sxs-lookup"><span data-stu-id="ed0b5-122">AllowInputPanel</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowinputpanel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed0b5-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ed0b5-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed0b5-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ed0b5-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed0b5-125">AllowJapaneseIMESurrogatePairCharacters</span><span class="sxs-lookup"><span data-stu-id="ed0b5-125">AllowJapaneseIMESurrogatePairCharacters</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseimesurrogatepaircharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed0b5-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ed0b5-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed0b5-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ed0b5-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed0b5-128">AllowJapaneseIVSCharacters</span><span class="sxs-lookup"><span data-stu-id="ed0b5-128">AllowJapaneseIVSCharacters</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseivscharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed0b5-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ed0b5-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed0b5-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ed0b5-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed0b5-131">AllowJapaneseNonPublishingStandardGlyph</span><span class="sxs-lookup"><span data-stu-id="ed0b5-131">AllowJapaneseNonPublishingStandardGlyph</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapanesenonpublishingstandardglyph)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed0b5-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ed0b5-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed0b5-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ed0b5-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed0b5-134">AllowJapaneseUserDictionary</span><span class="sxs-lookup"><span data-stu-id="ed0b5-134">AllowJapaneseUserDictionary</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseuserdictionary)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed0b5-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ed0b5-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed0b5-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ed0b5-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed0b5-137">AllowKeyboardTextSuggestions</span><span class="sxs-lookup"><span data-stu-id="ed0b5-137">AllowKeyboardTextSuggestions</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowkeyboardtextsuggestions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed0b5-138">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ed0b5-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed0b5-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ed0b5-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed0b5-140">AllowLanguageFeaturesUninstall</span><span class="sxs-lookup"><span data-stu-id="ed0b5-140">AllowLanguageFeaturesUninstall</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowlanguagefeaturesuninstall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed0b5-141">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ed0b5-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed0b5-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ed0b5-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed0b5-143">ExcludeJapaneseIMEExceptJIS0208</span><span class="sxs-lookup"><span data-stu-id="ed0b5-143">ExcludeJapaneseIMEExceptJIS0208</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptjis0208)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed0b5-144">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ed0b5-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed0b5-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ed0b5-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed0b5-146">ExcludeJapaneseIMEExceptJIS0208andEUDC</span><span class="sxs-lookup"><span data-stu-id="ed0b5-146">ExcludeJapaneseIMEExceptJIS0208andEUDC</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptjis0208andeudc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed0b5-147">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ed0b5-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed0b5-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ed0b5-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed0b5-149">Exclude japaneseimeexceptshiftjis</span><span class="sxs-lookup"><span data-stu-id="ed0b5-149">ExcludeJapaneseIMEExceptShiftJIS</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptshiftjis)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed0b5-150">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ed0b5-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed0b5-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ed0b5-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ed0b5-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ed0b5-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed0b5-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ed0b5-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed0b5-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ed0b5-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed0b5-155">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ed0b5-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ed0b5-156">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="ed0b5-156">Identifies the name of the parent node.</span></span> <span data-ttu-id="ed0b5-157">Für diese Klasse ist die Zeichenfolge "TextInput".</span><span class="sxs-lookup"><span data-stu-id="ed0b5-157">For this class, the string is "TextInput"</span></span>

</dd> <dt>

<span data-ttu-id="ed0b5-158">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ed0b5-158">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed0b5-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ed0b5-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed0b5-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ed0b5-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed0b5-161">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ed0b5-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ed0b5-162">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="ed0b5-162">Describes the full path to the parent node.</span></span> <span data-ttu-id="ed0b5-163">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/result".</span><span class="sxs-lookup"><span data-stu-id="ed0b5-163">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed0b5-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed0b5-164">Requirements</span></span>



| <span data-ttu-id="ed0b5-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed0b5-165">Requirement</span></span> | <span data-ttu-id="ed0b5-166">Wert</span><span class="sxs-lookup"><span data-stu-id="ed0b5-166">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed0b5-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed0b5-167">Minimum supported client</span></span><br/> | <span data-ttu-id="ed0b5-168">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed0b5-168">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ed0b5-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed0b5-169">Minimum supported server</span></span><br/> | <span data-ttu-id="ed0b5-170">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ed0b5-170">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ed0b5-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="ed0b5-171">Namespace</span></span><br/>                | <span data-ttu-id="ed0b5-172">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="ed0b5-172">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="ed0b5-173">MOF</span><span class="sxs-lookup"><span data-stu-id="ed0b5-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed0b5-174"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ed0b5-174"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed0b5-175">DLL</span><span class="sxs-lookup"><span data-stu-id="ed0b5-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed0b5-176"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed0b5-176"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed0b5-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed0b5-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed0b5-178">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="ed0b5-178">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

