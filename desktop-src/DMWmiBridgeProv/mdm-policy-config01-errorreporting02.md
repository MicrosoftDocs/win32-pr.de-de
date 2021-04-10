---
title: MDM_Policy_Config01_ErrorReporting02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ ErrorReporting02-Klasse konfiguriert die Richtlinien für die Fehlerberichterstattung.
ms.assetid: 41067b5e-0db5-43b3-b1d5-2d6c54c35388
keywords:
- MDM_Policy_Config01_ErrorReporting02-Klasse
- MDM_Policy_Config01_ErrorReporting02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ErrorReporting02
- MDM_Policy_Config01_ErrorReporting02.InstanceID
- MDM_Policy_Config01_ErrorReporting02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1c23cf5b0b01f05fa3712d6b1de11461c6f47da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040411"
---
# <a name="mdm_policy_config01_errorreporting02-class"></a><span data-ttu-id="7d96c-105">MDM- \_ Richtlinie \_ Config01 \_ ErrorReporting02-Klasse</span><span class="sxs-lookup"><span data-stu-id="7d96c-105">MDM\_Policy\_Config01\_ErrorReporting02 class</span></span>

<span data-ttu-id="7d96c-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="7d96c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7d96c-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="7d96c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7d96c-108">Die MDM- \_ Richtlinie \_ Config01 \_ ErrorReporting02-Klasse konfiguriert die Richtlinien für die Fehlerberichterstattung.</span><span class="sxs-lookup"><span data-stu-id="7d96c-108">The MDM\_Policy\_Config01\_ErrorReporting02 class configures the error reporting policies.</span></span>

<span data-ttu-id="7d96c-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="7d96c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d96c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d96c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ErrorReporting02
{
  string InstanceID;
  string ParentID;
  string CustomizeConsentSettings;
  string DisableWindowsErrorReporting;
  string DisplayErrorNotification;
  string DoNotSendAdditionalData;
  string PreventCriticalErrorDisplay;
};
```

## <a name="members"></a><span data-ttu-id="7d96c-111">Member</span><span class="sxs-lookup"><span data-stu-id="7d96c-111">Members</span></span>

<span data-ttu-id="7d96c-112">Die **MDM- \_ Richtlinie \_ Config01 \_ ErrorReporting02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7d96c-112">The **MDM\_Policy\_Config01\_ErrorReporting02** class has these types of members:</span></span>

-   [<span data-ttu-id="7d96c-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7d96c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7d96c-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7d96c-114">Properties</span></span>

<span data-ttu-id="7d96c-115">Die **MDM- \_ Richtlinie \_ Config01 \_ ErrorReporting02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7d96c-115">The **MDM\_Policy\_Config01\_ErrorReporting02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7d96c-116">Customizeconsentsettings</span><span class="sxs-lookup"><span data-stu-id="7d96c-116">CustomizeConsentSettings</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-customizeconsentsettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d96c-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7d96c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d96c-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7d96c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d96c-119">Disablewindowserrorreporting</span><span class="sxs-lookup"><span data-stu-id="7d96c-119">DisableWindowsErrorReporting</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-disablewindowserrorreporting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d96c-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7d96c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d96c-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7d96c-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d96c-122">Display errornotification</span><span class="sxs-lookup"><span data-stu-id="7d96c-122">DisplayErrorNotification</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-displayerrornotification)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d96c-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7d96c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d96c-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7d96c-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d96c-125">Donotsendadditionaldata</span><span class="sxs-lookup"><span data-stu-id="7d96c-125">DoNotSendAdditionalData</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-donotsendadditionaldata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d96c-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7d96c-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d96c-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7d96c-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7d96c-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7d96c-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d96c-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7d96c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d96c-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7d96c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d96c-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7d96c-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7d96c-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7d96c-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d96c-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7d96c-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d96c-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7d96c-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d96c-135">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7d96c-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d96c-136">Preventcriticalerrordisplay</span><span class="sxs-lookup"><span data-stu-id="7d96c-136">PreventCriticalErrorDisplay</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-preventcriticalerrordisplay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d96c-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7d96c-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d96c-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7d96c-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d96c-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d96c-139">Requirements</span></span>



| <span data-ttu-id="7d96c-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d96c-140">Requirement</span></span> | <span data-ttu-id="7d96c-141">Wert</span><span class="sxs-lookup"><span data-stu-id="7d96c-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d96c-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7d96c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="7d96c-143">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d96c-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7d96c-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7d96c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="7d96c-145">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7d96c-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7d96c-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="7d96c-146">Namespace</span></span><br/>                | <span data-ttu-id="7d96c-147">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="7d96c-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7d96c-148">MOF</span><span class="sxs-lookup"><span data-stu-id="7d96c-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d96c-149"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7d96c-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d96c-150">DLL</span><span class="sxs-lookup"><span data-stu-id="7d96c-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d96c-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d96c-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

