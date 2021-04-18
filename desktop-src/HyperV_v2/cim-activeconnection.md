---
description: Definiert eine Verbindung, die derzeit aktiviert und konfiguriert ist, um die Kommunikation zwischen zwei CIM \_ serviceaccesspoint-Objekten bereitzustellen.
ms.assetid: 03f8e43f-a77b-46e2-bb7d-c29758c65aee
title: CIM_ActiveConnection-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActiveConnection
- CIM_ActiveConnection.Antecedent
- CIM_ActiveConnection.Dependent
- CIM_ActiveConnection.TrafficType
- CIM_ActiveConnection.OtherTrafficDescription
- CIM_ActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 644e8aaae1368e4164ceca7f7db29e343116c93c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368172"
---
# <a name="cim_activeconnection-class"></a><span data-ttu-id="204e8-103">CIM \_ ActiveConnection-Klasse</span><span class="sxs-lookup"><span data-stu-id="204e8-103">CIM\_ActiveConnection class</span></span>

<span data-ttu-id="204e8-104">Definiert eine Verbindung, die derzeit aktiviert und konfiguriert ist, um die Kommunikation zwischen zwei **CIM \_ serviceaccesspoint** -Objekten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="204e8-104">Defines a connection that is currently turned on and configured to provide communication between two **CIM\_ServiceAccessPoint** objects.</span></span> <span data-ttu-id="204e8-105">**CIM \_ ActiveConnection** wird verwendet, wenn die Verbindung nicht als **CIM \_ managedelta** -Objekt behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="204e8-105">**CIM\_ActiveConnection** is used when the connection is not treated as a **CIM\_ManagedElement** object.</span></span> <span data-ttu-id="204e8-106">Dienst Zugriffspunkte, die über eine aktive Verbindung verbunden sind, befinden sich in der Regel auf derselben Netzwerk-oder Anwendungsebene.</span><span class="sxs-lookup"><span data-stu-id="204e8-106">Service access points that are connected by an active connection are typically at the same networking or application layer.</span></span>

## <a name="syntax"></a><span data-ttu-id="204e8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="204e8-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ActiveConnection : CIM_SAPSAPDependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
  uint16                     TrafficType;
  string                     OtherTrafficDescription;
  boolean                    IsUnidirectional;
};
```

## <a name="members"></a><span data-ttu-id="204e8-108">Member</span><span class="sxs-lookup"><span data-stu-id="204e8-108">Members</span></span>

<span data-ttu-id="204e8-109">Die **CIM \_ ActiveConnection** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="204e8-109">The **CIM\_ActiveConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="204e8-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="204e8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="204e8-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="204e8-111">Properties</span></span>

<span data-ttu-id="204e8-112">Die **CIM \_ ActiveConnection** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="204e8-112">The **CIM\_ActiveConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="204e8-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="204e8-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="204e8-114">Datentyp: **CIM \_ serviceaccesspoint**</span><span class="sxs-lookup"><span data-stu-id="204e8-114">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="204e8-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="204e8-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="204e8-116">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="204e8-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="204e8-117">Der Dienst Zugriffspunkt, der über die aktive Verbindung mit dem anderen Dienst Zugriffspunkt verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="204e8-117">The service access point that is connected to the other service access point through the active connection.</span></span> <span data-ttu-id="204e8-118">**CIM \_ Serviceaccesspoint** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="204e8-118">**CIM\_ServiceAccessPoint** object.</span></span> <span data-ttu-id="204e8-119">Bei einer unidirektionalen Verbindung handelt es sich bei diesem Zugriffspunkt um den Zugriffspunkt, der Daten überträgt.</span><span class="sxs-lookup"><span data-stu-id="204e8-119">In a unidirectional connection, this access point is the one that is transmitting data.</span></span>

</dd> <dt>

<span data-ttu-id="204e8-120">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="204e8-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="204e8-121">Datentyp: **CIM \_ serviceaccesspoint**</span><span class="sxs-lookup"><span data-stu-id="204e8-121">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="204e8-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="204e8-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="204e8-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="204e8-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="204e8-124">Der Dienst Zugriffspunkt, der für die Kommunikation oder die aktive Kommunikation mit dem Dienst Zugriffspunkt konfiguriert ist, der in der **Vorgänger** Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="204e8-124">The service access point that is configured to communicate or is actively communicating with the service access point specified in the **Antecedent** property.</span></span> <span data-ttu-id="204e8-125">Bei einer unidirektionalen Verbindung ist dieser Zugriffspunkt derjenige, der Daten empfängt.</span><span class="sxs-lookup"><span data-stu-id="204e8-125">In a unidirectional connection, this access point is the one that is receiving data.</span></span>

</dd> <dt>

<span data-ttu-id="204e8-126">**Isunidirektional**</span><span class="sxs-lookup"><span data-stu-id="204e8-126">**IsUnidirectional**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="204e8-127">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="204e8-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="204e8-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="204e8-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="204e8-129">True, wenn die Verbindung unidirektional ist. false, wenn die Verbindung bidirektional ist.</span><span class="sxs-lookup"><span data-stu-id="204e8-129">True if the connection is unidirectional; false if the connection is bidirectional.</span></span> <span data-ttu-id="204e8-130">Wenn die Verbindung unidirektional ist, gibt die **Vorgänger** Eigenschaft den Zugriffspunkt an, der Daten überträgt.</span><span class="sxs-lookup"><span data-stu-id="204e8-130">When the connection is unidirectional, the **Antecedent** property specifies the access point that is transmitting data.</span></span> <span data-ttu-id="204e8-131">Bei einer bidirektionalen Verbindung kann der **Vorgänger** entweder einen Zugriffspunkt angeben, der der Verbindung zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="204e8-131">In a bidirectional connection, **Antecedent** can specify either access point assigned to the connection.</span></span>

</dd> <dt>

<span data-ttu-id="204e8-132">**Othertrafficdescription**</span><span class="sxs-lookup"><span data-stu-id="204e8-132">**OtherTrafficDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="204e8-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="204e8-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="204e8-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="204e8-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="204e8-135">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("kein Wert"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ActiveConnection**".**Traffictype**")</span><span class="sxs-lookup"><span data-stu-id="204e8-135">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ActiveConnection**.**TrafficType**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="204e8-136">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="204e8-136">This property is deprecated.</span></span> <span data-ttu-id="204e8-137">Stattdessen wird empfohlen, dass Sie diese Informationen in der Adressierungs-, Protokoll-und grundlegenden Funktionalität der Endpunkte angeben.</span><span class="sxs-lookup"><span data-stu-id="204e8-137">Instead, we recommend that you specify this information in the addressing, protocol, and basic functionality of the endpoints.</span></span>

 

<span data-ttu-id="204e8-138">Eine Beschreibung des Datenverkehrs Typs, der angegeben wird, wenn die **traffictype** -Eigenschaft auf "1" (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="204e8-138">A description of the traffic type that is specified when the **TrafficType** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="204e8-139">**TrafficType**</span><span class="sxs-lookup"><span data-stu-id="204e8-139">**TrafficType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="204e8-140">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="204e8-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="204e8-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="204e8-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="204e8-142">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("kein Wert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ActiveConnection**".**Othertrafficdescription**")</span><span class="sxs-lookup"><span data-stu-id="204e8-142">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ActiveConnection**.**OtherTrafficDescription**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="204e8-143">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="204e8-143">This property is deprecated.</span></span> <span data-ttu-id="204e8-144">Stattdessen wird empfohlen, dass Sie diese Informationen in der Adressierungs-, Protokoll-und grundlegenden Funktionalität der Endpunkte angeben.</span><span class="sxs-lookup"><span data-stu-id="204e8-144">Instead, we recommend that you specify this information in the addressing, protocol, and basic functionality of the endpoints.</span></span>

 

<span data-ttu-id="204e8-145">Der Typ des Datenverkehrs, der über diese Verbindung übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="204e8-145">The type of traffic that is transmitted over this connection.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="204e8-146">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="204e8-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="204e8-147">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="204e8-147">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicast"></span><span id="unicast"></span><span id="UNICAST"></span>

<span data-ttu-id="204e8-148">**Unicast** (2)</span><span class="sxs-lookup"><span data-stu-id="204e8-148">**Unicast** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Broadcast"></span><span id="broadcast"></span><span id="BROADCAST"></span>

<span data-ttu-id="204e8-149">**Broadcast** (3)</span><span class="sxs-lookup"><span data-stu-id="204e8-149">**Broadcast** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Multicast"></span><span id="multicast"></span><span id="MULTICAST"></span>

<span data-ttu-id="204e8-150">**Multicast** (4)</span><span class="sxs-lookup"><span data-stu-id="204e8-150">**Multicast** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Anycast"></span><span id="anycast"></span><span id="ANYCAST"></span>

<span data-ttu-id="204e8-151">**Anycast** (5)</span><span class="sxs-lookup"><span data-stu-id="204e8-151">**Anycast** (5)</span></span>


<span data-ttu-id="204e8-152"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="204e8-152"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="204e8-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="204e8-153">Requirements</span></span>



| <span data-ttu-id="204e8-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="204e8-154">Requirement</span></span> | <span data-ttu-id="204e8-155">Wert</span><span class="sxs-lookup"><span data-stu-id="204e8-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="204e8-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="204e8-156">Minimum supported client</span></span><br/> | <span data-ttu-id="204e8-157">Windows 8</span><span class="sxs-lookup"><span data-stu-id="204e8-157">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="204e8-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="204e8-158">Minimum supported server</span></span><br/> | <span data-ttu-id="204e8-159">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="204e8-159">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="204e8-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="204e8-160">Namespace</span></span><br/>                | <span data-ttu-id="204e8-161">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="204e8-161">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="204e8-162">MOF</span><span class="sxs-lookup"><span data-stu-id="204e8-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="204e8-163"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="204e8-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="204e8-164">DLL</span><span class="sxs-lookup"><span data-stu-id="204e8-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="204e8-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="204e8-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="204e8-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="204e8-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="204e8-167">**CIM \_ sapsapabhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="204e8-167">**CIM\_SAPSAPDependency**</span></span>](cim-sapsapdependency.md)
</dt> </dl>

 

