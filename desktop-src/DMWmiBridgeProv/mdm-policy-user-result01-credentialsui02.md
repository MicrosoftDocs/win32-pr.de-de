---
title: MDM_Policy_User_Result01_CredentialsUI02-Klasse
description: Die MDM- \_ Richtlinie \_ User \_ Result01 \_ CredentialsUI02-Klasse stellt die verfügbaren Anmelde Informationsrichtlinien dar.
ms.assetid: e1df7798-676a-4846-89e5-2c05d0259086
keywords:
- MDM_Policy_User_Result01_CredentialsUI02-Klasse
- MDM_Policy_User_Result01_CredentialsUI02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_CredentialsUI02
- MDM_Policy_User_Result01_CredentialsUI02.InstanceID
- MDM_Policy_User_Result01_CredentialsUI02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7659990ee980872059bd26b0a8b553202e6cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040653"
---
# <a name="mdm_policy_user_result01_credentialsui02-class"></a><span data-ttu-id="c3152-105">MDM- \_ Richtlinien \_ Benutzer \_ Result01 \_ CredentialsUI02-Klasse</span><span class="sxs-lookup"><span data-stu-id="c3152-105">MDM\_Policy\_User\_Result01\_CredentialsUI02 class</span></span>

<span data-ttu-id="c3152-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="c3152-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c3152-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="c3152-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c3152-108">Die MDM- \_ Richtlinie \_ User \_ Result01 \_ CredentialsUI02-Klasse stellt die verfügbaren Anmelde Informationsrichtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="c3152-108">The MDM\_Policy\_User\_Result01\_CredentialsUI02 class represents the available credentials policies.</span></span>

<span data-ttu-id="c3152-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="c3152-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3152-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3152-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_CredentialsUI02
{
  string InstanceID;
  string ParentID;
  string DisablePasswordReveal;
};
```

## <a name="members"></a><span data-ttu-id="c3152-111">Member</span><span class="sxs-lookup"><span data-stu-id="c3152-111">Members</span></span>

<span data-ttu-id="c3152-112">Die **\_ \_ Benutzer \_ Result01 \_ CredentialsUI02-Klasse der MDM-Richtlinie** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c3152-112">The **MDM\_Policy\_User\_Result01\_CredentialsUI02** class has these types of members:</span></span>

-   [<span data-ttu-id="c3152-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c3152-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c3152-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c3152-114">Properties</span></span>

<span data-ttu-id="c3152-115">Die **\_ \_ Benutzer \_ Result01 \_ CredentialsUI02-Klasse der MDM-Richtlinie** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c3152-115">The **MDM\_Policy\_User\_Result01\_CredentialsUI02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c3152-116">Disablepasswordreveal</span><span class="sxs-lookup"><span data-stu-id="c3152-116">DisablePasswordReveal</span></span>](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-disablepasswordreveal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3152-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3152-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3152-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c3152-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c3152-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c3152-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3152-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3152-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3152-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3152-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3152-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c3152-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c3152-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c3152-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3152-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3152-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3152-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3152-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3152-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c3152-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3152-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3152-127">Requirements</span></span>



| <span data-ttu-id="c3152-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3152-128">Requirement</span></span> | <span data-ttu-id="c3152-129">Wert</span><span class="sxs-lookup"><span data-stu-id="c3152-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3152-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3152-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c3152-131">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3152-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c3152-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3152-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c3152-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c3152-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c3152-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="c3152-134">Namespace</span></span><br/>                | <span data-ttu-id="c3152-135">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="c3152-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c3152-136">MOF</span><span class="sxs-lookup"><span data-stu-id="c3152-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3152-137"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c3152-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3152-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c3152-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3152-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3152-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

