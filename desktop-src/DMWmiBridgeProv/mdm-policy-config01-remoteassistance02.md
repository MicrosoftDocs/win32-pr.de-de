---
title: MDM_Policy_Config01_RemoteAssistance02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ RemoteAssistance02-Klasse konfiguriert die Remote Unterstützungs Richtlinien.
ms.assetid: bcc6c570-66d9-4dcd-b7f2-2d03733c0bcb
keywords:
- MDM_Policy_Config01_RemoteAssistance02-Klasse
- MDM_Policy_Config01_RemoteAssistance02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteAssistance02
- MDM_Policy_Config01_RemoteAssistance02.InstanceID
- MDM_Policy_Config01_RemoteAssistance02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aceadb2eb784e72e4e332cdd34df44d779c99e97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858878"
---
# <a name="mdm_policy_config01_remoteassistance02-class"></a><span data-ttu-id="484c9-105">MDM- \_ Richtlinie \_ Config01 \_ RemoteAssistance02-Klasse</span><span class="sxs-lookup"><span data-stu-id="484c9-105">MDM\_Policy\_Config01\_RemoteAssistance02 class</span></span>

<span data-ttu-id="484c9-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="484c9-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="484c9-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="484c9-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="484c9-108">Die MDM- \_ Richtlinie \_ Config01 \_ RemoteAssistance02-Klasse konfiguriert die Remote Unterstützungs Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="484c9-108">The MDM\_Policy\_Config01\_RemoteAssistance02 class configures the remote assistance policies.</span></span>

<span data-ttu-id="484c9-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="484c9-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="484c9-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="484c9-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteAssistance02
{
  string InstanceID;
  string ParentID;
  string CustomizeWarningMessages;
  string SessionLogging;
  string SolicitedRemoteAssistance;
  string UnsolicitedRemoteAssistance;
};
```

## <a name="members"></a><span data-ttu-id="484c9-111">Member</span><span class="sxs-lookup"><span data-stu-id="484c9-111">Members</span></span>

<span data-ttu-id="484c9-112">Die **MDM- \_ Richtlinie \_ Config01 \_ RemoteAssistance02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="484c9-112">The **MDM\_Policy\_Config01\_RemoteAssistance02** class has these types of members:</span></span>

-   [<span data-ttu-id="484c9-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="484c9-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="484c9-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="484c9-114">Properties</span></span>

<span data-ttu-id="484c9-115">Die **MDM- \_ Richtlinie \_ Config01 \_ RemoteAssistance02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="484c9-115">The **MDM\_Policy\_Config01\_RemoteAssistance02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="484c9-116">"Customizewarningmessages"</span><span class="sxs-lookup"><span data-stu-id="484c9-116">CustomizeWarningMessages</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-customizewarningmessages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="484c9-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="484c9-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="484c9-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="484c9-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="484c9-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="484c9-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="484c9-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="484c9-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="484c9-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="484c9-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="484c9-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="484c9-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="484c9-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="484c9-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="484c9-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="484c9-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="484c9-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="484c9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="484c9-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="484c9-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="484c9-127">Sessionlogging</span><span class="sxs-lookup"><span data-stu-id="484c9-127">SessionLogging</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-sessionlogging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="484c9-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="484c9-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="484c9-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="484c9-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="484c9-130">Solicitedremoteassistance</span><span class="sxs-lookup"><span data-stu-id="484c9-130">SolicitedRemoteAssistance</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-solicitedremoteassistance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="484c9-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="484c9-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="484c9-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="484c9-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="484c9-133">Unsolicitedremoteassistance</span><span class="sxs-lookup"><span data-stu-id="484c9-133">UnsolicitedRemoteAssistance</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-unsolicitedremoteassistance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="484c9-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="484c9-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="484c9-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="484c9-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="484c9-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="484c9-136">Requirements</span></span>



| <span data-ttu-id="484c9-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="484c9-137">Requirement</span></span> | <span data-ttu-id="484c9-138">Wert</span><span class="sxs-lookup"><span data-stu-id="484c9-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="484c9-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="484c9-139">Minimum supported client</span></span><br/> | <span data-ttu-id="484c9-140">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="484c9-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="484c9-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="484c9-141">Minimum supported server</span></span><br/> | <span data-ttu-id="484c9-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="484c9-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="484c9-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="484c9-143">Namespace</span></span><br/>                | <span data-ttu-id="484c9-144">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="484c9-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="484c9-145">MOF</span><span class="sxs-lookup"><span data-stu-id="484c9-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="484c9-146"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="484c9-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="484c9-147">DLL</span><span class="sxs-lookup"><span data-stu-id="484c9-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="484c9-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="484c9-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

