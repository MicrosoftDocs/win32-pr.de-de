---
title: MDM_Policy_User_Config01_CredentialsUI02-Klasse
description: Die MDM- \_ Richtlinie \_ User \_ Config01 \_ CredentialsUI02-Klasse stellt die verfügbaren Anmelde Informationsrichtlinien dar.
ms.assetid: b0a45070-c25b-4a4d-9fbc-cd107fd0fa2f
keywords:
- MDM_Policy_User_Config01_CredentialsUI02-Klasse
- MDM_Policy_User_Config01_CredentialsUI02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_CredentialsUI02
- MDM_Policy_User_Config01_CredentialsUI02.InstanceID
- MDM_Policy_User_Config01_CredentialsUI02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 230d0286ac36540b4d0b8506a72a9b4389d37e6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040828"
---
# <a name="mdm_policy_user_config01_credentialsui02-class"></a><span data-ttu-id="59403-105">MDM- \_ Richtlinien \_ Benutzer \_ Config01 \_ CredentialsUI02-Klasse</span><span class="sxs-lookup"><span data-stu-id="59403-105">MDM\_Policy\_User\_Config01\_CredentialsUI02 class</span></span>

<span data-ttu-id="59403-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="59403-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="59403-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="59403-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="59403-108">Die MDM- \_ Richtlinie \_ User \_ Config01 \_ CredentialsUI02-Klasse stellt die verfügbaren Anmelde Informationsrichtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="59403-108">The MDM\_Policy\_User\_Config01\_CredentialsUI02 class represents the available credentials policies.</span></span>

<span data-ttu-id="59403-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="59403-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="59403-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="59403-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_CredentialsUI02
{
  string InstanceID;
  string ParentID;
  string DisablePasswordReveal;
};
```

## <a name="members"></a><span data-ttu-id="59403-111">Member</span><span class="sxs-lookup"><span data-stu-id="59403-111">Members</span></span>

<span data-ttu-id="59403-112">Die **\_ \_ Benutzer \_ Config01 \_ CredentialsUI02-Klasse der MDM-Richtlinie** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="59403-112">The **MDM\_Policy\_User\_Config01\_CredentialsUI02** class has these types of members:</span></span>

-   [<span data-ttu-id="59403-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="59403-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="59403-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="59403-114">Properties</span></span>

<span data-ttu-id="59403-115">Die **\_ \_ Benutzer \_ Config01 \_ CredentialsUI02-Klasse der MDM-Richtlinie** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="59403-115">The **MDM\_Policy\_User\_Config01\_CredentialsUI02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="59403-116">Disablepasswordreveal</span><span class="sxs-lookup"><span data-stu-id="59403-116">DisablePasswordReveal</span></span>](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-disablepasswordreveal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="59403-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="59403-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59403-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="59403-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="59403-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="59403-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59403-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="59403-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59403-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="59403-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59403-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="59403-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="59403-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="59403-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59403-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="59403-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="59403-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="59403-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="59403-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="59403-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="59403-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59403-127">Requirements</span></span>



| <span data-ttu-id="59403-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59403-128">Requirement</span></span> | <span data-ttu-id="59403-129">Wert</span><span class="sxs-lookup"><span data-stu-id="59403-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59403-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="59403-130">Minimum supported client</span></span><br/> | <span data-ttu-id="59403-131">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59403-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="59403-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="59403-132">Minimum supported server</span></span><br/> | <span data-ttu-id="59403-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="59403-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="59403-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="59403-134">Namespace</span></span><br/>                | <span data-ttu-id="59403-135">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="59403-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="59403-136">MOF</span><span class="sxs-lookup"><span data-stu-id="59403-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59403-137"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="59403-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="59403-138">DLL</span><span class="sxs-lookup"><span data-stu-id="59403-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59403-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59403-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

