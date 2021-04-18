---
description: Stellt eine Zuordnung zwischen einem virtuellen System und den Einstellungsdaten der Momentaufnahme dar, die zuletzt auf das virtuelle System angewendet wurde.
ms.assetid: 9231b441-20c4-468b-905f-5baabc32a8cc
title: Msvm_LastAppliedSnapshot-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LastAppliedSnapshot
- Msvm_LastAppliedSnapshot.Antecedent
- Msvm_LastAppliedSnapshot.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 48854d7b5aaaa6f8026f8dec14745545b0c58806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347350"
---
# <a name="msvm_lastappliedsnapshot-class"></a><span data-ttu-id="3c2cc-103">MSVM \_ lastappliedsnapshot-Klasse</span><span class="sxs-lookup"><span data-stu-id="3c2cc-103">Msvm\_LastAppliedSnapshot class</span></span>

<span data-ttu-id="3c2cc-104">Stellt eine Zuordnung zwischen einem virtuellen System und den Einstellungsdaten der Momentaufnahme dar, die zuletzt auf das virtuelle System angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="3c2cc-104">Represents an association between a virtual system and the setting data of the snapshot that was most recently applied to the virtual system.</span></span>

<span data-ttu-id="3c2cc-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3c2cc-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c2cc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c2cc-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LastAppliedSnapshot : CIM_LastAppliedSnapshot
{
  CIM_VirtualSystemSettingData REF Antecedent;
  CIM_ComputerSystem           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3c2cc-107">Member</span><span class="sxs-lookup"><span data-stu-id="3c2cc-107">Members</span></span>

<span data-ttu-id="3c2cc-108">Die **MSVM \_ lastappliedsnapshot** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3c2cc-108">The **Msvm\_LastAppliedSnapshot** class has these types of members:</span></span>

-   [<span data-ttu-id="3c2cc-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3c2cc-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3c2cc-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3c2cc-110">Properties</span></span>

<span data-ttu-id="3c2cc-111">Die **MSVM \_ lastappliedsnapshot** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3c2cc-111">The **Msvm\_LastAppliedSnapshot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3c2cc-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="3c2cc-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c2cc-113">Datentyp: **CIM \_ virtualsystemsettingdata**</span><span class="sxs-lookup"><span data-stu-id="3c2cc-113">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="3c2cc-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c2cc-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c2cc-115">Qualifizierer: **außer Kraft** setzung, **Min** (0), **Max** (1)</span><span class="sxs-lookup"><span data-stu-id="3c2cc-115">Qualifiers: **Override**, **Min** ( 0 ), **Max** ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="3c2cc-116">Verweis auf eine Instanz der [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Klasse, die die Momentaufnahme des virtuellen Systems darstellt, die zuletzt auf das virtuelle System angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="3c2cc-116">Reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents the virtual system snapshot that was last applied to the virtual system.</span></span> <span data-ttu-id="3c2cc-117">Diese Eigenschaft wird von der **CIM- \_ Abhängigkeit** geerbt.</span><span class="sxs-lookup"><span data-stu-id="3c2cc-117">This property is inherited from **CIM\_Dependency**.</span></span>

</dd> <dt>

<span data-ttu-id="3c2cc-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="3c2cc-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c2cc-119">Datentyp: **CIM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="3c2cc-119">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="3c2cc-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c2cc-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c2cc-121">Qualifizierer: **außer Kraft** setzung, **Min** (0), **Max** (1)</span><span class="sxs-lookup"><span data-stu-id="3c2cc-121">Qualifiers: **Override**, **Min** ( 0 ), **Max** ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="3c2cc-122">Verweis auf eine Instanz der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse, die das virtuelle System darstellt, auf dem die durch die **Vorgänger** Eigenschaft dargestellte virtuelle System Momentaufnahme zuletzt angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="3c2cc-122">Reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual system upon which the virtual system snapshot represented by the **Antecedent** property was most recently applied.</span></span> <span data-ttu-id="3c2cc-123">Diese Eigenschaft wird von der **CIM- \_ Abhängigkeit** geerbt.</span><span class="sxs-lookup"><span data-stu-id="3c2cc-123">This property is inherited from **CIM\_Dependency**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3c2cc-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c2cc-124">Requirements</span></span>



| <span data-ttu-id="3c2cc-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c2cc-125">Requirement</span></span> | <span data-ttu-id="3c2cc-126">Wert</span><span class="sxs-lookup"><span data-stu-id="3c2cc-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c2cc-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c2cc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3c2cc-128">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c2cc-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3c2cc-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c2cc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3c2cc-130">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c2cc-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3c2cc-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="3c2cc-131">Namespace</span></span><br/>                | <span data-ttu-id="3c2cc-132">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3c2cc-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3c2cc-133">MOF</span><span class="sxs-lookup"><span data-stu-id="3c2cc-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c2cc-134"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3c2cc-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c2cc-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3c2cc-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c2cc-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3c2cc-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




