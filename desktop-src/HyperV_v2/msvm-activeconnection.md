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
ms.openlocfilehash: cf682fac419658785cfe7594aa6fc17e4b2dd28e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867307"
---
# <a name="msvm_activeconnection-class"></a>MSVM \_ ActiveConnection-Klasse

Verbindet einen Switchport mit dem LAN-Endpunkt, mit dem der Port verbunden ist. Das vorhanden sein dieses Objekts bedeutet, dass der Switchport und der LAN-Endpunkt aktiv verbunden sind und der Ethernet-Port, der dem LAN-Endpunkt zugeordnet ist, über den Switchport mit dem Netzwerk kommunizieren kann.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

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

Die **MSVM \_ ActiveConnection** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ ActiveConnection** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ lanendpoint**](msvm-lanendpoint.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")
</dt> </dl>

Ein Verweis auf eine Instanz der [**MSVM \_ lanendpoint**](msvm-lanendpoint.md) -Klasse, die den Dienst Zugriffspunkt (SAP) darstellt, der für die Kommunikation oder aktive Kommunikation mit dem abhängigen SAP konfiguriert ist. Bei einer unidirektionalen Verbindung handelt es sich bei diesem SAP um das, das übertragen wird.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ lanendpoint**](cim-lanendpoint.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")
</dt> </dl>

Ein Verweis auf eine Instanz der [**MSVM \_ lanendpoint**](cim-lanendpoint.md) -Klasse, die den SAP darstellt, der für die Kommunikation konfiguriert ist oder aktiv mit dem Vorgänger-SAP kommuniziert. Bei einer unidirektionalen Verbindung handelt es sich bei diesem SAP um den, der empfängt.

</dd> <dt>

**Isunidirektional**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wenn diese Eigenschaft den Wert **true** hat, ist diese Verbindung unidirektional. Andernfalls ist diese Verbindung bidirektional. Wenn eine Verbindung unidirektional ist, sollte der "Sprecher" als **vorangehende** Verweis definiert werden. Bei einer bidirektionalen Verbindung spielt es keine Rolle, ob der ausgewählte Zugriffspunkt der **Vorgänger** oder der **abhängige** ist. Diese Eigenschaft wird von [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))geerbt.

</dd> <dt>

**Othertrafficdescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))geerbt, aber nicht verwendet.

</dd> <dt>

**TrafficType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft wird von [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))geerbt, aber nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM \_ ActiveConnection** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Beispiele

Weitere Informationen finden Sie unter [Abfragen von Netzwerk Objekten](querying-networking-objects.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ ActiveConnection**](cim-activeconnection.md)
</dt> <dt>

[**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))
</dt> </dl>

 

