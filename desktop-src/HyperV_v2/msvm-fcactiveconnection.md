---
description: Verbindet einen Switchport mit dem Fibre Channel-Endpunkt, mit dem der Port verbunden ist.
ms.assetid: e2762e0c-2f78-4159-a67c-31213e311072
title: Msvm_FcActiveConnection-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcActiveConnection
- Msvm_FcActiveConnection.Antecedent
- Msvm_FcActiveConnection.Dependent
- Msvm_FcActiveConnection.TrafficType
- Msvm_FcActiveConnection.OtherTrafficDescription
- Msvm_FcActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e29330e073266f2f2a8749ec3c70d9e26b35ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345145"
---
# <a name="msvm_fcactiveconnection-class"></a>MSVM- \_ Klasse "ficactiveconnection"

Verbindet einen Switchport mit dem Fibre Channel-Endpunkt, mit dem der Port verbunden ist. Das vorhanden sein dieses Objekts bedeutet, dass der Switchport und der Fibre Channel Endpunkt aktiv verbunden sind und dass der Fibre Channel Port, der dem Fibre Channel Endpunkt zugeordnet ist, über den Switchport mit dem Netzwerk kommunizieren kann.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcActiveConnection : CIM_ActiveConnection
{
  Msvm_FcEndpoint REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
  uint16              TrafficType;
  string              OtherTrafficDescription;
  boolean             IsUnidirectional;
};
```

## <a name="members"></a>Member

Die **MSVM \_ fcactiveconnection** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM-Klasse " \_ ficactiveconnection** " verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **MSVM \_ fcendpoint**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")
</dt> </dl>

Ein Verweis auf eine Instanz der [**MSVM \_ fcendpoint**](msvm-fcendpoint.md) -Klasse, die den Dienst Zugriffspunkt (SAP) darstellt, der für die Kommunikation oder aktive Kommunikation mit dem abhängigen SAP konfiguriert ist. Bei einer unidirektionalen Verbindung handelt es sich bei diesem SAP um das, das übertragen wird.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **MSVM \_ fcendpoint**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")
</dt> </dl>

Ein Verweis auf eine Instanz der [**MSVM \_ fcendpoint**](msvm-fcendpoint.md) -Klasse, die den SAP darstellt, der für die Kommunikation oder aktive Kommunikation mit dem Vorgänger-SAP konfiguriert ist. Bei einer unidirektionalen Verbindung ist dieser SAP der empfangende SAP.

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

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

