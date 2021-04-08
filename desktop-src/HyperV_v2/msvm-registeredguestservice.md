---
description: Stellt eine Zuordnung zwischen einer Instanz von MSVM \_ guestserviceinterfacecomponent und einer Instanz von MSVM \_ guestservice dar, die einen Dienst darstellt, der im Gast Betriebssystem ausgeführt wird.
ms.assetid: 246CFAC1-7D83-4DE7-B9D3-96326511E08B
title: Msvm_RegisteredGuestService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredGuestService
- Msvm_RegisteredGuestService.Antecedent
- Msvm_RegisteredGuestService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 850d7f081b070fd34ef11bc56e8cd1f914e498b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756894"
---
# <a name="msvm_registeredguestservice-class"></a><span data-ttu-id="cbe99-103">MSVM \_ registeredguestservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="cbe99-103">Msvm\_RegisteredGuestService class</span></span>

<span data-ttu-id="cbe99-104">Stellt eine Zuordnung zwischen einer Instanz von [**MSVM \_ guestserviceinterfacecomponent**](msvm-guestserviceinterfacecomponent.md) und einer Instanz von [**MSVM \_ guestservice**](msvm-guestservice.md)dar, die einen Dienst darstellt, der im Gast Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cbe99-104">Represents an association between an instance of [**Msvm\_GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) and an instance of [**Msvm\_GuestService**](msvm-guestservice.md), which represents a service running in the guest.</span></span> <span data-ttu-id="cbe99-105">Diese Klasse wird von der [**CIM- \_ Abhängigkeits**](/windows/desktop/CIMWin32Prov/cim-dependency) Klasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="cbe99-105">This class derives from the [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency) class.</span></span>

<span data-ttu-id="cbe99-106">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="cbe99-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbe99-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cbe99-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RegisteredGuestService : CIM_Dependency
{
  Msvm_GuestServiceInterfaceComponent REF Antecedent;
  Msvm_GuestService                   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="cbe99-108">Member</span><span class="sxs-lookup"><span data-stu-id="cbe99-108">Members</span></span>

<span data-ttu-id="cbe99-109">Die **MSVM \_ registeredguestservice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cbe99-109">The **Msvm\_RegisteredGuestService** class has these types of members:</span></span>

-   [<span data-ttu-id="cbe99-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cbe99-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cbe99-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cbe99-111">Properties</span></span>

<span data-ttu-id="cbe99-112">Die **MSVM \_ registeredguestservice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cbe99-112">The **Msvm\_RegisteredGuestService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cbe99-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="cbe99-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbe99-114">Datentyp: **[ **MSVM \_ guestserviceinterfacecomponent**](msvm-guestserviceinterfacecomponent.md)**</span><span class="sxs-lookup"><span data-stu-id="cbe99-114">Data type: **[**Msvm\_GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)**</span></span>
</dt> <dt>

<span data-ttu-id="cbe99-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cbe99-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbe99-116">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM- \_ Abhängigkeit. Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="cbe99-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="cbe99-117">Verweis auf die Komponente der Gast Dienst Schnittstelle in dieser Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="cbe99-117">Reference to the guest service interface component in this association.</span></span>

</dd> <dt>

<span data-ttu-id="cbe99-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="cbe99-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbe99-119">Datentyp: **[ **MSVM \_ guestservice**](msvm-guestservice.md)**</span><span class="sxs-lookup"><span data-stu-id="cbe99-119">Data type: **[**Msvm\_GuestService**](msvm-guestservice.md)**</span></span>
</dt> <dt>

<span data-ttu-id="cbe99-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cbe99-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbe99-121">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM- \_ Abhängigkeit. abhängig")</span><span class="sxs-lookup"><span data-stu-id="cbe99-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="cbe99-122">Verweis auf den registrierten Gast Dienst, der von der **Vorgänger** Eigenschaft abhängt.</span><span class="sxs-lookup"><span data-stu-id="cbe99-122">Reference to the registered guest service that is dependent on the **Antecedent** property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cbe99-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cbe99-123">Requirements</span></span>



| <span data-ttu-id="cbe99-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cbe99-124">Requirement</span></span> | <span data-ttu-id="cbe99-125">Wert</span><span class="sxs-lookup"><span data-stu-id="cbe99-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbe99-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cbe99-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cbe99-127">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="cbe99-127">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="cbe99-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cbe99-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cbe99-129">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cbe99-129">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cbe99-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="cbe99-130">Namespace</span></span><br/>                | <span data-ttu-id="cbe99-131">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="cbe99-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cbe99-132">MOF</span><span class="sxs-lookup"><span data-stu-id="cbe99-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cbe99-133"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cbe99-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cbe99-134">DLL</span><span class="sxs-lookup"><span data-stu-id="cbe99-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbe99-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cbe99-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cbe99-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cbe99-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbe99-137">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="cbe99-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="cbe99-138">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="cbe99-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

