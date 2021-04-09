---
description: Definiert die registrierten Profile, denen das eigenständige System, auf das verwiesen wird, entspricht.
ms.assetid: d9ede8d0-c6f3-48bd-84a9-7f2c31637819
title: Msvm_StandaloneV2ElementConformsToProfile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StandaloneV2ElementConformsToProfile
- Msvm_StandaloneV2ElementConformsToProfile.ConformantStandard
- Msvm_StandaloneV2ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c492ad5bdd0e50bbbe86fd220000099269501ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959276"
---
# <a name="msvm_standalonev2elementconformstoprofile-class"></a><span data-ttu-id="0389d-103">MSVM \_ StandaloneV2ElementConformsToProfile-Klasse</span><span class="sxs-lookup"><span data-stu-id="0389d-103">Msvm\_StandaloneV2ElementConformsToProfile class</span></span>

<span data-ttu-id="0389d-104">Definiert die registrierten Profile, denen das eigenständige System, auf das verwiesen wird, entspricht.</span><span class="sxs-lookup"><span data-stu-id="0389d-104">Defines the registered profiles to which the referenced standalone system conforms.</span></span>

<span data-ttu-id="0389d-105">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="0389d-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0389d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0389d-106">Syntax</span></span>

``` syntax
class Msvm_StandaloneV2ElementConformsToProfile : Msvm_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard = $SVP;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a><span data-ttu-id="0389d-107">Member</span><span class="sxs-lookup"><span data-stu-id="0389d-107">Members</span></span>

<span data-ttu-id="0389d-108">Die **MSVM \_ StandaloneV2ElementConformsToProfile** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0389d-108">The **Msvm\_StandaloneV2ElementConformsToProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="0389d-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0389d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0389d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0389d-110">Properties</span></span>

<span data-ttu-id="0389d-111">Die **MSVM- \_ StandaloneV2ElementConformsToProfile** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0389d-111">The **Msvm\_StandaloneV2ElementConformsToProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0389d-112">**Conformantstandard**</span><span class="sxs-lookup"><span data-stu-id="0389d-112">**ConformantStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0389d-113">Datentyp: **MSVM \_ registeredprofile**</span><span class="sxs-lookup"><span data-stu-id="0389d-113">Data type: **Msvm\_RegisteredProfile**</span></span>
</dt> <dt>

<span data-ttu-id="0389d-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0389d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0389d-115">Qualifizierer: [ **override**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0389d-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0389d-116">Das registrierte Profil, dem das eigenständige System entspricht.</span><span class="sxs-lookup"><span data-stu-id="0389d-116">The registered profile to which the standalone system conforms.</span></span>

</dd> <dt>

<span data-ttu-id="0389d-117">**"Managedelement"**</span><span class="sxs-lookup"><span data-stu-id="0389d-117">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0389d-118">Datentyp: **MSVM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="0389d-118">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="0389d-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0389d-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0389d-120">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers), **MSFT \_ targetNamespace** ("root \\ \\ Virtualization \\ \\ V2")</span><span class="sxs-lookup"><span data-stu-id="0389d-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers), **MSFT\_TargetNamespace** ("root\\\\virtualization\\\\v2")</span></span>
</dt> </dl>

<span data-ttu-id="0389d-121">Das eigenständige System, das dem registrierten Profil entspricht.</span><span class="sxs-lookup"><span data-stu-id="0389d-121">The standalone system that conforms to the registered profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0389d-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0389d-122">Requirements</span></span>



| <span data-ttu-id="0389d-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0389d-123">Requirement</span></span> | <span data-ttu-id="0389d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="0389d-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0389d-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0389d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0389d-126">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0389d-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="0389d-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0389d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0389d-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0389d-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0389d-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="0389d-129">Namespace</span></span><br/>                | <span data-ttu-id="0389d-130">Root- \\ Interop</span><span class="sxs-lookup"><span data-stu-id="0389d-130">Root\\interop</span></span><br/>                                                                                |
| <span data-ttu-id="0389d-131">MOF</span><span class="sxs-lookup"><span data-stu-id="0389d-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0389d-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0389d-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0389d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0389d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0389d-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0389d-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0389d-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0389d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0389d-136">**MSVM \_ elementreformstoprofile**</span><span class="sxs-lookup"><span data-stu-id="0389d-136">**Msvm\_ElementConformsToProfile**</span></span>](msvm-elementconformstoprofile.md)
</dt> </dl>

 

