---
title: MDM_Policy_User_Config01_AttachmentManager02-Klasse
description: Die MDM- \_ Richtlinie \_ User \_ Config01 \_ AttachmentManager02 Class stellt die verfügbaren Anlagen-Manager-Richtlinien dar.
ms.assetid: b20ec516-cdc9-4aeb-802d-97cd8423eceb
keywords:
- MDM_Policy_User_Config01_AttachmentManager02-Klasse
- MDM_Policy_User_Config01_AttachmentManager02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_AttachmentManager02
- MDM_Policy_User_Config01_AttachmentManager02.InstanceID
- MDM_Policy_User_Config01_AttachmentManager02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d127fc3770f6ba605bd8e1efdd82314231ab27f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518431"
---
# <a name="mdm_policy_user_config01_attachmentmanager02-class"></a><span data-ttu-id="68434-105">MDM- \_ Richtlinien \_ Benutzer \_ Config01 \_ AttachmentManager02-Klasse</span><span class="sxs-lookup"><span data-stu-id="68434-105">MDM\_Policy\_User\_Config01\_AttachmentManager02 class</span></span>

<span data-ttu-id="68434-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="68434-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="68434-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="68434-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="68434-108">Die MDM- \_ Richtlinie \_ User \_ Config01 \_ AttachmentManager02 Class stellt die verfügbaren Anlagen-Manager-Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="68434-108">The MDM\_Policy\_User\_Config01\_AttachmentManager02 class represents the available attachment manager policies.</span></span>

<span data-ttu-id="68434-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="68434-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="68434-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="68434-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_AttachmentManager02
{
  string InstanceID;
  string ParentID;
  string DoNotPreserveZoneInformation;
  string HideZoneInfoMechanism;
  string NotifyAntivirusPrograms;
};
```

## <a name="members"></a><span data-ttu-id="68434-111">Member</span><span class="sxs-lookup"><span data-stu-id="68434-111">Members</span></span>

<span data-ttu-id="68434-112">Die **\_ \_ Benutzer \_ Config01 \_ AttachmentManager02-Klasse der MDM-Richtlinie** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="68434-112">The **MDM\_Policy\_User\_Config01\_AttachmentManager02** class has these types of members:</span></span>

-   [<span data-ttu-id="68434-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="68434-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="68434-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="68434-114">Properties</span></span>

<span data-ttu-id="68434-115">Die **\_ \_ Benutzer \_ Config01 \_ AttachmentManager02-Klasse der MDM-Richtlinie** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="68434-115">The **MDM\_Policy\_User\_Config01\_AttachmentManager02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="68434-116">Donotpreservezoneinformation</span><span class="sxs-lookup"><span data-stu-id="68434-116">DoNotPreserveZoneInformation</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-donotpreservezoneinformation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="68434-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="68434-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68434-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="68434-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="68434-119">Hidezoneinf-chanismus</span><span class="sxs-lookup"><span data-stu-id="68434-119">HideZoneInfoMechanism</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-hidezoneinfomechanism)
</dt> <dd> <dl> <dt>

<span data-ttu-id="68434-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="68434-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68434-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="68434-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="68434-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="68434-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68434-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="68434-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68434-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="68434-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68434-125">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="68434-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="68434-126">Notigyantivirusprograms</span><span class="sxs-lookup"><span data-stu-id="68434-126">NotifyAntivirusPrograms</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-notifyantivirusprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="68434-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="68434-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68434-128">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="68434-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="68434-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="68434-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68434-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="68434-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68434-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="68434-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68434-132">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="68434-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68434-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68434-133">Requirements</span></span>



| <span data-ttu-id="68434-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68434-134">Requirement</span></span> | <span data-ttu-id="68434-135">Wert</span><span class="sxs-lookup"><span data-stu-id="68434-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68434-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68434-136">Minimum supported client</span></span><br/> | <span data-ttu-id="68434-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68434-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="68434-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68434-138">Minimum supported server</span></span><br/> | <span data-ttu-id="68434-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="68434-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="68434-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="68434-140">Namespace</span></span><br/>                | <span data-ttu-id="68434-141">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="68434-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="68434-142">MOF</span><span class="sxs-lookup"><span data-stu-id="68434-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68434-143"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="68434-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="68434-144">DLL</span><span class="sxs-lookup"><span data-stu-id="68434-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68434-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68434-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

