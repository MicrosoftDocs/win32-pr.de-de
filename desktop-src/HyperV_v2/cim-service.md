---
description: Stellt ein logisches Element dar, das Informationen zur Darstellung und Verwaltung der von einem Gerät oder einer Software Funktion bereitgestellten Funktionen enthält.
ms.assetid: 0b2312da-433b-43d8-8d21-babab12a5b2c
title: CIM_Service-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service
- CIM_Service.SystemCreationClassName
- CIM_Service.SystemName
- CIM_Service.CreationClassName
- CIM_Service.Name
- CIM_Service.PrimaryOwnerName
- CIM_Service.PrimaryOwnerContact
- CIM_Service.StartMode
- CIM_Service.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b6ee3c51b6af50d77e94bb0a29bd1c8148cda8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345758"
---
# <a name="cim_service-class-hyper-v-management"></a><span data-ttu-id="c886d-103">CIM_Service-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="c886d-103">CIM_Service class (Hyper-V management)</span></span>

<span data-ttu-id="c886d-104">Stellt ein logisches Element dar, das Informationen zur Darstellung und Verwaltung der von einem Gerät oder einer Software Funktion bereitgestellten Funktionen enthält.</span><span class="sxs-lookup"><span data-stu-id="c886d-104">Represents a logical element that contains information to represent and manage the functionality provided by a device or software feature.</span></span> <span data-ttu-id="c886d-105">Bei einem Dienst handelt es sich um ein allgemeines Objekt, um die Implementierung von Funktionen zu konfigurieren und zu verwalten. Es handelt sich nicht um die eigentliche Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="c886d-105">A service is a general-purpose object to configure and manage the implementation of functionality; it is not the functionality itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="c886d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c886d-106">Syntax</span></span>

``` syntax
[Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_Service : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  string  Name;
  string  PrimaryOwnerName;
  string  PrimaryOwnerContact;
  string  StartMode;
  boolean Started;
};
```

## <a name="members"></a><span data-ttu-id="c886d-107">Member</span><span class="sxs-lookup"><span data-stu-id="c886d-107">Members</span></span>

<span data-ttu-id="c886d-108">Die **CIM- \_ Dienst** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c886d-108">The **CIM\_Service** class has these types of members:</span></span>

-   [<span data-ttu-id="c886d-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="c886d-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="c886d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c886d-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c886d-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="c886d-111">Methods</span></span>

<span data-ttu-id="c886d-112">Die **CIM- \_ Dienst** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="c886d-112">The **CIM\_Service** class has these methods.</span></span>



| <span data-ttu-id="c886d-113">Methode</span><span class="sxs-lookup"><span data-stu-id="c886d-113">Method</span></span>                                           | <span data-ttu-id="c886d-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c886d-114">Description</span></span>                    |
|:-------------------------------------------------|:-------------------------------|
| [<span data-ttu-id="c886d-115">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="c886d-115">**StartService**</span></span>](cim-service-startservice.md) | <span data-ttu-id="c886d-116">Startet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="c886d-116">Starts the service.</span></span><br/> |
| [<span data-ttu-id="c886d-117">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="c886d-117">**StopService**</span></span>](cim-service-stopservice.md)   | <span data-ttu-id="c886d-118">Beendet den Dienst.</span><span class="sxs-lookup"><span data-stu-id="c886d-118">Stops the service.</span></span><br/>  |



 

### <a name="properties"></a><span data-ttu-id="c886d-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c886d-119">Properties</span></span>

<span data-ttu-id="c886d-120">Die **CIM- \_ Dienst** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c886d-120">The **CIM\_Service** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c886d-121">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="c886d-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c886d-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c886d-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c886d-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c886d-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c886d-124">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c886d-124">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c886d-125">Der Klassenname, der verwendet wird, um eine Instanz dieser Klasse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c886d-125">The class name used to create an instance of this class.</span></span> <span data-ttu-id="c886d-126">" **Kreationclassname** " wird mit anderen Schlüsseleigenschaften dieser Klasse kombiniert, um Instanzen dieser Klasse und ihrer Unterklassen eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c886d-126">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="c886d-127">**Name**</span><span class="sxs-lookup"><span data-stu-id="c886d-127">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c886d-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c886d-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c886d-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c886d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c886d-130">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c886d-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c886d-131">Ein eindeutiger Bezeichner des Dienstanbieter, der die Funktionalität des Dienstanbieter angibt.</span><span class="sxs-lookup"><span data-stu-id="c886d-131">A unique identifier of the service that indicates the functionality of the service.</span></span>

</dd> <dt>

<span data-ttu-id="c886d-132">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="c886d-132">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c886d-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c886d-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c886d-134">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c886d-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c886d-135">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Allgemeine Informationen zu DMTF \| \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="c886d-135">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="c886d-136">Kontaktinformationen für den primären Besitzer des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="c886d-136">Contact information for the primary owner of the service.</span></span>

</dd> <dt>

<span data-ttu-id="c886d-137">**Primaryownername**</span><span class="sxs-lookup"><span data-stu-id="c886d-137">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c886d-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c886d-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c886d-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c886d-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c886d-140">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Allgemeine Informationen zu DMTF \| \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="c886d-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="c886d-141">Der Name des primären Besitzers des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="c886d-141">The name of the primary owner of the service.</span></span>

</dd> <dt>

<span data-ttu-id="c886d-142">**Gestartet**</span><span class="sxs-lookup"><span data-stu-id="c886d-142">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c886d-143">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="c886d-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c886d-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c886d-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c886d-145">**true** , wenn der Dienst gestartet wurde. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="c886d-145">**true** if the service has been started; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="c886d-146">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="c886d-146">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c886d-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c886d-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c886d-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c886d-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c886d-149">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM- \_ Dienst**.**Enableddefault**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="c886d-149">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_Service**.**EnabledDefault**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="c886d-150">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="c886d-150">This property is deprecated.</span></span> <span data-ttu-id="c886d-151">Verwenden Sie stattdessen die **enableddefault** -Eigenschaft, die von [**CIM \_ enabledlogicalelement**](cim-enabledlogicalelement.md)geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="c886d-151">Instead, use the **EnabledDefault** property that is inherited from [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).</span></span>

> [!Note]  
> <span data-ttu-id="c886d-152">Deprecated Description: gibt an, ob der Dienst automatisch gestartet wird (z. b. durch ein Betriebssystem) oder nur nach Anforderung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c886d-152">Deprecated description: Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

 

<dt>



 <span data-ttu-id="c886d-153">("Automatisch")</span><span class="sxs-lookup"><span data-stu-id="c886d-153">("Automatic")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c886d-154">("Manuell")</span><span class="sxs-lookup"><span data-stu-id="c886d-154">("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c886d-155">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="c886d-155">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c886d-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c886d-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c886d-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c886d-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c886d-158">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**")</span><span class="sxs-lookup"><span data-stu-id="c886d-158">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="c886d-159">Der Klassenname, der zum Erstellen einer Instanz des Systems verwendet wird, das den Dienst enthält.</span><span class="sxs-lookup"><span data-stu-id="c886d-159">The class name used to create an instance of the system that contains the service.</span></span> <span data-ttu-id="c886d-160">**Systemkreationclassname** wird mit anderen Schlüsseleigenschaften dieser Klasse kombiniert, um Instanzen dieser Klasse und ihrer Unterklassen eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c886d-160">**SystemCreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="c886d-161">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="c886d-161">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c886d-162">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c886d-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c886d-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c886d-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c886d-164">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ System**](cim-system.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="c886d-164">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="c886d-165">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="c886d-165">The name of the scoping system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c886d-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c886d-166">Requirements</span></span>



| <span data-ttu-id="c886d-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c886d-167">Requirement</span></span> | <span data-ttu-id="c886d-168">Wert</span><span class="sxs-lookup"><span data-stu-id="c886d-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c886d-169">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c886d-169">Minimum supported client</span></span><br/> | <span data-ttu-id="c886d-170">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c886d-170">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="c886d-171">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c886d-171">Minimum supported server</span></span><br/> | <span data-ttu-id="c886d-172">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c886d-172">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="c886d-173">Namespace</span><span class="sxs-lookup"><span data-stu-id="c886d-173">Namespace</span></span><br/>                | <span data-ttu-id="c886d-174">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="c886d-174">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c886d-175">MOF</span><span class="sxs-lookup"><span data-stu-id="c886d-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c886d-176"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c886d-176"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c886d-177">DLL</span><span class="sxs-lookup"><span data-stu-id="c886d-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c886d-178"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c886d-178"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c886d-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c886d-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c886d-180">**CIM \_ enabledlogicalelement**</span><span class="sxs-lookup"><span data-stu-id="c886d-180">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

