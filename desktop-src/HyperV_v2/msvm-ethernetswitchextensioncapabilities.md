---
description: Stellt die Zuordnung zwischen Ethernet-Erweiterungen und ihren Funktionen dar.
ms.assetid: 6b32235a-175d-48f9-af3a-2d40f748a518
title: Msvm_EthernetSwitchExtensionCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchExtensionCapabilities
- Msvm_EthernetSwitchExtensionCapabilities.ManagedElement
- Msvm_EthernetSwitchExtensionCapabilities.Capabilities
- Msvm_EthernetSwitchExtensionCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 950a8a0288487bf557e9dd201100b2a894417641
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760855"
---
# <a name="msvm_ethernetswitchextensioncapabilities-class"></a>MSVM \_ ethernetzwitchextensionfunktionalitäten-Klasse

Stellt die Zuordnung zwischen Ethernet-Erweiterungen und ihren Funktionen dar.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchExtensionCapabilities : CIM_ElementCapabilities
{
  Msvm_InstalledEthernetSwitchExtension  REF ManagedElement;
  Msvm_EthernetSwitchFeatureCapabilities REF Capabilities;
  uint16                                     Characteristics[];
};
```

## <a name="members"></a>Member

Die **MSVM \_ ethernetzwitchextensionfunktionsklasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM-Klasse " \_ ethernetzwitchextensionfunktionalitäten** " verfügt über diese Eigenschaften.

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ ethernetungwitchfeatuerabilitäten**](msvm-ethernetswitchfeaturecapabilities.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Funktionen")
</dt> </dl>

Ein Verweis auf eine Instanz der [**MSVM-Klasse " \_ ethernetzwitchfeaturecapabili"**](msvm-ethernetswitchfeaturecapabilities.md) , die das dem Switch zugeordnete Objekt "Funktionen" darstellt. Diese Eigenschaft wird von [**CIM- \_ Element Funktionen**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)geerbt.

</dd> <dt>

**Characteristics**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Stellt beschreibende Informationen zu den Funktionen bereit. Diese Eigenschaft wird von [**CIM- \_ Element Funktionen**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)geerbt.



| Wert                                                                                                                                                                                                                       | Bedeutung                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <dt>**Standard**</dt> Wert <dt>2</dt> </dl> | Die zugehörigen Funktionen stellen die Standardfunktionen des verwalteten Elements dar.<br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <dt>**Aktuell**</dt> <dt>3</dt> </dl> | Die zugehörigen Funktionen stellen die aktuellen Funktionen des verwalteten Elements dar.<br/> |



 

</dd> <dt>

**"Managedelement"**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ installedethernetzwitchextension**](msvm-installedethernetswitchextension.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("managedelta")
</dt> </dl>

Ein Verweis auf eine Instanz der [**MSVM \_ installedethernetzwitchextension**](msvm-installedethernetswitchextension.md) -Klasse, die die installierte Erweiterung darstellt. Diese Eigenschaft wird von [**CIM- \_ Element Funktionen**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)geerbt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

