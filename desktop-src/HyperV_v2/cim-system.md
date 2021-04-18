---
description: Stellt einen Satz von Komponenten dar, die als einzelne Entität auf hoher Ebene fungieren.
ms.assetid: 784cee32-e0ae-4632-8dac-e5110513f5c9
title: CIM_System-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_System
- CIM_System.CreationClassName
- CIM_System.Name
- CIM_System.NameFormat
- CIM_System.PrimaryOwnerName
- CIM_System.PrimaryOwnerContact
- CIM_System.Roles
- CIM_System.OtherIdentifyingInfo
- CIM_System.IdentifyingDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a51e56ad3e8f91200fbe5bc7e09ac2f14c4ee232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347926"
---
# <a name="cim_system-class-hyper-v-management"></a><span data-ttu-id="99e07-103">CIM_System-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="99e07-103">CIM_System class (Hyper-V management)</span></span>

<span data-ttu-id="99e07-104">Stellt einen Satz von Komponenten dar, die als einzelne Entität auf hoher Ebene fungieren.</span><span class="sxs-lookup"><span data-stu-id="99e07-104">Represents a set of components that function as a single high-level entity.</span></span>

## <a name="syntax"></a><span data-ttu-id="99e07-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="99e07-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_System : CIM_EnabledLogicalElement
{
  string CreationClassName;
  string Name;
  string NameFormat;
  string PrimaryOwnerName;
  string PrimaryOwnerContact;
  string Roles[];
  string OtherIdentifyingInfo[];
  string IdentifyingDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="99e07-106">Member</span><span class="sxs-lookup"><span data-stu-id="99e07-106">Members</span></span>

<span data-ttu-id="99e07-107">Die **CIM- \_ System** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="99e07-107">The **CIM\_System** class has these types of members:</span></span>

-   [<span data-ttu-id="99e07-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="99e07-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="99e07-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="99e07-109">Properties</span></span>

<span data-ttu-id="99e07-110">Die **CIM- \_ System** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="99e07-110">The **CIM\_System** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="99e07-111">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="99e07-111">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99e07-112">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="99e07-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="99e07-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="99e07-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="99e07-114">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="99e07-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="99e07-115">Der Klassenname, der verwendet wird, um eine Instanz dieser Klasse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="99e07-115">The class name used to create an instance of this class.</span></span> <span data-ttu-id="99e07-116">" **Kreationclassname** " wird mit anderen Schlüsseleigenschaften dieser Klasse kombiniert, um Instanzen dieser Klasse und ihrer Unterklassen eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="99e07-116">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="99e07-117">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="99e07-117">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99e07-118">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="99e07-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="99e07-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="99e07-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="99e07-120">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ System**".**"OtherIdentifyingInfo**")</span><span class="sxs-lookup"><span data-stu-id="99e07-120">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_System**.**OtherIdentifyingInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="99e07-121">Ein Array, das Beschreibungen der Werte in der Eigenschaft " **OtherIdentifyingInfo** " enthält.</span><span class="sxs-lookup"><span data-stu-id="99e07-121">An array that contains descriptions of the values in the **OtherIdentifyingInfo** property.</span></span> <span data-ttu-id="99e07-122">Die Array Elemente in **identifyingbeschreibungen** entsprechen den Elementen in der **identifyingbeschreibungen** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="99e07-122">The array items in **IdentifyingDescriptions** correspond to the items in the **IdentifyingDescriptions** property.</span></span>

</dd> <dt>

<span data-ttu-id="99e07-123">**Name**</span><span class="sxs-lookup"><span data-stu-id="99e07-123">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99e07-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="99e07-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="99e07-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="99e07-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="99e07-126">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="99e07-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="99e07-127">Der Schlüssel dieser Instanz in einer Unternehmensumgebung.</span><span class="sxs-lookup"><span data-stu-id="99e07-127">The key of this instance in an enterprise environment.</span></span>

</dd> <dt>

<span data-ttu-id="99e07-128">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="99e07-128">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99e07-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="99e07-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="99e07-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="99e07-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="99e07-131">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="99e07-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="99e07-132">Die Namenskonvention, die von der Name-Eigenschaft verwendet wird, um sicherzustellen, dass die **namens** Werte eindeutig sind</span><span class="sxs-lookup"><span data-stu-id="99e07-132">The naming convention used by the Name property to ensure that **Name** values are unique.</span></span>

</dd> <dt>

<span data-ttu-id="99e07-133">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="99e07-133">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99e07-134">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="99e07-134">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="99e07-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="99e07-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="99e07-136">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ System**".**Identifyingbeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="99e07-136">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_System**.**IdentifyingDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="99e07-137">Ein Array, das einen Satz zusätzlicher Daten enthält, die über Systemnamen Informationen hinausgehen und zur Identifizierung eines Computer Systems verwendet werden könnten.</span><span class="sxs-lookup"><span data-stu-id="99e07-137">An array that contains a set of additional data, beyond system name information, that could be used to identify a computer system.</span></span>

</dd> <dt>

<span data-ttu-id="99e07-138">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="99e07-138">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99e07-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="99e07-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="99e07-140">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="99e07-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="99e07-141">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Allgemeine Informationen zu DMTF \| \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="99e07-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="99e07-142">Eine Zeichenfolge, die Informationen darüber bereitstellt, wie der primäre Systembesitzer erreicht werden kann (z. b. Telefonnummer, e-Mail-Adresse usw.).</span><span class="sxs-lookup"><span data-stu-id="99e07-142">A string that provides information on how the primary system owner can be reached (for example, phone number, e-mail address, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="99e07-143">**Primaryownername**</span><span class="sxs-lookup"><span data-stu-id="99e07-143">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99e07-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="99e07-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="99e07-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="99e07-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="99e07-146">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Allgemeine Informationen zu DMTF \| \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="99e07-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="99e07-147">Der Name des primären Benutzers des Systems.</span><span class="sxs-lookup"><span data-stu-id="99e07-147">The name of the primary user of the system.</span></span>

</dd> <dt>

<span data-ttu-id="99e07-148">**Rollen**</span><span class="sxs-lookup"><span data-stu-id="99e07-148">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99e07-149">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="99e07-149">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="99e07-150">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="99e07-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="99e07-151">Ein Array, das die Rollen enthält, die vom System in einer Unternehmensumgebung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="99e07-151">An array that contains the roles carried out by the system in an enterprise environment.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="99e07-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99e07-152">Requirements</span></span>



| <span data-ttu-id="99e07-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99e07-153">Requirement</span></span> | <span data-ttu-id="99e07-154">Wert</span><span class="sxs-lookup"><span data-stu-id="99e07-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99e07-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="99e07-155">Minimum supported client</span></span><br/> | <span data-ttu-id="99e07-156">Windows 8</span><span class="sxs-lookup"><span data-stu-id="99e07-156">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="99e07-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="99e07-157">Minimum supported server</span></span><br/> | <span data-ttu-id="99e07-158">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="99e07-158">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="99e07-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="99e07-159">Namespace</span></span><br/>                | <span data-ttu-id="99e07-160">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="99e07-160">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="99e07-161">MOF</span><span class="sxs-lookup"><span data-stu-id="99e07-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99e07-162"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="99e07-162"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="99e07-163">DLL</span><span class="sxs-lookup"><span data-stu-id="99e07-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99e07-164"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="99e07-164"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="99e07-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99e07-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99e07-166">**CIM \_ enabledlogicalelement**</span><span class="sxs-lookup"><span data-stu-id="99e07-166">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

