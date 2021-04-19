---
description: Stellt einen Dienst Zugriffspunkt (SAP) dar, der einen Dienst verwenden oder aufrufen kann. SAPS geben an, dass ein Dienst für andere zu verwendende Entitäten verfügbar ist.
ms.assetid: 09349c95-3f7e-46c5-bea1-c3d14ee16a2a
title: CIM_ServiceAccessPoint-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessPoint
- CIM_ServiceAccessPoint.SystemCreationClassName
- CIM_ServiceAccessPoint.SystemName
- CIM_ServiceAccessPoint.CreationClassName
- CIM_ServiceAccessPoint.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e3e27fc667c55cd101b06a34f9140cb9eed8923f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356794"
---
# <a name="cim_serviceaccesspoint-class-hyper-v-management"></a><span data-ttu-id="7ef5a-104">CIM_ServiceAccessPoint-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="7ef5a-104">CIM_ServiceAccessPoint class (Hyper-V management)</span></span>

<span data-ttu-id="7ef5a-105">Stellt einen Dienst Zugriffspunkt (SAP) dar, der einen Dienst verwenden oder aufrufen kann.</span><span class="sxs-lookup"><span data-stu-id="7ef5a-105">Represents a service access point (SAP), which is able to utilize or invoke a service.</span></span> <span data-ttu-id="7ef5a-106">SAPS geben an, dass ein Dienst für andere zu verwendende Entitäten verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7ef5a-106">SAPs indicate that a service is available for other entities to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ef5a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ef5a-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ServiceAccessPoint : CIM_EnabledLogicalElement
{
  string SystemCreationClassName;
  string SystemName;
  string CreationClassName;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="7ef5a-108">Member</span><span class="sxs-lookup"><span data-stu-id="7ef5a-108">Members</span></span>

<span data-ttu-id="7ef5a-109">Die **CIM \_ serviceaccesspoint** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7ef5a-109">The **CIM\_ServiceAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="7ef5a-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7ef5a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ef5a-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7ef5a-111">Properties</span></span>

<span data-ttu-id="7ef5a-112">Die **CIM \_ serviceaccesspoint** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7ef5a-112">The **CIM\_ServiceAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7ef5a-113">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="7ef5a-113">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ef5a-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7ef5a-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ef5a-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ef5a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ef5a-116">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7ef5a-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7ef5a-117">Der Klassenname, der verwendet wird, um eine Instanz dieser Klasse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7ef5a-117">The class name used to create an instance of this class.</span></span> <span data-ttu-id="7ef5a-118">" **Kreationclassname** " wird mit anderen Schlüsseleigenschaften dieser Klasse kombiniert, um Instanzen dieser Klasse und ihrer Unterklassen eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7ef5a-118">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="7ef5a-119">**Name**</span><span class="sxs-lookup"><span data-stu-id="7ef5a-119">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ef5a-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7ef5a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ef5a-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ef5a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ef5a-122">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7ef5a-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7ef5a-123">Der eindeutige Name des SAP, der die von SAP unterstützten Funktionen angibt.</span><span class="sxs-lookup"><span data-stu-id="7ef5a-123">The unique name of the SAP that indicates the features supported by the SAP.</span></span>

</dd> <dt>

<span data-ttu-id="7ef5a-124">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="7ef5a-124">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ef5a-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7ef5a-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ef5a-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ef5a-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ef5a-127">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**")</span><span class="sxs-lookup"><span data-stu-id="7ef5a-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="7ef5a-128">Der Klassenname, der zum Erstellen einer Instanz des Systems verwendet wird, das den SAP enthält.</span><span class="sxs-lookup"><span data-stu-id="7ef5a-128">The class name used to create an instance of the system that contains the SAP.</span></span> <span data-ttu-id="7ef5a-129">**Systemkreationclassname** wird mit anderen Schlüsseleigenschaften dieser Klasse kombiniert, um Instanzen dieser Klasse und ihrer Unterklassen eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7ef5a-129">**SystemCreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="7ef5a-130">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="7ef5a-130">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ef5a-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7ef5a-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ef5a-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7ef5a-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ef5a-133">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ System**](cim-system.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="7ef5a-133">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="7ef5a-134">Der Name des Systems, das den SAP enthält.</span><span class="sxs-lookup"><span data-stu-id="7ef5a-134">The name of the system that contains the SAP.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7ef5a-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ef5a-135">Requirements</span></span>



| <span data-ttu-id="7ef5a-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ef5a-136">Requirement</span></span> | <span data-ttu-id="7ef5a-137">Wert</span><span class="sxs-lookup"><span data-stu-id="7ef5a-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ef5a-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ef5a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7ef5a-139">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7ef5a-139">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="7ef5a-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ef5a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7ef5a-141">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ef5a-141">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="7ef5a-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="7ef5a-142">Namespace</span></span><br/>                | <span data-ttu-id="7ef5a-143">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="7ef5a-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7ef5a-144">MOF</span><span class="sxs-lookup"><span data-stu-id="7ef5a-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ef5a-145"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7ef5a-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ef5a-146">DLL</span><span class="sxs-lookup"><span data-stu-id="7ef5a-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ef5a-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7ef5a-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7ef5a-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ef5a-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ef5a-149">**CIM \_ enabledlogicalelement**</span><span class="sxs-lookup"><span data-stu-id="7ef5a-149">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

