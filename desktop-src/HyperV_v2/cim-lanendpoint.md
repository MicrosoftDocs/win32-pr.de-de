---
description: Ein Kommunikations Endpunkt, der eine Verbindung mit einem LAN herstellen kann, um Datenrahmen zu senden und zu empfangen. Zu den LAN-Endpunkten gehören Ethernet-, TokenRing-und sddi-Schnittstellen.
ms.assetid: c69464cf-00a9-476d-a494-2d7d65776334
title: CIM_LANEndpoint-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LANEndpoint
- CIM_LANEndpoint.LANID
- CIM_LANEndpoint.LANType
- CIM_LANEndpoint.OtherLANType
- CIM_LANEndpoint.MACAddress
- CIM_LANEndpoint.AliasAddresses
- CIM_LANEndpoint.GroupAddresses
- CIM_LANEndpoint.MaxDataSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c924d175cb48e53346daff59a6317a4a0f241f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354876"
---
# <a name="cim_lanendpoint-class"></a><span data-ttu-id="06cba-104">CIM \_ lanendpoint-Klasse</span><span class="sxs-lookup"><span data-stu-id="06cba-104">CIM\_LANEndpoint class</span></span>

<span data-ttu-id="06cba-105">Ein Kommunikations Endpunkt, der eine Verbindung mit einem LAN herstellen kann, um Datenrahmen zu senden und zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="06cba-105">A communication endpoint that can connect to a LAN to send and receive data frames.</span></span> <span data-ttu-id="06cba-106">Zu den LAN-Endpunkten gehören Ethernet-, TokenRing-und sddi-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="06cba-106">LAN endpoints include ethernet, token Ring, and FDDI interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="06cba-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="06cba-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints"), AMENDMENT]
class CIM_LANEndpoint : CIM_ProtocolEndpoint
{
  string LANID;
  uint16 LANType;
  string OtherLANType;
  string MACAddress;
  string AliasAddresses[];
  string GroupAddresses[];
  uint32 MaxDataSize;
};
```

## <a name="members"></a><span data-ttu-id="06cba-108">Member</span><span class="sxs-lookup"><span data-stu-id="06cba-108">Members</span></span>

<span data-ttu-id="06cba-109">Die **CIM \_ lanendpoint** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="06cba-109">The **CIM\_LANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="06cba-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="06cba-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="06cba-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="06cba-111">Properties</span></span>

<span data-ttu-id="06cba-112">Die **CIM \_ lanendpoint** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="06cba-112">The **CIM\_LANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06cba-113">**Aliasadressen**</span><span class="sxs-lookup"><span data-stu-id="06cba-113">**AliasAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06cba-114">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="06cba-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="06cba-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="06cba-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06cba-116">Ein Array, das andere Unicastadressen enthält, die für die Kommunikation mit dem LAN-Endpunkt verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="06cba-116">An array that contains other unicast addresses that may be used to communicate with the LAN endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="06cba-117">**Groupadressen**</span><span class="sxs-lookup"><span data-stu-id="06cba-117">**GroupAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06cba-118">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="06cba-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="06cba-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="06cba-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06cba-120">Ein Array, das die Multicast Adressen enthält, auf die der LAN-Endpunkt lauscht.</span><span class="sxs-lookup"><span data-stu-id="06cba-120">An array that contains the multicast addresses to which the LAN endpoint listens.</span></span>

</dd> <dt>

<span data-ttu-id="06cba-121">**Lanid**</span><span class="sxs-lookup"><span data-stu-id="06cba-121">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06cba-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="06cba-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06cba-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="06cba-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06cba-124">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ lanconnectivitysegment. lanid, CIM \_ lansegment. lanid")</span><span class="sxs-lookup"><span data-stu-id="06cba-124">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_LANConnectivitySegment.LANID, CIM\_LANSegment.LANID")</span></span>
</dt> </dl>

<span data-ttu-id="06cba-125">Eine Bezeichnung oder ein Bezeichner für das LAN-Segment, mit dem der Endpunkt verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="06cba-125">A label or identifier for the LAN segment to which the endpoint is connected.</span></span> <span data-ttu-id="06cba-126">Wenn der Endpunkt derzeit nicht verbunden ist oder diese Informationen unbekannt sind, ist **lanid** NULL.</span><span class="sxs-lookup"><span data-stu-id="06cba-126">If the endpoint is not currently connected or if this information is unknown, then **LANID** is NULL.</span></span>

</dd> <dt>

<span data-ttu-id="06cba-127">**Lantype**</span><span class="sxs-lookup"><span data-stu-id="06cba-127">**LANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06cba-128">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06cba-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06cba-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="06cba-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06cba-130">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ protocolendpoint**](cim-protocolendpoint.md).**ProtocolType**"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ lanconnectivitysegment. connectivitytype, CIM \_ lansegment. lantype ")</span><span class="sxs-lookup"><span data-stu-id="06cba-130">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md).**ProtocolType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_LANConnectivitySegment.ConnectivityType, CIM\_LANSegment.LANType")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="06cba-131">Veraltete Beschreibung: die Art der im LAN verwendeten Technologie.</span><span class="sxs-lookup"><span data-stu-id="06cba-131">Deprecated description: The kind of technology used on the LAN.</span></span>

 

<span data-ttu-id="06cba-132">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="06cba-132">This property is deprecated.</span></span> <span data-ttu-id="06cba-133">Stattdessen wird empfohlen, die **ProtocolType** -Eigenschaft zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="06cba-133">Instead we recommend that you use the **ProtocolType** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06cba-134">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="06cba-134">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="06cba-135">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="06cba-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="06cba-136">**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="06cba-136">**Ethernet** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TokenRing"></span><span id="tokenring"></span><span id="TOKENRING"></span>

<span data-ttu-id="06cba-137">**TokenRing** (3)</span><span class="sxs-lookup"><span data-stu-id="06cba-137">**TokenRing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="06cba-138">" **F** " (4)</span><span class="sxs-lookup"><span data-stu-id="06cba-138">**FDDI** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06cba-139">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="06cba-139">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06cba-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="06cba-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06cba-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="06cba-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06cba-142">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (12)</span><span class="sxs-lookup"><span data-stu-id="06cba-142">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12)</span></span>
</dt> </dl>

<span data-ttu-id="06cba-143">Die vom LAN-Endpunkt verwendete Prinzipal-Unicastadresse.</span><span class="sxs-lookup"><span data-stu-id="06cba-143">The principal unicast address used by the LAN endpoint.</span></span>

<span data-ttu-id="06cba-144">Die Mac-Adresse muss mit den folgenden Merkmalen formatiert sein:</span><span class="sxs-lookup"><span data-stu-id="06cba-144">The MAC address must be formatted with the following characteristics:</span></span>

-   <span data-ttu-id="06cba-145">Die Adresse besteht aus zwölf hexadezimalen Ziffern.</span><span class="sxs-lookup"><span data-stu-id="06cba-145">The address consists of twelve hexadecimal digits.</span></span>
-   <span data-ttu-id="06cba-146">Jedes Ziffern paar stellt einen der sechs Oktette der Mac-Adresse dar.</span><span class="sxs-lookup"><span data-stu-id="06cba-146">Each pair of digits represents one of the six octets of the MAC address.</span></span>
-   <span data-ttu-id="06cba-147">Jedes Ziffern Paar muss gemäß RFC 2469 in kanonischer bitreihenfolge vorliegen.</span><span class="sxs-lookup"><span data-stu-id="06cba-147">Each pair of digits must be in canonical bit order according to RFC 2469.</span></span>

</dd> <dt>

<span data-ttu-id="06cba-148">**Maxdatasize**</span><span class="sxs-lookup"><span data-stu-id="06cba-148">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06cba-149">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="06cba-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06cba-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="06cba-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06cba-151">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")</span><span class="sxs-lookup"><span data-stu-id="06cba-151">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="06cba-152">Die maximale Größe (in Bytes) der vom LAN-Endpunkt gesendeten oder empfangenen Datenfelder.</span><span class="sxs-lookup"><span data-stu-id="06cba-152">The maximum size, in bytes, of data fields sent or received by the LAN endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="06cba-153">**Otherlantype**</span><span class="sxs-lookup"><span data-stu-id="06cba-153">**OtherLANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06cba-154">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="06cba-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06cba-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="06cba-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06cba-156">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ protocolendpoint**](cim-protocolendpoint.md).**OtherTypeDescription**"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ lanconnectivitysegment. OtherTypeDescription ","**CIM \_ lanendpoint**".**Lantype**")</span><span class="sxs-lookup"><span data-stu-id="06cba-156">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md).**OtherTypeDescription**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_LANConnectivitySegment.OtherTypeDescription", "**CIM\_LANEndpoint**.**LANType**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="06cba-157">Deprecated Description: der Typ der im LAN verwendeten Technologie, wenn die Eigenschaft **lantype** auf "1" (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="06cba-157">Deprecated description: The type of technology used on the LAN when the **LANType** property is set to "1" (Other).</span></span>

 

<span data-ttu-id="06cba-158">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="06cba-158">This property is deprecated.</span></span> <span data-ttu-id="06cba-159">Stattdessen wird empfohlen, die **OtherTypeDescription** -Eigenschaft zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="06cba-159">Instead we recommend that you use the **OtherTypeDescription** property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="06cba-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06cba-160">Requirements</span></span>



| <span data-ttu-id="06cba-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06cba-161">Requirement</span></span> | <span data-ttu-id="06cba-162">Wert</span><span class="sxs-lookup"><span data-stu-id="06cba-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06cba-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06cba-163">Minimum supported client</span></span><br/> | <span data-ttu-id="06cba-164">Windows 8</span><span class="sxs-lookup"><span data-stu-id="06cba-164">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="06cba-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06cba-165">Minimum supported server</span></span><br/> | <span data-ttu-id="06cba-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="06cba-166">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="06cba-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="06cba-167">Namespace</span></span><br/>                | <span data-ttu-id="06cba-168">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="06cba-168">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="06cba-169">MOF</span><span class="sxs-lookup"><span data-stu-id="06cba-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06cba-170"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="06cba-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="06cba-171">DLL</span><span class="sxs-lookup"><span data-stu-id="06cba-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06cba-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="06cba-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="06cba-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06cba-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06cba-174">**CIM- \_ protocolendpoint**</span><span class="sxs-lookup"><span data-stu-id="06cba-174">**CIM\_ProtocolEndpoint**</span></span>](cim-protocolendpoint.md)
</dt> </dl>

 

