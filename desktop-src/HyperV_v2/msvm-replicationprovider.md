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
ms.openlocfilehash: 84b64ec1462d9d3cb487cac807891d57c219de7f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885700"
---
# <a name="msvm_replicationprovider-class"></a>Msvm \_ ReplicationProvider-Klasse

Stellt die verfügbaren Anbieter für die Replikation dar.

Die folgende Syntax wird aus MOF-Code vereinfacht und enthält diese geerbten Eigenschaften.

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

Die **Msvm \_ ReplicationProvider-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ ReplicationProvider-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** (64)
</dt> </dl>

Eine kurze Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt. Für dieses Objekt lautet der Wert:

"Replikationsanbieter"

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt. Für externe Anbieter wird der Wert von ihnen bereitgestellt. Der Wert für host to host inbuilt provider lautet:

"Vm-Replikationsanbieter auf Hyper-V-Host"

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für den Endpunktanbieter. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

Für den Host zum Hosten des inbuilten Anbieters ist diese Eigenschaft immer auf festgelegt:

"Vm-Replikationsanbieter auf Hyper-V-Host"

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel,** **MaxLen** (256)
</dt> </dl>

Die WMI-Instanz-ID, die den Anbieter identifiziert. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt. Das Format dieser Eigenschaft lautet "Microsoft: &lt; host-machine-name &gt; \\ ReplicationProvider \\ &lt; provider-Name". &gt;

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel,**](/windows/desktop/WmiSdk/key-qualifier) [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der GUID (Globally Unique Identifier) des Anbieters, der den Endpunktanbieter identifiziert. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt.

Bei einem externen Anbieter ist diese Eigenschaft die CLSID des COM-Klassenobjekts des Anbieters. Für host to host inbuilt provider (Host zum Hosten des inbuilten Anbieters) wird diese Eigenschaft wie hier festgelegt:

"22391CDC-272C-4DDF-BA88-9BEFB1A0975C"

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die aktuellen Status des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)geerbt, und jedes Arrayelement ist immer auf festgelegt:

<dl> <dt>

<span id="S_OK"></span><span id="s_ok"></span>**S \_ OK** (2)
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie können einen beliebigen verfügbaren Anbieter und die [**Msvm \_ ReplicationRelationship-Klasse**](msvm-replicationrelationship.md) verwenden, um eine Replikationsbeziehung zu aktivieren. Hyper-V wählt standardmäßig den integrierte Host zum Hostanbieter aus, der beim Erstellen der Replikation geändert werden kann. Der Hyper-V-Verwaltungsdienst kommuniziert mit einem externen Anbieter über COM.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)
</dt> <dt>

[**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)
</dt> </dl>

 

