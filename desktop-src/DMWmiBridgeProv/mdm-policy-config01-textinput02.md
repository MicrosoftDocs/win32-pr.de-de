---
title: MDM_Policy_Config01_TextInput02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ TextInput02-Klasse stellt die verfügbaren Texteingabe Richtlinien dar.
ms.assetid: e5a8d331-40ec-49f2-aedd-5941fe59092f
keywords:
- MDM_Policy_Config01_TextInput02-Klasse
- MDM_Policy_Config01_TextInput02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_TextInput02
- MDM_Policy_Config01_TextInput02.InstanceID
- MDM_Policy_Config01_TextInput02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f79d750973edf501ca292d042e04bf4dc27ef42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476920"
---
# <a name="mdm_policy_config01_textinput02-class"></a><span data-ttu-id="c6a02-105">MDM- \_ Richtlinie \_ Config01 \_ TextInput02-Klasse</span><span class="sxs-lookup"><span data-stu-id="c6a02-105">MDM\_Policy\_Config01\_TextInput02 class</span></span>

<span data-ttu-id="c6a02-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="c6a02-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c6a02-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="c6a02-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c6a02-108">Die **MDM- \_ Richtlinie \_ Config01 \_ TextInput02** -Klasse stellt die verfügbaren Texteingabe Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="c6a02-108">The **MDM\_Policy\_Config01\_TextInput02** class represents the text input policies available.</span></span>

<span data-ttu-id="c6a02-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c6a02-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6a02-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6a02-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_TextInput02
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

## <a name="members"></a><span data-ttu-id="c6a02-111">Member</span><span class="sxs-lookup"><span data-stu-id="c6a02-111">Members</span></span>

<span data-ttu-id="c6a02-112">Die **MDM- \_ Richtlinie \_ Config01 \_ TextInput02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c6a02-112">The **MDM\_Policy\_Config01\_TextInput02** class has these types of members:</span></span>

-   [<span data-ttu-id="c6a02-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c6a02-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c6a02-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c6a02-114">Properties</span></span>

<span data-ttu-id="c6a02-115">Die **MDM- \_ Richtlinie \_ Config01 \_ TextInput02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c6a02-115">The **MDM\_Policy\_Config01\_TextInput02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c6a02-116">Zuordnung</span><span class="sxs-lookup"><span data-stu-id="c6a02-116">AllowIMELogging</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowimelogging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6a02-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c6a02-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6a02-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c6a02-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c6a02-119">AllowIMENetworkAccess</span><span class="sxs-lookup"><span data-stu-id="c6a02-119">AllowIMENetworkAccess</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowimenetworkaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6a02-120">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c6a02-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6a02-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c6a02-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c6a02-122">AllowInputPanel</span><span class="sxs-lookup"><span data-stu-id="c6a02-122">AllowInputPanel</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowinputpanel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6a02-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c6a02-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6a02-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c6a02-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c6a02-125">AllowJapaneseIMESurrogatePairCharacters</span><span class="sxs-lookup"><span data-stu-id="c6a02-125">AllowJapaneseIMESurrogatePairCharacters</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseimesurrogatepaircharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6a02-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c6a02-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6a02-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c6a02-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c6a02-128">AllowJapaneseIVSCharacters</span><span class="sxs-lookup"><span data-stu-id="c6a02-128">AllowJapaneseIVSCharacters</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseivscharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6a02-129">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c6a02-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6a02-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c6a02-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c6a02-131">AllowJapaneseNonPublishingStandardGlyph</span><span class="sxs-lookup"><span data-stu-id="c6a02-131">AllowJapaneseNonPublishingStandardGlyph</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapanesenonpublishingstandardglyph)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6a02-132">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c6a02-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6a02-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c6a02-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c6a02-134">AllowJapaneseUserDictionary</span><span class="sxs-lookup"><span data-stu-id="c6a02-134">AllowJapaneseUserDictionary</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseuserdictionary)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6a02-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c6a02-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6a02-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c6a02-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c6a02-137">AllowKeyboardTextSuggestions</span><span class="sxs-lookup"><span data-stu-id="c6a02-137">AllowKeyboardTextSuggestions</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowkeyboardtextsuggestions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6a02-138">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c6a02-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6a02-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c6a02-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c6a02-140">AllowLanguageFeaturesUninstall</span><span class="sxs-lookup"><span data-stu-id="c6a02-140">AllowLanguageFeaturesUninstall</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowlanguagefeaturesuninstall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6a02-141">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c6a02-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6a02-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c6a02-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c6a02-143">ExcludeJapaneseIMEExceptJIS0208</span><span class="sxs-lookup"><span data-stu-id="c6a02-143">ExcludeJapaneseIMEExceptJIS0208</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptjis0208)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6a02-144">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c6a02-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6a02-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c6a02-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c6a02-146">ExcludeJapaneseIMEExceptJIS0208andEUDC</span><span class="sxs-lookup"><span data-stu-id="c6a02-146">ExcludeJapaneseIMEExceptJIS0208andEUDC</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptjis0208andeudc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6a02-147">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c6a02-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6a02-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c6a02-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c6a02-149">Exclude japaneseimeexceptshiftjis</span><span class="sxs-lookup"><span data-stu-id="c6a02-149">ExcludeJapaneseIMEExceptShiftJIS</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptshiftjis)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6a02-150">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c6a02-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c6a02-151">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c6a02-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c6a02-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c6a02-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6a02-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c6a02-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6a02-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6a02-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6a02-155">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c6a02-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c6a02-156">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="c6a02-156">Identifies the name of the parent node.</span></span> <span data-ttu-id="c6a02-157">Für diese Klasse ist die Zeichenfolge "TextInput".</span><span class="sxs-lookup"><span data-stu-id="c6a02-157">For this class, the string is "TextInput"</span></span>

</dd> <dt>

<span data-ttu-id="c6a02-158">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c6a02-158">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6a02-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c6a02-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c6a02-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c6a02-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c6a02-161">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c6a02-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c6a02-162">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="c6a02-162">Describes the full path to the parent node.</span></span> <span data-ttu-id="c6a02-163">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/config".</span><span class="sxs-lookup"><span data-stu-id="c6a02-163">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c6a02-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6a02-164">Requirements</span></span>



| <span data-ttu-id="c6a02-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6a02-165">Requirement</span></span> | <span data-ttu-id="c6a02-166">Wert</span><span class="sxs-lookup"><span data-stu-id="c6a02-166">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6a02-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6a02-167">Minimum supported client</span></span><br/> | <span data-ttu-id="c6a02-168">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6a02-168">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c6a02-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6a02-169">Minimum supported server</span></span><br/> | <span data-ttu-id="c6a02-170">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c6a02-170">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c6a02-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="c6a02-171">Namespace</span></span><br/>                | <span data-ttu-id="c6a02-172">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="c6a02-172">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="c6a02-173">MOF</span><span class="sxs-lookup"><span data-stu-id="c6a02-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6a02-174"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c6a02-174"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c6a02-175">DLL</span><span class="sxs-lookup"><span data-stu-id="c6a02-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6a02-176"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6a02-176"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6a02-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6a02-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6a02-178">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="c6a02-178">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

