---
description: Wird verwendet, um eine Instanz CIM \_ registeredprofile einer Instanz von CIM \_ registeredprofile eines anderen Profils zuzuordnen, das auf das abhängige Profil als verknüpftes Profil verweist.
ms.assetid: 631003de-477b-4447-9633-1601a7f8eadb
ms.tgt_platform: multiple
title: CIM_ReferencedProfile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ReferencedProfile
- CIM_ReferencedProfile.Antecedent
- CIM_ReferencedProfile.Dependent
api_type:
- Schema
api_location:
- Root\interop
ms.openlocfilehash: 8fdc0d8dccd325ae7e13de971e09cce6faf93455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363317"
---
# <a name="cim_referencedprofile-class"></a><span data-ttu-id="06a1a-103">CIM \_ referencedprofile-Klasse</span><span class="sxs-lookup"><span data-stu-id="06a1a-103">CIM\_ReferencedProfile class</span></span>

<span data-ttu-id="06a1a-104">Wird verwendet, um eine Instanz [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85)) einer Instanz von **CIM \_ registeredprofile** eines anderen Profils zuzuordnen, das auf das abhängige Profil als verknüpftes Profil verweist.</span><span class="sxs-lookup"><span data-stu-id="06a1a-104">Used to associate an instance [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) with an instance of **CIM\_RegisteredProfile** of another profile that references the dependent profile as a related profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="06a1a-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="06a1a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="06a1a-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="06a1a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="06a1a-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="06a1a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="06a1a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="06a1a-108">Syntax</span></span>

``` syntax
[Association, Version("2.8.0"), UMLPackagePath("CIM::Interop"), AMENDMENT]
class CIM_ReferencedProfile : CIM_Dependency
{
  CIM_RegisteredProfile REF Antecedent;
  CIM_RegisteredProfile REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="06a1a-109">Member</span><span class="sxs-lookup"><span data-stu-id="06a1a-109">Members</span></span>

<span data-ttu-id="06a1a-110">Die **CIM \_ referencedprofile** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="06a1a-110">The **CIM\_ReferencedProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="06a1a-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="06a1a-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="06a1a-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="06a1a-112">Properties</span></span>

<span data-ttu-id="06a1a-113">Die **CIM \_ referencedprofile** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="06a1a-113">The **CIM\_ReferencedProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06a1a-114">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="06a1a-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a1a-115">Datentyp: **[ **CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="06a1a-115">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="06a1a-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="06a1a-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a1a-117">Gibt die [**CIM- \_ registeredprofile**](/previous-versions//ee309375(v=vs.85)) -Instanz an, auf die vom **abhängigen** Profil verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="06a1a-117">Specifies the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) instance that is referenced by the **Dependent** profile.</span></span>

</dd> <dt>

<span data-ttu-id="06a1a-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="06a1a-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06a1a-119">Datentyp: **[ **CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="06a1a-119">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="06a1a-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="06a1a-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06a1a-121">Gibt eine [**CIM- \_ registeredprofile**](/previous-versions//ee309375(v=vs.85)) -Instanz an, die auf andere Profile verweist.</span><span class="sxs-lookup"><span data-stu-id="06a1a-121">Specifies a [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) instance that references other profiles.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06a1a-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06a1a-122">Remarks</span></span>

<span data-ttu-id="06a1a-123">Die Verwendung der **abhängigen** und der **Vorgänger** Eigenschaften in der **CIM \_ referencedprofile** -Zuordnung wird so definiert, dass das Profil, auf das verwiesen wird, der Vorgänger ist und dass das Profil, das die Referenzierung durchläuft, abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="06a1a-123">The use of the **Dependent** and **Antecedent** properties in the **CIM\_ReferencedProfile** association is defined such that the profile being referenced is the antecedent and the profile doing the referencing is the dependent.</span></span>

<span data-ttu-id="06a1a-124">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="06a1a-124">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="06a1a-125">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="06a1a-125">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="06a1a-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06a1a-126">Requirements</span></span>



| <span data-ttu-id="06a1a-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06a1a-127">Requirement</span></span> | <span data-ttu-id="06a1a-128">Wert</span><span class="sxs-lookup"><span data-stu-id="06a1a-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06a1a-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06a1a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="06a1a-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="06a1a-130">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="06a1a-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06a1a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="06a1a-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="06a1a-132">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="06a1a-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="06a1a-133">Namespace</span></span><br/>                | <span data-ttu-id="06a1a-134">Root- \\ Interop</span><span class="sxs-lookup"><span data-stu-id="06a1a-134">Root\\interop</span></span><br/>                                                               |
| <span data-ttu-id="06a1a-135">MOF</span><span class="sxs-lookup"><span data-stu-id="06a1a-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06a1a-136"><dt>Interop. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="06a1a-136"><dt>Interop.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06a1a-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06a1a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06a1a-138">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="06a1a-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

