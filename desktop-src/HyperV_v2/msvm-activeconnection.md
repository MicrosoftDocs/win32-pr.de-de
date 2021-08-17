---
description: Verbindet einen Switchport mit dem LAN-Endpunkt, mit dem der Port verbunden ist.
ms.assetid: 963EC004-6A67-4F75-BD93-1BCD17F32490
title: Msvm_ActiveConnection-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ActiveConnection
- Msvm_ActiveConnection.Antecedent
- Msvm_ActiveConnection.Dependent
- Msvm_ActiveConnection.TrafficType
- Msvm_ActiveConnection.OtherTrafficDescription
- Msvm_ActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2f8326fe50d3fef4e7776fa865afdd730416cb38fccd6347b4b27f0079966501
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693610"
---
# <a name="msvm_activeconnection-class"></a>Msvm \_ ActiveConnection-Klasse

Verbindet einen Switchport mit dem LAN-Endpunkt, mit dem der Port verbunden ist. Das Vorhandensein dieses Objekts bedeutet, dass der Switchport und der LAN-Endpunkt aktiv verbunden sind und der ethernet-Port, der dem LAN-Endpunkt zugeordnet ist, über den Switchport mit dem Netzwerk kommunizieren kann.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ActiveConnection : CIM_ActiveConnection
{
  Msvm_LANEndpoint REF Antecedent;
  CIM_LANEndpoint  REF Dependent;
  uint16               TrafficType;
  string               OtherTrafficDescription;
  boolean              IsUnidirectional;
};
```

## <a name="members"></a>Member

Die **Msvm \_ ActiveConnection-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ ActiveConnection-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Msvm \_ LANEndpoint**](msvm-lanendpoint.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")
</dt> </dl>

Ein Verweis auf eine Instanz der [**Msvm \_ LANEndpoint-Klasse,**](msvm-lanendpoint.md) die den Dienstzugriffspunkt (SAP) darstellt, der für die Kommunikation konfiguriert ist oder aktiv mit dem abhängigen SAP kommuniziert. Bei einer unidirektionalen Verbindung wird diese SAP-Verbindung übertragen.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ LANEndpoint**](cim-lanendpoint.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")
</dt> </dl>

Ein Verweis auf eine Instanz der [**Msvm \_ LANEndpoint-Klasse,**](cim-lanendpoint.md) die den SAP darstellt, der für die Kommunikation konfiguriert ist oder aktiv mit dem vorgängerigen SAP kommuniziert. Bei einer unidirektionalen Verbindung ist dies die SAP-Verbindung, die empfängt.

</dd> <dt>

**IsUnidirectional**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wenn diese Eigenschaft **True** ist, ist diese Verbindung unidirektional. Andernfalls ist diese Verbindung bidirektional. Wenn eine Verbindung unidirektional ist, sollte der  "Sprecher" als Vorgängerverweis definiert werden. Bei einer bidirektionalen Verbindung spielt es keine Rolle, ob der ausgewählte Zugriffspunkt **der** Vorgänger oder **abhängig** ist. Diese Eigenschaft wird von [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))geerbt.

</dd> <dt>

**OtherTrafficDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))geerbt, aber nicht verwendet.

</dd> <dt>

**TrafficType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))geerbt, aber nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ ActiveConnection-Klasse** kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Beispiele

Weitere Informationen finden Sie unter [Abfragen von Netzwerkobjekten.](querying-networking-objects.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ ActiveConnection**](cim-activeconnection.md)
</dt> <dt>

[**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))
</dt> </dl>

 

