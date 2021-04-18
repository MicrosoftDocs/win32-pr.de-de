---
title: MDM_Policy_Config01_ActiveXControls02-Klasse
description: Mit dieser Richtlinien Einstellung wird festgelegt, welche ActiveX-Installations Standorte Standardbenutzer in Ihrer Organisation verwenden können, um ActiveX-Steuerelemente auf ihren Computern zu installieren.
ms.assetid: 242888ae-f07a-40b7-9539-29fcca9cfc40
keywords:
- MDM_Policy_Config01_ActiveXControls02-Klasse
- MDM_Policy_Config01_ActiveXControls02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ActiveXControls02
- MDM_Policy_Config01_ActiveXControls02.InstanceID
- MDM_Policy_Config01_ActiveXControls02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 213edcea47bc0fd3379f753613c5b884963ca781
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339323"
---
# <a name="mdm_policy_config01_activexcontrols02-class"></a><span data-ttu-id="815a4-105">MDM- \_ Richtlinie \_ Config01 \_ ActiveXControls02-Klasse</span><span class="sxs-lookup"><span data-stu-id="815a4-105">MDM\_Policy\_Config01\_ActiveXControls02 class</span></span>

<span data-ttu-id="815a4-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="815a4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="815a4-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="815a4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="815a4-108">Mit dieser Richtlinien Einstellung wird festgelegt, welche ActiveX-Installations Standorte Standardbenutzer in Ihrer Organisation verwenden können, um ActiveX-Steuerelemente auf ihren Computern zu installieren.</span><span class="sxs-lookup"><span data-stu-id="815a4-108">This policy setting determines which ActiveX installation sites standard users in your organization can use to install ActiveX controls on their computers.</span></span> <span data-ttu-id="815a4-109">Wenn diese Einstellung aktiviert ist, kann der Administrator eine Liste der genehmigten ActiveX-Installations Standorte erstellen, die von der Host-URL angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="815a4-109">When this setting is enabled, the administrator can create a list of approved Activex Install sites specified by host URL.</span></span>

<span data-ttu-id="815a4-110">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="815a4-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="815a4-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="815a4-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ActiveXControls02
{
  string InstanceID;
  string ParentID;
  string ApprovedInstallationSites;
};
```

## <a name="members"></a><span data-ttu-id="815a4-112">Member</span><span class="sxs-lookup"><span data-stu-id="815a4-112">Members</span></span>

<span data-ttu-id="815a4-113">Die **MDM- \_ Richtlinie \_ Config01 \_ ActiveXControls02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="815a4-113">The **MDM\_Policy\_Config01\_ActiveXControls02** class has these types of members:</span></span>

-   [<span data-ttu-id="815a4-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="815a4-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="815a4-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="815a4-115">Properties</span></span>

<span data-ttu-id="815a4-116">Die **MDM- \_ Richtlinie \_ Config01 \_ ActiveXControls02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="815a4-116">The **MDM\_Policy\_Config01\_ActiveXControls02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="815a4-117">Approvedinstallationsites</span><span class="sxs-lookup"><span data-stu-id="815a4-117">ApprovedInstallationSites</span></span>](/windows/client-management/mdm/policy-csp-activexcontrols#activexcontrols-approvedinstallationsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="815a4-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="815a4-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="815a4-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="815a4-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="815a4-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="815a4-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="815a4-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="815a4-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="815a4-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="815a4-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="815a4-123">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="815a4-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="815a4-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="815a4-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="815a4-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="815a4-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="815a4-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="815a4-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="815a4-127">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="815a4-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="815a4-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="815a4-128">Requirements</span></span>



| <span data-ttu-id="815a4-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="815a4-129">Requirement</span></span> | <span data-ttu-id="815a4-130">Wert</span><span class="sxs-lookup"><span data-stu-id="815a4-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="815a4-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="815a4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="815a4-132">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="815a4-132">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="815a4-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="815a4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="815a4-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="815a4-134">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="815a4-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="815a4-135">Namespace</span></span><br/>                | <span data-ttu-id="815a4-136">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="815a4-136">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="815a4-137">MOF</span><span class="sxs-lookup"><span data-stu-id="815a4-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="815a4-138"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="815a4-138"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="815a4-139">DLL</span><span class="sxs-lookup"><span data-stu-id="815a4-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="815a4-140"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="815a4-140"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

