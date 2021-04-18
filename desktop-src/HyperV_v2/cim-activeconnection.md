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
# <a name="cim_activeconnection-class"></a>CIM \_ ActiveConnection-Klasse

Definiert eine Verbindung, die derzeit aktiviert und konfiguriert ist, um die Kommunikation zwischen zwei **CIM \_ serviceaccesspoint** -Objekten bereitzustellen. **CIM \_ ActiveConnection** wird verwendet, wenn die Verbindung nicht als **CIM \_ managedelta** -Objekt behandelt wird. Dienst Zugriffspunkte, die über eine aktive Verbindung verbunden sind, befinden sich in der Regel auf derselben Netzwerk-oder Anwendungsebene.

## <a name="syntax"></a>Syntax

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

## <a name="members"></a>Member

Die **CIM \_ ActiveConnection** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ ActiveConnection** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ serviceaccesspoint**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")
</dt> </dl>

Der Dienst Zugriffspunkt, der über die aktive Verbindung mit dem anderen Dienst Zugriffspunkt verbunden ist. **CIM \_ Serviceaccesspoint** -Objekt. Bei einer unidirektionalen Verbindung handelt es sich bei diesem Zugriffspunkt um den Zugriffspunkt, der Daten überträgt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ serviceaccesspoint**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")
</dt> </dl>

Der Dienst Zugriffspunkt, der für die Kommunikation oder die aktive Kommunikation mit dem Dienst Zugriffspunkt konfiguriert ist, der in der **Vorgänger** Eigenschaft angegeben ist. Bei einer unidirektionalen Verbindung ist dieser Zugriffspunkt derjenige, der Daten empfängt.

</dd> <dt>

**Isunidirektional**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True, wenn die Verbindung unidirektional ist. false, wenn die Verbindung bidirektional ist. Wenn die Verbindung unidirektional ist, gibt die **Vorgänger** Eigenschaft den Zugriffspunkt an, der Daten überträgt. Bei einer bidirektionalen Verbindung kann der **Vorgänger** entweder einen Zugriffspunkt angeben, der der Verbindung zugewiesen ist.

</dd> <dt>

**Othertrafficdescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("kein Wert"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ActiveConnection**".**Traffictype**")
</dt> </dl>

> [!Note]  
> Diese Eigenschaft ist veraltet. Stattdessen wird empfohlen, dass Sie diese Informationen in der Adressierungs-, Protokoll-und grundlegenden Funktionalität der Endpunkte angeben.

 

Eine Beschreibung des Datenverkehrs Typs, der angegeben wird, wenn die **traffictype** -Eigenschaft auf "1" (sonstige) festgelegt ist.

</dd> <dt>

**TrafficType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("kein Wert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ActiveConnection**".**Othertrafficdescription**")
</dt> </dl>

> [!Note]  
> Diese Eigenschaft ist veraltet. Stattdessen wird empfohlen, dass Sie diese Informationen in der Adressierungs-, Protokoll-und grundlegenden Funktionalität der Endpunkte angeben.

 

Der Typ des Datenverkehrs, der über diese Verbindung übertragen wird.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unicast"></span><span id="unicast"></span><span id="UNICAST"></span>

**Unicast** (2)


</dt> <dd></dd> <dt>

<span id="Broadcast"></span><span id="broadcast"></span><span id="BROADCAST"></span>

**Broadcast** (3)


</dt> <dd></dd> <dt>

<span id="Multicast"></span><span id="multicast"></span><span id="MULTICAST"></span>

**Multicast** (4)


</dt> <dd></dd> <dt>

<span id="Anycast"></span><span id="anycast"></span><span id="ANYCAST"></span>

**Anycast** (5)


</dt> <dd></dd> </dl>

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

[**CIM \_ sapsapabhängigkeit**](cim-sapsapdependency.md)
</dt> </dl>

 

