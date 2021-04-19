---
description: Beschreibt ein Profil, auf das von einem anderen registrierten Profil verwiesen wird.
ms.assetid: 36FC0161-C57F-488A-9B4A-C86C6EB481D7
title: Msvm_ReferencedProfile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencedProfile
- Msvm_ReferencedProfile.Antecedent
- Msvm_ReferencedProfile.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cbe95658556be8a15bed0e7e5b5b32dda23ff21d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348645"
---
# <a name="msvm_referencedprofile-class"></a><span data-ttu-id="0514a-103">MSVM \_ referencedprofile-Klasse</span><span class="sxs-lookup"><span data-stu-id="0514a-103">Msvm\_ReferencedProfile class</span></span>

<span data-ttu-id="0514a-104">Beschreibt ein Profil, auf das von einem anderen registrierten Profil verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="0514a-104">Describes a profile that is referenced by another registered profile.</span></span>

<span data-ttu-id="0514a-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0514a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0514a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0514a-106">Syntax</span></span>

``` syntax
class Msvm_ReferencedProfile : CIM_ReferencedProfile
{
  CIM_RegisteredProfile REF Antecedent;
  CIM_RegisteredProfile REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="0514a-107">Member</span><span class="sxs-lookup"><span data-stu-id="0514a-107">Members</span></span>

<span data-ttu-id="0514a-108">Die **MSVM \_ referencedprofile** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0514a-108">The **Msvm\_ReferencedProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="0514a-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0514a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0514a-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0514a-110">Properties</span></span>

<span data-ttu-id="0514a-111">Die **MSVM \_ referencedprofile** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0514a-111">The **Msvm\_ReferencedProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0514a-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="0514a-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0514a-113">Datentyp: **[ **CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="0514a-113">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="0514a-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0514a-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0514a-115">Das registrierte Profil, auf das vom **abhängigen** Profil verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="0514a-115">The registered profile that is referenced by the **Dependent** profile.</span></span>

</dd> <dt>

<span data-ttu-id="0514a-116">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="0514a-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0514a-117">Datentyp: **[ **CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="0514a-117">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="0514a-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0514a-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0514a-119">Ein registriertes Profil, das auf andere Profile verweist.</span><span class="sxs-lookup"><span data-stu-id="0514a-119">A registered profile that references other profiles.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0514a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0514a-120">Requirements</span></span>



| <span data-ttu-id="0514a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0514a-121">Requirement</span></span> | <span data-ttu-id="0514a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="0514a-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0514a-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0514a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0514a-124">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="0514a-124">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="0514a-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0514a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0514a-126">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0514a-126">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0514a-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="0514a-127">Namespace</span></span><br/>                | <span data-ttu-id="0514a-128">Root- \\ Interop</span><span class="sxs-lookup"><span data-stu-id="0514a-128">Root\\interop</span></span><br/>                                                                                |
| <span data-ttu-id="0514a-129">MOF</span><span class="sxs-lookup"><span data-stu-id="0514a-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0514a-130"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0514a-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0514a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="0514a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0514a-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0514a-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

