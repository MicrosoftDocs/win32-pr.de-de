---
description: Eine abstrakte Klasse, die Einstellungen für eine bestimmte Funktion eines Systems oder einer Komponente darstellt.
ms.assetid: f55eacdd-a802-4374-8756-a59733af6d2c
title: Msvm_FeatureSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FeatureSettingData
- Msvm_FeatureSettingData.InstanceID
- Msvm_FeatureSettingData.Caption
- Msvm_FeatureSettingData.Description
- Msvm_FeatureSettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98f022515ac877c0dd598cb9a962bc3133f76eb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525235"
---
# <a name="msvm_featuresettingdata-class"></a><span data-ttu-id="b82d9-103">MSVM \_ featuresettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="b82d9-103">Msvm\_FeatureSettingData class</span></span>

<span data-ttu-id="b82d9-104">Eine abstrakte Klasse, die Einstellungen für eine bestimmte Funktion eines Systems oder einer Komponente darstellt.</span><span class="sxs-lookup"><span data-stu-id="b82d9-104">An abstract class that represents settings for a specific feature of a system or component.</span></span>

<span data-ttu-id="b82d9-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b82d9-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b82d9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b82d9-106">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FeatureSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="b82d9-107">Member</span><span class="sxs-lookup"><span data-stu-id="b82d9-107">Members</span></span>

<span data-ttu-id="b82d9-108">Die **MSVM \_ featuresettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b82d9-108">The **Msvm\_FeatureSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b82d9-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b82d9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b82d9-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b82d9-110">Properties</span></span>

<span data-ttu-id="b82d9-111">Die **MSVM \_ featuresettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b82d9-111">The **Msvm\_FeatureSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b82d9-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b82d9-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b82d9-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b82d9-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b82d9-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b82d9-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b82d9-115">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b82d9-115">A short description of the object.</span></span> <span data-ttu-id="b82d9-116">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b82d9-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b82d9-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b82d9-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b82d9-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b82d9-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b82d9-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b82d9-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b82d9-120">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="b82d9-120">A description of the object.</span></span> <span data-ttu-id="b82d9-121">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b82d9-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b82d9-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b82d9-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b82d9-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b82d9-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b82d9-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b82d9-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b82d9-125">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b82d9-125">A display name for the object.</span></span> <span data-ttu-id="b82d9-126">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="b82d9-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b82d9-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b82d9-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b82d9-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b82d9-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b82d9-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b82d9-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b82d9-130">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="b82d9-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b82d9-131">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="b82d9-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b82d9-132">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="b82d9-132">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b82d9-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b82d9-133">Requirements</span></span>



| <span data-ttu-id="b82d9-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b82d9-134">Requirement</span></span> | <span data-ttu-id="b82d9-135">Wert</span><span class="sxs-lookup"><span data-stu-id="b82d9-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b82d9-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b82d9-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b82d9-137">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b82d9-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b82d9-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b82d9-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b82d9-139">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b82d9-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b82d9-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="b82d9-140">Namespace</span></span><br/>                | <span data-ttu-id="b82d9-141">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b82d9-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b82d9-142">MOF</span><span class="sxs-lookup"><span data-stu-id="b82d9-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b82d9-143"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b82d9-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b82d9-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b82d9-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b82d9-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b82d9-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

