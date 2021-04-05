---
title: MDM_Policy_Config01_WindowsLogon02-Klasse
description: Die MDM \_ -Richtlinie \_ Config01 \_ WindowsLogon02-Klasse konfiguriert den Sperrbildschirm und die Netzwerk Benutzeroberfläche bei der Anmeldung.
ms.assetid: eb155cf8-628d-4325-8b39-f193733d4c87
keywords:
- MDM_Policy_Config01_WindowsLogon02-Klasse
- MDM_Policy_Config01_WindowsLogon02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_WindowsLogon02
- MDM_Policy_Config01_WindowsLogon02.InstanceID
- MDM_Policy_Config01_WindowsLogon02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf723729f8b90974b1ecaf5a0d8ee08eba0a3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858928"
---
# <a name="mdm_policy_config01_windowslogon02-class"></a><span data-ttu-id="6c567-105">MDM- \_ Richtlinie \_ Config01 \_ WindowsLogon02-Klasse</span><span class="sxs-lookup"><span data-stu-id="6c567-105">MDM\_Policy\_Config01\_WindowsLogon02 class</span></span>

<span data-ttu-id="6c567-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="6c567-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6c567-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="6c567-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6c567-108">Die MDM \_ -Richtlinie \_ Config01 \_ WindowsLogon02-Klasse konfiguriert den Sperrbildschirm und die Netzwerk Benutzeroberfläche bei der Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="6c567-108">The MDM\_Policy\_Config01\_WindowsLogon02 class configures the lock screen and network user interface at logon.</span></span>

<span data-ttu-id="6c567-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="6c567-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c567-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c567-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_WindowsLogon02
{
  string InstanceID;
  string ParentID;
  string DontDisplayNetworkSelectionUI;
  string DisableLockScreenAppNotifications;
  sint32 HideFastUserSwitching;
};
```

## <a name="members"></a><span data-ttu-id="6c567-111">Member</span><span class="sxs-lookup"><span data-stu-id="6c567-111">Members</span></span>

<span data-ttu-id="6c567-112">Die **MDM- \_ Richtlinie \_ Config01 \_ WindowsLogon02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6c567-112">The **MDM\_Policy\_Config01\_WindowsLogon02** class has these types of members:</span></span>

-   [<span data-ttu-id="6c567-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c567-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c567-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6c567-114">Properties</span></span>

<span data-ttu-id="6c567-115">Die **MDM- \_ Richtlinie \_ Config01 \_ WindowsLogon02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6c567-115">The **MDM\_Policy\_Config01\_WindowsLogon02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6c567-116">Disablelockscreenappbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="6c567-116">DisableLockScreenAppNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-disablelockscreenappnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c567-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6c567-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c567-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6c567-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6c567-119">Dontdisplaynetworkselectionui</span><span class="sxs-lookup"><span data-stu-id="6c567-119">DontDisplayNetworkSelectionUI</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-dontdisplaynetworkselectionui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c567-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6c567-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c567-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6c567-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6c567-122">Hidefastuserswitching</span><span class="sxs-lookup"><span data-stu-id="6c567-122">HideFastUserSwitching</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-hidefastuserswitching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c567-123">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6c567-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c567-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6c567-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6c567-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6c567-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c567-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6c567-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c567-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c567-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c567-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6c567-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6c567-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6c567-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c567-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6c567-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6c567-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6c567-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c567-132">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6c567-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c567-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c567-133">Requirements</span></span>



| <span data-ttu-id="6c567-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c567-134">Requirement</span></span> | <span data-ttu-id="6c567-135">Wert</span><span class="sxs-lookup"><span data-stu-id="6c567-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c567-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c567-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6c567-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c567-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6c567-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c567-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6c567-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6c567-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6c567-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="6c567-140">Namespace</span></span><br/>                | <span data-ttu-id="6c567-141">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="6c567-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="6c567-142">MOF</span><span class="sxs-lookup"><span data-stu-id="6c567-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c567-143"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6c567-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c567-144">DLL</span><span class="sxs-lookup"><span data-stu-id="6c567-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c567-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c567-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

