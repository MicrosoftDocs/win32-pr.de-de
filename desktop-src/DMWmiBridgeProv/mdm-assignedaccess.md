---
title: MDM_AssignedAccess-Klasse
description: Die MDM \_ assignedaccess-Klasse wird verwendet, um festzulegen, dass das Gerät im Kiosk Modus ausgeführt wird.
ms.assetid: b9837f91-3c13-4a80-bf6d-66d8b53dfa70
keywords:
- MDM_AssignedAccess-Klasse
- MDM_AssignedAccess-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_AssignedAccess
- MDM_AssignedAccess.InstanceID
- MDM_AssignedAccess.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b5f03f99183400d4e7672323072415918e8e58e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479074"
---
# <a name="mdm_assignedaccess-class"></a><span data-ttu-id="90adc-105">MDM- \_ assignedaccess-Klasse</span><span class="sxs-lookup"><span data-stu-id="90adc-105">MDM\_AssignedAccess class</span></span>

<span data-ttu-id="90adc-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="90adc-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="90adc-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="90adc-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="90adc-108">Die **MDM \_ assignedaccess** -Klasse wird verwendet, um festzulegen, dass das Gerät im Kiosk Modus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90adc-108">The **MDM\_AssignedAccess** class is used to set the device to run in kiosk mode.</span></span> <span data-ttu-id="90adc-109">Nachdem die Klasse ausgeführt wurde, versetzt die nächste Benutzeranmeldung, die dem Kiosk Modus zugeordnet ist, das Gerät in den Kiosk Modus, in dem die im Bereitstellungs Paket angegebene Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90adc-109">Once the class has been executed, then the next user login that is associated with the kiosk mode puts the device in the kiosk mode running the application specified in the provisioning package.</span></span>

<span data-ttu-id="90adc-110">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="90adc-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="90adc-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="90adc-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AssignedAccess
{
  string InstanceID;
  string ParentID;
  string KioskModeApp;
  string Configuration;
};
```

## <a name="members"></a><span data-ttu-id="90adc-112">Member</span><span class="sxs-lookup"><span data-stu-id="90adc-112">Members</span></span>

<span data-ttu-id="90adc-113">Die **MDM \_ assignedaccess** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="90adc-113">The **MDM\_AssignedAccess** class has these types of members:</span></span>

-   [<span data-ttu-id="90adc-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="90adc-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="90adc-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="90adc-115">Properties</span></span>

<span data-ttu-id="90adc-116">Die **MDM \_ assignedaccess** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="90adc-116">The **MDM\_AssignedAccess** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="90adc-117">Configuration</span><span class="sxs-lookup"><span data-stu-id="90adc-117">Configuration</span></span>](/windows/client-management/mdm/assignedaccess-csp#assignedaccess-configuration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90adc-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="90adc-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90adc-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="90adc-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="90adc-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="90adc-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90adc-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="90adc-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90adc-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90adc-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90adc-123">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="90adc-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="90adc-124">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="90adc-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="90adc-125">Für diese Klasse lautet die Zeichenfolge "assignedaccess".</span><span class="sxs-lookup"><span data-stu-id="90adc-125">For this class, the string is "AssignedAccess".</span></span>

</dd> <dt>

[<span data-ttu-id="90adc-126">Kioskmodeapp</span><span class="sxs-lookup"><span data-stu-id="90adc-126">KioskModeApp</span></span>](/windows/client-management/mdm/assignedaccess-csp#assignedaccess-kioskmodeapp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90adc-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="90adc-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90adc-128">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="90adc-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="90adc-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="90adc-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90adc-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="90adc-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90adc-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="90adc-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90adc-132">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="90adc-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="90adc-133">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="90adc-133">Describes the full path to the parent node.</span></span> <span data-ttu-id="90adc-134">Für diese Klasse ist die Zeichenfolge "./Vendor/msft/".</span><span class="sxs-lookup"><span data-stu-id="90adc-134">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="90adc-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90adc-135">Requirements</span></span>



| <span data-ttu-id="90adc-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90adc-136">Requirement</span></span> | <span data-ttu-id="90adc-137">Wert</span><span class="sxs-lookup"><span data-stu-id="90adc-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90adc-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90adc-138">Minimum supported client</span></span><br/> | <span data-ttu-id="90adc-139">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90adc-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="90adc-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90adc-140">Minimum supported server</span></span><br/> | <span data-ttu-id="90adc-141">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="90adc-141">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="90adc-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="90adc-142">Namespace</span></span><br/>                | <span data-ttu-id="90adc-143">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="90adc-143">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="90adc-144">MOF</span><span class="sxs-lookup"><span data-stu-id="90adc-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90adc-145"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="90adc-145"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="90adc-146">DLL</span><span class="sxs-lookup"><span data-stu-id="90adc-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90adc-147"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90adc-147"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90adc-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90adc-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90adc-149">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="90adc-149">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

