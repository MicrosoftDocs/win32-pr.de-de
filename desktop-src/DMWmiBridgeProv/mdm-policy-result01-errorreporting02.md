---
title: MDM_Policy_Result01_ErrorReporting02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ ErrorReporting02-Klasse stellt die Fehler Berichterstattungs Richtlinien dar.
ms.assetid: 8cc8c570-70d7-4dcb-a558-122604a14110
keywords:
- MDM_Policy_Result01_ErrorReporting02-Klasse
- MDM_Policy_Result01_ErrorReporting02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_ErrorReporting02
- MDM_Policy_Result01_ErrorReporting02.InstanceID
- MDM_Policy_Result01_ErrorReporting02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1435e86f4e957a420a76c79f574939cb45df2a4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213717"
---
# <a name="mdm_policy_result01_errorreporting02-class"></a><span data-ttu-id="cdbf7-105">MDM- \_ Richtlinie \_ Result01 \_ ErrorReporting02-Klasse</span><span class="sxs-lookup"><span data-stu-id="cdbf7-105">MDM\_Policy\_Result01\_ErrorReporting02 class</span></span>

<span data-ttu-id="cdbf7-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="cdbf7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cdbf7-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="cdbf7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cdbf7-108">Die MDM- \_ Richtlinie \_ Result01 \_ ErrorReporting02-Klasse stellt die Fehler Berichterstattungs Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="cdbf7-108">The MDM\_Policy\_Result01\_ErrorReporting02 class represents the error reporting policies.</span></span>

<span data-ttu-id="cdbf7-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="cdbf7-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdbf7-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdbf7-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_ErrorReporting02
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

## <a name="members"></a><span data-ttu-id="cdbf7-111">Member</span><span class="sxs-lookup"><span data-stu-id="cdbf7-111">Members</span></span>

<span data-ttu-id="cdbf7-112">Die **MDM- \_ Richtlinie \_ Result01 \_ ErrorReporting02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cdbf7-112">The **MDM\_Policy\_Result01\_ErrorReporting02** class has these types of members:</span></span>

-   [<span data-ttu-id="cdbf7-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cdbf7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cdbf7-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cdbf7-114">Properties</span></span>

<span data-ttu-id="cdbf7-115">Die **MDM- \_ Richtlinie \_ Result01 \_ ErrorReporting02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cdbf7-115">The **MDM\_Policy\_Result01\_ErrorReporting02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="cdbf7-116">Customizeconsentsettings</span><span class="sxs-lookup"><span data-stu-id="cdbf7-116">CustomizeConsentSettings</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-customizeconsentsettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdbf7-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cdbf7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdbf7-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cdbf7-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cdbf7-119">Disablewindowserrorreporting</span><span class="sxs-lookup"><span data-stu-id="cdbf7-119">DisableWindowsErrorReporting</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-disablewindowserrorreporting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdbf7-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cdbf7-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdbf7-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cdbf7-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cdbf7-122">Display errornotification</span><span class="sxs-lookup"><span data-stu-id="cdbf7-122">DisplayErrorNotification</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-displayerrornotification)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdbf7-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cdbf7-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdbf7-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cdbf7-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cdbf7-125">Donotsendadditionaldata</span><span class="sxs-lookup"><span data-stu-id="cdbf7-125">DoNotSendAdditionalData</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-donotsendadditionaldata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdbf7-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cdbf7-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdbf7-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cdbf7-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cdbf7-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cdbf7-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdbf7-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cdbf7-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdbf7-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cdbf7-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdbf7-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cdbf7-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cdbf7-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="cdbf7-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdbf7-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cdbf7-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdbf7-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cdbf7-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdbf7-135">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cdbf7-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cdbf7-136">Preventcriticalerrordisplay</span><span class="sxs-lookup"><span data-stu-id="cdbf7-136">PreventCriticalErrorDisplay</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-preventcriticalerrordisplay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdbf7-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cdbf7-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdbf7-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cdbf7-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cdbf7-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cdbf7-139">Requirements</span></span>



| <span data-ttu-id="cdbf7-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cdbf7-140">Requirement</span></span> | <span data-ttu-id="cdbf7-141">Wert</span><span class="sxs-lookup"><span data-stu-id="cdbf7-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdbf7-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cdbf7-142">Minimum supported client</span></span><br/> | <span data-ttu-id="cdbf7-143">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cdbf7-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cdbf7-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cdbf7-144">Minimum supported server</span></span><br/> | <span data-ttu-id="cdbf7-145">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cdbf7-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="cdbf7-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="cdbf7-146">Namespace</span></span><br/>                | <span data-ttu-id="cdbf7-147">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="cdbf7-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="cdbf7-148">MOF</span><span class="sxs-lookup"><span data-stu-id="cdbf7-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cdbf7-149"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cdbf7-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="cdbf7-150">DLL</span><span class="sxs-lookup"><span data-stu-id="cdbf7-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdbf7-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdbf7-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

