---
description: Stellt die Lauf Zeit Sicherheitseinstellungen eines CIM- \_ Computer Systems dar.
ms.assetid: fa4448dc-9353-475f-ac9b-5c50f36360d8
title: Msvm_SecurityElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityElement
- Msvm_SecurityElement.SystemCreationClassName
- Msvm_SecurityElement.SystemName
- Msvm_SecurityElement.CreationClassName
- Msvm_SecurityElement.Shielded
- Msvm_SecurityElement.EncryptStateAndVmMigrationTrafficEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0f0de0fe1a515db0e7b1d8d49b96b61500703480
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103961009"
---
# <a name="msvm_securityelement-class"></a><span data-ttu-id="ba7e4-103">MSVM \_ SecurityElement-Klasse</span><span class="sxs-lookup"><span data-stu-id="ba7e4-103">Msvm\_SecurityElement class</span></span>

<span data-ttu-id="ba7e4-104">Stellt die Lauf Zeit Sicherheitseinstellungen eines [**CIM- \_ Computer Systems**](cim-computersystem.md)dar.</span><span class="sxs-lookup"><span data-stu-id="ba7e4-104">Represents the runtime security settings of a [**CIM\_ComputerSystem**](cim-computersystem.md).</span></span>

<span data-ttu-id="ba7e4-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ba7e4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba7e4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba7e4-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecurityElement : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  boolean Shielded;
  boolean EncryptStateAndVmMigrationTrafficEnabled;
};
```

## <a name="members"></a><span data-ttu-id="ba7e4-107">Member</span><span class="sxs-lookup"><span data-stu-id="ba7e4-107">Members</span></span>

<span data-ttu-id="ba7e4-108">Die **MSVM \_ SecurityElement** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ba7e4-108">The **Msvm\_SecurityElement** class has these types of members:</span></span>

-   [<span data-ttu-id="ba7e4-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ba7e4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ba7e4-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ba7e4-110">Properties</span></span>

<span data-ttu-id="ba7e4-111">Die **MSVM \_ SecurityElement** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ba7e4-111">The **Msvm\_SecurityElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ba7e4-112">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="ba7e4-112">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7e4-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ba7e4-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba7e4-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ba7e4-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba7e4-115">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ba7e4-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ba7e4-116">Der Name der Klasse oder der Unterklasse, die bei der Erstellung einer-Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ba7e4-116">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="ba7e4-117">Wenn Sie mit den anderen Schlüsseleigenschaften dieser Klasse verwendet wird, können Sie mit " **kreationclassname** " alle Instanzen dieser Klasse und ihrer Unterklassen eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ba7e4-117">When used with the other key properties of this class, **CreationClassName** allows all instances of this class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="ba7e4-118">**"Verschlüsseltstateandvmmigrationtrafficenabled"**</span><span class="sxs-lookup"><span data-stu-id="ba7e4-118">**EncryptStateAndVmMigrationTrafficEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7e4-119">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ba7e4-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ba7e4-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ba7e4-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba7e4-121">Gibt an, ob der Zustands-und Migrations Datenverkehr der VM verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="ba7e4-121">Indicates whether the VM is currently having its state and migration traffic encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="ba7e4-122">**Geschützt**</span><span class="sxs-lookup"><span data-stu-id="ba7e4-122">**Shielded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7e4-123">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ba7e4-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ba7e4-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ba7e4-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ba7e4-125">Gibt an, ob der virtuelle Computer zurzeit geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="ba7e4-125">Indicates whether the VM is currently shielded.</span></span>

</dd> <dt>

<span data-ttu-id="ba7e4-126">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="ba7e4-126">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7e4-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ba7e4-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba7e4-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ba7e4-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba7e4-129">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**")</span><span class="sxs-lookup"><span data-stu-id="ba7e4-129">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="ba7e4-130">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="ba7e4-130">The creation class name of the scoping system.</span></span>

</dd> <dt>

<span data-ttu-id="ba7e4-131">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="ba7e4-131">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7e4-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ba7e4-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba7e4-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ba7e4-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba7e4-134">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ System**](cim-system.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="ba7e4-134">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="ba7e4-135">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="ba7e4-135">The name of the scoping system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba7e4-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba7e4-136">Requirements</span></span>



| <span data-ttu-id="ba7e4-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba7e4-137">Requirement</span></span> | <span data-ttu-id="ba7e4-138">Wert</span><span class="sxs-lookup"><span data-stu-id="ba7e4-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba7e4-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ba7e4-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ba7e4-140">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba7e4-140">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ba7e4-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ba7e4-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ba7e4-142">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ba7e4-142">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ba7e4-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="ba7e4-143">Namespace</span></span><br/>                | <span data-ttu-id="ba7e4-144">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="ba7e4-144">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ba7e4-145">MOF</span><span class="sxs-lookup"><span data-stu-id="ba7e4-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba7e4-146"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ba7e4-146"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba7e4-147">DLL</span><span class="sxs-lookup"><span data-stu-id="ba7e4-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba7e4-148"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ba7e4-148"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ba7e4-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba7e4-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba7e4-150">**CIM \_ enabledlogicalelement**</span><span class="sxs-lookup"><span data-stu-id="ba7e4-150">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

