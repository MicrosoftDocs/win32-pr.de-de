---
description: Stellt die verfügbaren Anbieter für die Replikation dar.
ms.assetid: CAAD1CFC-6473-4642-8366-0A5625AE1F70
title: Msvm_ReplicationProvider-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationProvider
- Msvm_ReplicationProvider.InstanceID
- Msvm_ReplicationProvider.Caption
- Msvm_ReplicationProvider.Description
- Msvm_ReplicationProvider.ElementName
- Msvm_ReplicationProvider.Name
- Msvm_ReplicationProvider.OperationalStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8cc821b6bdd5d6f5d1c1085a804799c662f9d62e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865520"
---
# <a name="msvm_replicationprovider-class"></a>MSVM \_ replicationprovider-Klasse

Stellt die verfügbaren Anbieter für die Replikation dar.

Die folgende Syntax wird aus dem MOF-Code vereinfacht und enthält diese geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationProvider : CIM_ManagedSystemElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string Name;
  uint16 OperationalStatus[];
};
```

## <a name="members"></a>Member

Die **MSVM- \_ replicationprovider** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM- \_ replicationprovider** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **maxlen** (64)
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt. Für dieses Objekt lautet der Wert:

"Replikations Anbieter"

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt. Für externe Anbieter wird der Wert von Ihnen bereitgestellt. Für Host zum Hosten des integrierten Anbieters lautet der Wert:

"Replikations Anbieter für virtuelle Computer auf Hyper-V-Host"

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für den Endpunkt Anbieter. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

Damit Host den integrierten Anbieter hostet, wird diese Eigenschaft immer auf festgelegt:

"Replikations Anbieter für virtuelle Computer auf Hyper-V-Host"

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Key**, **maxlen** (256)
</dt> </dl>

Die WMI-Instanz-ID, die den Anbieter identifiziert. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt. Das Format dieser Eigenschaft ist "Microsoft: <Host-Computername>\\ replicationprovider \\<Provider-Name>".

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der Globally Unique Identifier (GUID) des Anbieters, der den Endpunkt Anbieter identifiziert. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

Bei einem externen Anbieter ist diese Eigenschaft die CLSID des COM-Klassen Objekts des Anbieters. Damit Host den integrierten Anbieter hostet, wird diese Eigenschaft wie folgt korrigiert:

"22391cdc-272c-4ddf-ba88-9bebb1a0975c"

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die aktuellen Status des-Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Array Element ist immer auf festgelegt:

<dl> <dt>

<span id="S_OK"></span><span id="s_ok"></span>**S \_ OK** (2)
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Zum Aktivieren einer Replikations Beziehung können Sie einen beliebigen verfügbaren Anbieter und die [**MSVM \_ replicationrelationship**](msvm-replicationrelationship.md) -Klasse verwenden. Standardmäßig wählt Hyper-V den integrierten Host zum Hosten des Anbieters aus, der beim Erstellen der Replikation geändert werden kann. Der Hyper-V-Verwaltungsdienst kommuniziert mit einem externen Anbieter mithilfe von com.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)
</dt> <dt>

[**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)
</dt> </dl>

 

