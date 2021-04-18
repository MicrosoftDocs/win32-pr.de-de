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
# <a name="cim_lanendpoint-class"></a>CIM \_ lanendpoint-Klasse

Ein Kommunikations Endpunkt, der eine Verbindung mit einem LAN herstellen kann, um Datenrahmen zu senden und zu empfangen. Zu den LAN-Endpunkten gehören Ethernet-, TokenRing-und sddi-Schnittstellen.

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

Die **CIM \_ lanendpoint** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ lanendpoint** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Aliasadressen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array, das andere Unicastadressen enthält, die für die Kommunikation mit dem LAN-Endpunkt verwendet werden können.

</dd> <dt>

**Groupadressen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array, das die Multicast Adressen enthält, auf die der LAN-Endpunkt lauscht.

</dd> <dt>

**Lanid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ lanconnectivitysegment. lanid, CIM \_ lansegment. lanid")
</dt> </dl>

Eine Bezeichnung oder ein Bezeichner für das LAN-Segment, mit dem der Endpunkt verbunden ist. Wenn der Endpunkt derzeit nicht verbunden ist oder diese Informationen unbekannt sind, ist **lanid** NULL.

</dd> <dt>

**Lantype**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ protocolendpoint**](cim-protocolendpoint.md).**ProtocolType**"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ lanconnectivitysegment. connectivitytype, CIM \_ lansegment. lantype ")
</dt> </dl>

> [!Note]  
> Veraltete Beschreibung: die Art der im LAN verwendeten Technologie.

 

Diese Eigenschaft ist veraltet. Stattdessen wird empfohlen, die **ProtocolType** -Eigenschaft zu verwenden.

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

" **F** " (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**MACAddress**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (12)
</dt> </dl>

Die vom LAN-Endpunkt verwendete Prinzipal-Unicastadresse.

Die Mac-Adresse muss mit den folgenden Merkmalen formatiert sein:

-   Die Adresse besteht aus zwölf hexadezimalen Ziffern.
-   Jedes Ziffern paar stellt einen der sechs Oktette der Mac-Adresse dar.
-   Jedes Ziffern Paar muss gemäß RFC 2469 in kanonischer bitreihenfolge vorliegen.

</dd> <dt>

**Maxdatasize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")
</dt> </dl>

Die maximale Größe (in Bytes) der vom LAN-Endpunkt gesendeten oder empfangenen Datenfelder.

</dd> <dt>

**Otherlantype**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ protocolendpoint**](cim-protocolendpoint.md).**OtherTypeDescription**"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ lanconnectivitysegment. OtherTypeDescription ","**CIM \_ lanendpoint**".**Lantype**")
</dt> </dl>

> [!Note]  
> Deprecated Description: der Typ der im LAN verwendeten Technologie, wenn die Eigenschaft **lantype** auf "1" (sonstige) festgelegt ist.

 

Diese Eigenschaft ist veraltet. Stattdessen wird empfohlen, die **OtherTypeDescription** -Eigenschaft zu verwenden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ protocolendpoint**](cim-protocolendpoint.md)
</dt> </dl>

 

