---
description: Definiert die registrierten Profile, denen das System entspricht, auf das verwiesen wird.
ms.assetid: F01E79BE-82D9-49E0-AB0C-FD1B48BC4A55
title: Msvm_ElementConformsToProfile-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementConformsToProfile
- Msvm_ElementConformsToProfile.ConformantStandard
- Msvm_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e9b4e257c2ebc0584a8291461439f75238599d35
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843281"
---
# <a name="msvm_elementconformstoprofile-class"></a><span data-ttu-id="fc0d3-103">Msvm \_ ElementConformsToProfile-Klasse</span><span class="sxs-lookup"><span data-stu-id="fc0d3-103">Msvm\_ElementConformsToProfile class</span></span>

<span data-ttu-id="fc0d3-104">Definiert die registrierten Profile, denen das System entspricht, auf das verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="fc0d3-104">Defines the registered profiles to which the referenced system conforms.</span></span> <span data-ttu-id="fc0d3-105">Diese Zuordnung kann für jedes verwaltete Element gelten.</span><span class="sxs-lookup"><span data-stu-id="fc0d3-105">This association may apply to any managed element.</span></span> <span data-ttu-id="fc0d3-106">Die typische Verwendung wendet sie auf eine Instanz auf höherer Ebene an, z. B. auf ein System, einen Namespace oder einen Dienst.</span><span class="sxs-lookup"><span data-stu-id="fc0d3-106">Typical usage will apply it to a higher level instance, such as a System, Namespace, or Service.</span></span> <span data-ttu-id="fc0d3-107">Bei Anwendung auf eine Instanz auf höherer Ebene müssen sich alle Bestandteile entsprechend verhalten, um die Konformität des verwalteten Elements mit dem benannten registrierten Profil zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fc0d3-107">When applied to a higher level instance, all constituent parts must behave appropriately in support of the managed element's conformance to the named registered profile.</span></span>

<span data-ttu-id="fc0d3-108">Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fc0d3-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc0d3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc0d3-109">Syntax</span></span>

``` syntax
class Msvm_ElementConformsToProfile : CIM_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a><span data-ttu-id="fc0d3-110">Member</span><span class="sxs-lookup"><span data-stu-id="fc0d3-110">Members</span></span>

<span data-ttu-id="fc0d3-111">Die **Msvm \_ ElementConformsToProfile-Klasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fc0d3-111">The **Msvm\_ElementConformsToProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="fc0d3-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fc0d3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fc0d3-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fc0d3-113">Properties</span></span>

<span data-ttu-id="fc0d3-114">Die **Msvm \_ ElementConformsToProfile-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fc0d3-114">The **Msvm\_ElementConformsToProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc0d3-115">**ConformantStandard**</span><span class="sxs-lookup"><span data-stu-id="fc0d3-115">**ConformantStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc0d3-116">Datentyp: **[ **Msvm \_ RegisteredProfile**](msvm-registeredprofile.md)**</span><span class="sxs-lookup"><span data-stu-id="fc0d3-116">Data type: **[**Msvm\_RegisteredProfile**](msvm-registeredprofile.md)**</span></span>
</dt> <dt>

<span data-ttu-id="fc0d3-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fc0d3-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc0d3-118">Qualifizierer: [ **Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fc0d3-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fc0d3-119">Ein Verweis auf eine Instanz der [**Msvm \_ RegisteredProfile-Klasse,**](msvm-registeredprofile.md) die das registrierte Profil darstellt, dem das System entspricht.</span><span class="sxs-lookup"><span data-stu-id="fc0d3-119">A reference to an instance of the [**Msvm\_RegisteredProfile**](msvm-registeredprofile.md) class that represents the registered profile to which the system conforms.</span></span>

</dd> <dt>

<span data-ttu-id="fc0d3-120">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="fc0d3-120">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc0d3-121">Datentyp: **[ **Msvm \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="fc0d3-121">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="fc0d3-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fc0d3-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc0d3-123">Qualifizierer: [ **Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fc0d3-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fc0d3-124">Ein Verweis auf eine Instanz der [**Msvm \_ ComputerSystem-Klasse,**](msvm-computersystem.md) die das System darstellt, das dem registrierten Profil entspricht.</span><span class="sxs-lookup"><span data-stu-id="fc0d3-124">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the system that conforms to the registered profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fc0d3-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc0d3-125">Requirements</span></span>



| <span data-ttu-id="fc0d3-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc0d3-126">Requirement</span></span> | <span data-ttu-id="fc0d3-127">Wert</span><span class="sxs-lookup"><span data-stu-id="fc0d3-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc0d3-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fc0d3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fc0d3-129">nur Windows 8.1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc0d3-129">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="fc0d3-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fc0d3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fc0d3-131">Nur Windows Server 2012 \[ R2-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc0d3-131">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fc0d3-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="fc0d3-132">Namespace</span></span><br/>                | <span data-ttu-id="fc0d3-133">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="fc0d3-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fc0d3-134">MOF</span><span class="sxs-lookup"><span data-stu-id="fc0d3-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc0d3-135"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc0d3-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc0d3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="fc0d3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc0d3-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fc0d3-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

