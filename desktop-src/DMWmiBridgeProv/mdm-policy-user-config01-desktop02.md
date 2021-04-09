---
title: MDM_Policy_User_Config01_Desktop02-Klasse
description: Die Benutzer Config01 Desktop02-Klasse der MDM- \_ Richtlinie \_ \_ \_ stellt die verfügbaren Ordner Profil Richtlinien dar.
ms.assetid: 44a60c60-bae5-44b2-b096-387c915e2692
keywords:
- MDM_Policy_User_Config01_Desktop02-Klasse
- MDM_Policy_User_Config01_Desktop02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Desktop02
- MDM_Policy_User_Config01_Desktop02.InstanceID
- MDM_Policy_User_Config01_Desktop02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15f4ef08329b3927d7e3c3328c7c2f033fb25026
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858750"
---
# <a name="mdm_policy_user_config01_desktop02-class"></a><span data-ttu-id="cb6df-105">MDM- \_ Richtlinien \_ Benutzer \_ Config01 \_ Desktop02-Klasse</span><span class="sxs-lookup"><span data-stu-id="cb6df-105">MDM\_Policy\_User\_Config01\_Desktop02 class</span></span>

<span data-ttu-id="cb6df-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="cb6df-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cb6df-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="cb6df-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cb6df-108">Die Benutzer Config01 Desktop02-Klasse der MDM- \_ Richtlinie \_ \_ \_ stellt die verfügbaren Ordner Profil Richtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="cb6df-108">The MDM\_Policy\_User\_Config01\_Desktop02 class represents the available folder profile policies.</span></span>

<span data-ttu-id="cb6df-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="cb6df-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb6df-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb6df-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Desktop02
{
  string InstanceID;
  string ParentID;
  string PreventUserRedirectionOfProfileFolders;
};
```

## <a name="members"></a><span data-ttu-id="cb6df-111">Member</span><span class="sxs-lookup"><span data-stu-id="cb6df-111">Members</span></span>

<span data-ttu-id="cb6df-112">Die **\_ \_ Benutzer \_ Config01 \_ Desktop02-Klasse der MDM-Richtlinie** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cb6df-112">The **MDM\_Policy\_User\_Config01\_Desktop02** class has these types of members:</span></span>

-   [<span data-ttu-id="cb6df-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cb6df-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cb6df-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cb6df-114">Properties</span></span>

<span data-ttu-id="cb6df-115">Die **\_ \_ Benutzer \_ Config01 \_ Desktop02-Klasse der MDM-Richtlinie** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cb6df-115">The **MDM\_Policy\_User\_Config01\_Desktop02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cb6df-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cb6df-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb6df-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb6df-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb6df-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb6df-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb6df-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cb6df-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cb6df-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="cb6df-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb6df-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb6df-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb6df-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cb6df-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb6df-123">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cb6df-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cb6df-124">Preventuserredirectionofprofilefolders</span><span class="sxs-lookup"><span data-stu-id="cb6df-124">PreventUserRedirectionOfProfileFolders</span></span>](/windows/client-management/mdm/policy-csp-desktop#desktop-preventuserredirectionofprofilefolders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb6df-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cb6df-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb6df-126">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cb6df-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cb6df-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb6df-127">Requirements</span></span>



| <span data-ttu-id="cb6df-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb6df-128">Requirement</span></span> | <span data-ttu-id="cb6df-129">Wert</span><span class="sxs-lookup"><span data-stu-id="cb6df-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb6df-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb6df-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cb6df-131">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb6df-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cb6df-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb6df-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cb6df-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cb6df-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="cb6df-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="cb6df-134">Namespace</span></span><br/>                | <span data-ttu-id="cb6df-135">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="cb6df-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="cb6df-136">MOF</span><span class="sxs-lookup"><span data-stu-id="cb6df-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb6df-137"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cb6df-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb6df-138">DLL</span><span class="sxs-lookup"><span data-stu-id="cb6df-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb6df-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb6df-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

