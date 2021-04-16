---
title: MDM_Policy_User_Result01_AttachmentManager02-Klasse
description: Die MDM- \_ Richtlinie \_ User \_ Result01 \_ AttachmentManager02 Class stellt die verfügbaren Anlagen-Manager-Richtlinien dar.
ms.assetid: c6cfec0d-24f8-4356-a12b-d9b9944776a7
keywords:
- MDM_Policy_User_Result01_AttachmentManager02-Klasse
- MDM_Policy_User_Result01_AttachmentManager02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_AttachmentManager02
- MDM_Policy_User_Result01_AttachmentManager02.InstanceID
- MDM_Policy_User_Result01_AttachmentManager02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b78eadb9aa320d35d3a8078359a682536fd7e120
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476893"
---
# <a name="mdm_policy_user_result01_attachmentmanager02-class"></a><span data-ttu-id="8ff5b-105">MDM- \_ Richtlinien \_ Benutzer \_ Result01 \_ AttachmentManager02-Klasse</span><span class="sxs-lookup"><span data-stu-id="8ff5b-105">MDM\_Policy\_User\_Result01\_AttachmentManager02 class</span></span>

<span data-ttu-id="8ff5b-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8ff5b-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="8ff5b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8ff5b-108">Die MDM- \_ Richtlinie \_ User \_ Result01 \_ AttachmentManager02 Class stellt die verfügbaren Anlagen-Manager-Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-108">The MDM\_Policy\_User\_Result01\_AttachmentManager02 class represents the available attachment manager policies.</span></span>

<span data-ttu-id="8ff5b-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ff5b-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ff5b-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_AttachmentManager02
{
  string InstanceID;
  string ParentID;
  string DoNotPreserveZoneInformation;
  string HideZoneInfoMechanism;
  string NotifyAntivirusPrograms;
};
```

## <a name="members"></a><span data-ttu-id="8ff5b-111">Member</span><span class="sxs-lookup"><span data-stu-id="8ff5b-111">Members</span></span>

<span data-ttu-id="8ff5b-112">Die **\_ \_ Benutzer \_ Result01 \_ AttachmentManager02-Klasse der MDM-Richtlinie** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8ff5b-112">The **MDM\_Policy\_User\_Result01\_AttachmentManager02** class has these types of members:</span></span>

-   [<span data-ttu-id="8ff5b-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8ff5b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8ff5b-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8ff5b-114">Properties</span></span>

<span data-ttu-id="8ff5b-115">Die **\_ \_ Benutzer \_ Result01 \_ AttachmentManager02-Klasse der MDM-Richtlinie** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8ff5b-115">The **MDM\_Policy\_User\_Result01\_AttachmentManager02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8ff5b-116">Donotpreservezoneinformation</span><span class="sxs-lookup"><span data-stu-id="8ff5b-116">DoNotPreserveZoneInformation</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-donotpreservezoneinformation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ff5b-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8ff5b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ff5b-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8ff5b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ff5b-119">Hidezoneinf-chanismus</span><span class="sxs-lookup"><span data-stu-id="8ff5b-119">HideZoneInfoMechanism</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-hidezoneinfomechanism)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ff5b-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8ff5b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ff5b-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8ff5b-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8ff5b-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8ff5b-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ff5b-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8ff5b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ff5b-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8ff5b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ff5b-125">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8ff5b-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ff5b-126">Notigyantivirusprograms</span><span class="sxs-lookup"><span data-stu-id="8ff5b-126">NotifyAntivirusPrograms</span></span>](/windows/client-management/mdm/policy-csp-attachmentmanager#attachmentmanager-notifyantivirusprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ff5b-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8ff5b-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ff5b-128">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8ff5b-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8ff5b-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8ff5b-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ff5b-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="8ff5b-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ff5b-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8ff5b-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ff5b-132">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8ff5b-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8ff5b-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ff5b-133">Requirements</span></span>



| <span data-ttu-id="8ff5b-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ff5b-134">Requirement</span></span> | <span data-ttu-id="8ff5b-135">Wert</span><span class="sxs-lookup"><span data-stu-id="8ff5b-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ff5b-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8ff5b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8ff5b-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ff5b-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8ff5b-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8ff5b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8ff5b-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8ff5b-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8ff5b-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="8ff5b-140">Namespace</span></span><br/>                | <span data-ttu-id="8ff5b-141">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="8ff5b-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="8ff5b-142">MOF</span><span class="sxs-lookup"><span data-stu-id="8ff5b-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ff5b-143"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8ff5b-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ff5b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="8ff5b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ff5b-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ff5b-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

