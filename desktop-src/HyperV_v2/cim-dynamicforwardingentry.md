---
description: Stellt einen Eintrag in der Weiterleitungs Datenbank dar, der der CIM \_ transparentbridgingservice-Klasse zugeordnet ist.
ms.assetid: 4c3afe7c-f7e5-4a83-8ba1-f0b1909cee52
title: CIM_DynamicForwardingEntry-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DynamicForwardingEntry
- CIM_DynamicForwardingEntry.SystemCreationClassName
- CIM_DynamicForwardingEntry.SystemName
- CIM_DynamicForwardingEntry.ServiceCreationClassName
- CIM_DynamicForwardingEntry.ServiceName
- CIM_DynamicForwardingEntry.CreationClassName
- CIM_DynamicForwardingEntry.MACAddress
- CIM_DynamicForwardingEntry.DynamicStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65cf4f1bc5e678089d54dd99a09a6d3b7aeb3dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345781"
---
# <a name="cim_dynamicforwardingentry-class"></a><span data-ttu-id="cf4fc-103">CIM \_ dynamicforwardingentry-Klasse</span><span class="sxs-lookup"><span data-stu-id="cf4fc-103">CIM\_DynamicForwardingEntry class</span></span>

<span data-ttu-id="cf4fc-104">Stellt einen Eintrag in der Weiterleitungs Datenbank dar, der der [**CIM \_ transparentbridgingservice**](cim-transparentbridgingservice.md) -Klasse zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cf4fc-104">Represents an entry in the forwarding database associated with the [**CIM\_TransparentBridgingService**](cim-transparentbridgingservice.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf4fc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf4fc-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_DynamicForwardingEntry : CIM_LogicalElement
{
  string SystemCreationClassName;
  string SystemName;
  string ServiceCreationClassName;
  string ServiceName;
  string CreationClassName;
  string MACAddress;
  uint16 DynamicStatus;
};
```

## <a name="members"></a><span data-ttu-id="cf4fc-106">Member</span><span class="sxs-lookup"><span data-stu-id="cf4fc-106">Members</span></span>

<span data-ttu-id="cf4fc-107">Die **CIM \_ dynamicforwardingentry** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cf4fc-107">The **CIM\_DynamicForwardingEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="cf4fc-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cf4fc-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cf4fc-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cf4fc-109">Properties</span></span>

<span data-ttu-id="cf4fc-110">Die **CIM \_ dynamicforwardingentry** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cf4fc-110">The **CIM\_DynamicForwardingEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cf4fc-111">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="cf4fc-111">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf4fc-112">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cf4fc-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf4fc-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cf4fc-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf4fc-114">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="cf4fc-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cf4fc-115">Der Name der Klasse oder der Unterklasse, die zum Erstellen der Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cf4fc-115">The name of the class or the subclass used to create the instance.</span></span> <span data-ttu-id="cf4fc-116">Wenn diese Eigenschaft mit den anderen Schlüsseleigenschaften dieser Klasse verwendet wird, können alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="cf4fc-116">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="cf4fc-117">**Dynamicstatus**</span><span class="sxs-lookup"><span data-stu-id="cf4fc-117">**DynamicStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf4fc-118">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cf4fc-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cf4fc-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cf4fc-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf4fc-120">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dTpFdbStatus ")</span><span class="sxs-lookup"><span data-stu-id="cf4fc-120">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpFdbStatus")</span></span>
</dt> </dl>

<span data-ttu-id="cf4fc-121">Der Status des Eintrags.</span><span class="sxs-lookup"><span data-stu-id="cf4fc-121">The status of the entry.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cf4fc-122">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="cf4fc-122">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>

<span data-ttu-id="cf4fc-123">**Ungültig** (2)</span><span class="sxs-lookup"><span data-stu-id="cf4fc-123">**Invalid** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>

<span data-ttu-id="cf4fc-124">**Gelernt** (3)</span><span class="sxs-lookup"><span data-stu-id="cf4fc-124">**Learned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Self"></span><span id="self"></span><span id="SELF"></span>

<span data-ttu-id="cf4fc-125">**Selbst** (4)</span><span class="sxs-lookup"><span data-stu-id="cf4fc-125">**Self** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>

<span data-ttu-id="cf4fc-126">**Mgmt** (5)</span><span class="sxs-lookup"><span data-stu-id="cf4fc-126">**Mgmt** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cf4fc-127">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="cf4fc-127">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf4fc-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cf4fc-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf4fc-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cf4fc-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf4fc-130">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (12), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dTpFdbAddress ")</span><span class="sxs-lookup"><span data-stu-id="cf4fc-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpFdbAddress")</span></span>
</dt> </dl>

<span data-ttu-id="cf4fc-131">Die Unicast-MAC-Adresse, für die der Überbrückungs Dienst Informationen filtert.</span><span class="sxs-lookup"><span data-stu-id="cf4fc-131">The Unicast MAC address for which the bridging service filters information.</span></span> <span data-ttu-id="cf4fc-132">Die Mac-Adresse ist als zwölf hexadezimal Ziffern (z. b. 010203040506) formatiert, wobei jedes Paar eines der sechs Oktette der Mac-Adresse in kanonischer bitreihenfolge gemäß RFC 2469 darstellt.</span><span class="sxs-lookup"><span data-stu-id="cf4fc-132">The MAC address is formatted as twelve hexadecimal digits, such as 010203040506, with each pair representing one of the six octets of the MAC address in canonical bit order according to RFC 2469.</span></span>

</dd> <dt>

<span data-ttu-id="cf4fc-133">**Servicecreationclassname**</span><span class="sxs-lookup"><span data-stu-id="cf4fc-133">**ServiceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf4fc-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cf4fc-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf4fc-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cf4fc-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf4fc-136">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ Dienst**](cim-service.md).**"Kreationclassname**")</span><span class="sxs-lookup"><span data-stu-id="cf4fc-136">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Service**](cim-service.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="cf4fc-137">Der Wert von " **kreationclassname** " des Bereichs Dienst Objekts.</span><span class="sxs-lookup"><span data-stu-id="cf4fc-137">The **CreationClassName** value of the scoping service object.</span></span>

</dd> <dt>

<span data-ttu-id="cf4fc-138">**Service Name**</span><span class="sxs-lookup"><span data-stu-id="cf4fc-138">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf4fc-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cf4fc-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf4fc-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cf4fc-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf4fc-141">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ Dienst**](cim-service.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="cf4fc-141">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Service**](cim-service.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="cf4fc-142">Der Name des Bereichs Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="cf4fc-142">The name of the scoping service.</span></span>

</dd> <dt>

<span data-ttu-id="cf4fc-143">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="cf4fc-143">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf4fc-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cf4fc-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf4fc-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cf4fc-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf4fc-146">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**")</span><span class="sxs-lookup"><span data-stu-id="cf4fc-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="cf4fc-147">Der Wert von " **kreationclassname** " des Bereichs System Objekts.</span><span class="sxs-lookup"><span data-stu-id="cf4fc-147">The **CreationClassName** value of the scoping system object.</span></span>

</dd> <dt>

<span data-ttu-id="cf4fc-148">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="cf4fc-148">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf4fc-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cf4fc-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cf4fc-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cf4fc-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf4fc-151">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ System**](cim-system.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="cf4fc-151">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="cf4fc-152">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="cf4fc-152">The name of the scoping system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf4fc-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf4fc-153">Requirements</span></span>



| <span data-ttu-id="cf4fc-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf4fc-154">Requirement</span></span> | <span data-ttu-id="cf4fc-155">Wert</span><span class="sxs-lookup"><span data-stu-id="cf4fc-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4fc-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf4fc-156">Minimum supported client</span></span><br/> | <span data-ttu-id="cf4fc-157">Windows 8</span><span class="sxs-lookup"><span data-stu-id="cf4fc-157">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="cf4fc-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf4fc-158">Minimum supported server</span></span><br/> | <span data-ttu-id="cf4fc-159">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cf4fc-159">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="cf4fc-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="cf4fc-160">Namespace</span></span><br/>                | <span data-ttu-id="cf4fc-161">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="cf4fc-161">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cf4fc-162">MOF</span><span class="sxs-lookup"><span data-stu-id="cf4fc-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf4fc-163"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cf4fc-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf4fc-164">DLL</span><span class="sxs-lookup"><span data-stu-id="cf4fc-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf4fc-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cf4fc-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cf4fc-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf4fc-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf4fc-167">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="cf4fc-167">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

