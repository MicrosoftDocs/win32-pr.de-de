---
description: Definiert eine Verbindung, die derzeit aktiviert und für die Kommunikation zwischen zwei CIM \_ ServiceAccessPoint-Objekten konfiguriert ist.
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
ms.openlocfilehash: a2961779744e90d0e4281e53c3d78c92081993027deb6c435846abbffb41b110
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041760"
---
# <a name="cim_activeconnection-class"></a>CIM \_ ActiveConnection-Klasse

Definiert eine Verbindung, die derzeit aktiviert und für die Kommunikation zwischen zwei **CIM \_ ServiceAccessPoint-Objekten** konfiguriert ist. **CIM \_ ActiveConnection** wird verwendet, wenn die Verbindung nicht als **CIM \_ ManagedElement-Objekt** behandelt wird. Dienstzugriffspunkte, die über eine aktive Verbindung verbunden sind, befinden sich in der Regel auf derselben Netzwerk- oder Anwendungsschicht.

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

Die **CIM \_ ActiveConnection-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ ActiveConnection-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ServiceAccessPoint**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")
</dt> </dl>

Der Dienstzugriffspunkt, der über die aktive Verbindung mit dem anderen Dienstzugriffspunkt verbunden ist. **CIM \_ ServiceAccessPoint-Objekt.** Bei einer unidirektionalen Verbindung ist dieser Zugriffspunkt der, der Daten überträgt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ServiceAccessPoint**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")
</dt> </dl>

Der Dienstzugriffspunkt, der für die Kommunikation konfiguriert ist oder aktiv mit dem Dienstzugriffspunkt kommuniziert, der in der **Vorgängereigenschaft** angegeben ist. Bei einer unidirektionalen Verbindung ist dieser Zugriffspunkt der, der Daten empfängt.

</dd> <dt>

**IsUnidirectional**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

TRUE, wenn die Verbindung unidirektional ist; FALSE, wenn die Verbindung bidirektional ist. Wenn die Verbindung unidirektional ist, gibt die **Eigenschaft Vorgänger** den Zugriffspunkt an, der Daten überträgt. In einer bidirektionalen Verbindung kann **Antecedent** einen der Verbindung zugewiesenen Zugriffspunkt angeben.

</dd> <dt>

**OtherTrafficDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Kein Wert"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ActiveConnection**.**TrafficType**")
</dt> </dl>

> [!Note]  
> Diese Eigenschaft ist veraltet. Stattdessen wird empfohlen, diese Informationen in der Adressierung, dem Protokoll und den grundlegenden Funktionen der Endpunkte anzugeben.

 

Eine Beschreibung des Datenverkehrstyps, der angegeben wird, wenn die **TrafficType-Eigenschaft** auf "1" (Sonstige) festgelegt ist.

</dd> <dt>

**TrafficType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Kein Wert"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ActiveConnection**.**OtherTrafficDescription**")
</dt> </dl>

> [!Note]  
> Diese Eigenschaft ist veraltet. Stattdessen wird empfohlen, diese Informationen in der Adressierung, dem Protokoll und den grundlegenden Funktionen der Endpunkte anzugeben.

 

Der Typ des Datenverkehrs, der über diese Verbindung übertragen wird.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Andere** (1)


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
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ SAPSAPDependency**](cim-sapsapdependency.md)
</dt> </dl>

 

