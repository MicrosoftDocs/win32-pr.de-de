---
description: Ein Kommunikationsendpunkt, der eine Verbindung mit einem LAN herstellen kann, um Datenrahmen zu senden und zu empfangen. LAN-Endpunkte umfassen Ethernet-, Tokenring- und FDDI-Schnittstellen.
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
ms.openlocfilehash: 5e42f5edcc7010b9a84fdaaf3686208c9f82def03493c4c423aa3815b1d0758e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046810"
---
# <a name="cim_lanendpoint-class"></a>CIM \_ LANEndpoint-Klasse

Ein Kommunikationsendpunkt, der eine Verbindung mit einem LAN herstellen kann, um Datenrahmen zu senden und zu empfangen. LAN-Endpunkte umfassen Ethernet-, Tokenring- und FDDI-Schnittstellen.

## <a name="syntax"></a>Syntax

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

## <a name="members"></a>Member

Die **CIM \_ LANEndpoint-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ LANEndpoint-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AliasAddresses**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array, das andere Unicastadressen enthält, die für die Kommunikation mit dem LAN-Endpunkt verwendet werden können.

</dd> <dt>

**GroupAddresses**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array, das die Multicastadressen enthält, an denen der LAN-Endpunkt lausiert.

</dd> <dt>

**LANID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ LANConnectivitySegment.LANID, CIM \_ LANSegment.LANID")
</dt> </dl>

Eine Bezeichnung oder ein Bezeichner für das LAN-Segment, mit dem der Endpunkt verbunden ist. Wenn der Endpunkt derzeit nicht verbunden ist oder diese Informationen unbekannt sind, ist **LANID** NULL.

</dd> <dt>

**LANType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md).**ProtocolType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ LANConnectivitySegment.ConnectivityType, CIM \_ LANSegment.LANType")
</dt> </dl>

> [!Note]  
> Veraltete Beschreibung: Die Art der technologie, die im LAN verwendet wird.

 

Diese Eigenschaft ist veraltet. Stattdessen wird empfohlen, die **ProtocolType-Eigenschaft zu** verwenden.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (2)


</dt> <dd></dd> <dt>

<span id="TokenRing"></span><span id="tokenring"></span><span id="TOKENRING"></span>

**TokenRing** (3)


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

**FDDI** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**MACAddress**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12)
</dt> </dl>

Die vom LAN-Endpunkt verwendete Unicastadresse des Prinzipals.

Die MAC-Adresse muss mit den folgenden Merkmalen formatiert sein:

-   Die Adresse besteht aus zwölf Hexadezimalziffern.
-   Jedes Ziffernpaar stellt eines der sechs Oktette der MAC-Adresse dar.
-   Jedes Ziffernpaar muss gemäß RFC 2469 in kanonischer Bit reihenfolge sein.

</dd> <dt>

**MaxDataSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")
</dt> </dl>

Die maximale Größe der vom LAN-Endpunkt gesendeten oder empfangenen Datenfelder in Bytes.

</dd> <dt>

**OtherLANType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md).**OtherTypeDescription**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ LANConnectivitySegment.OtherTypeDescription", "**CIM \_ LANEndpoint**.**LANType**")
</dt> </dl>

> [!Note]  
> Veraltete Beschreibung: Der Typ der Technologie, die im LAN verwendet wird, wenn die **LANType-Eigenschaft** auf "1" (Sonstige) festgelegt ist.

 

Diese Eigenschaft ist veraltet. Stattdessen wird empfohlen, die **OtherTypeDescription-Eigenschaft zu** verwenden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md)
</dt> </dl>

 

