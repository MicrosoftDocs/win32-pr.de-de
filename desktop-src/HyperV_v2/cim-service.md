---
description: Stellt ein logisches Element dar, das Informationen zum Darstellen und Verwalten der funktionalität enthält, die von einem Geräte- oder Softwarefeature bereitgestellt wird.
ms.assetid: 0b2312da-433b-43d8-8d21-babab12a5b2c
title: CIM_Service-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service
- CIM_Service.SystemCreationClassName
- CIM_Service.SystemName
- CIM_Service.CreationClassName
- CIM_Service.Name
- CIM_Service.PrimaryOwnerName
- CIM_Service.PrimaryOwnerContact
- CIM_Service.StartMode
- CIM_Service.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fc6182ce024b616c49552cf13878d9ec06da97bd0d0b4c7ff3696e7747a943a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899860"
---
# <a name="cim_service-class-hyper-v-management"></a>CIM_Service-Klasse (Hyper-V-Verwaltung)

Stellt ein logisches Element dar, das Informationen zum Darstellen und Verwalten der funktionalität enthält, die von einem Geräte- oder Softwarefeature bereitgestellt wird. Ein Dienst ist ein allgemeines Objekt zum Konfigurieren und Verwalten der Implementierung von Funktionen. es ist nicht die Funktionalität selbst.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_Service : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  string  Name;
  string  PrimaryOwnerName;
  string  PrimaryOwnerContact;
  string  StartMode;
  boolean Started;
};
```

## <a name="members"></a>Member

Die **\_ CIM-Dienstklasse** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **\_ CIM-Dienstklasse** verfügt über diese Methoden.



| Methode                                           | BESCHREIBUNG                    |
|:-------------------------------------------------|:-------------------------------|
| [**Startservice**](cim-service-startservice.md) | Startet den Dienst.<br/> |
| [**StopService**](cim-service-stopservice.md)   | Beendet den Dienst.<br/>  |



 

### <a name="properties"></a>Eigenschaften

Die **\_ CIM-Dienstklasse** verfügt über diese Eigenschaften.

<dl> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel,**](/windows/desktop/WmiSdk/key-qualifier) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der Klassenname, der zum Erstellen einer Instanz dieser Klasse verwendet wird. **CreationClassName** wird mit anderen Schlüsseleigenschaften dieser Klasse kombiniert, um Instanzen dieser Klasse und deren Unterklassen eindeutig zu identifizieren.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel,**](/windows/desktop/WmiSdk/key-qualifier) [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Ein eindeutiger Bezeichner des Diensts, der die Funktionalität des Diensts angibt.

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| General Information \| 001.4")
</dt> </dl>

Kontaktinformationen für den primären Besitzer des Diensts.

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| General Information \| 001.3")
</dt> </dl>

Der Name des primären Besitzers des Diensts.

</dd> <dt>

**Begann**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**TRUE,** wenn der Dienst gestartet wurde; andernfalls **FALSE.**

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**\_ CIM-Dienst**.**EnabledDefault**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Diese Eigenschaft ist veraltet. Verwenden Sie stattdessen die **EnabledDefault-Eigenschaft,** die von [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md)geerbt wird.

> [!Note]  
> Veraltete Beschreibung: Gibt an, ob der Dienst automatisch gestartet wird (z. B. durch ein Betriebssystem) oder nur auf Anforderung gestartet wird.

 

<dt>



 ("Automatisch")


</dt> <dd></dd> <dt>



 ("Manuell")


</dt> <dd></dd> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**weitergegeben**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ CIM-System**](cim-system.md).**CreationClassName**")
</dt> </dl>

Der Klassenname, der zum Erstellen einer Instanz des Systems verwendet wird, das den Dienst enthält. **SystemCreationClassName** wird mit anderen Schlüsseleigenschaften dieser Klasse kombiniert, um Instanzen dieser Klasse und deren Unterklassen eindeutig zu identifizieren.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**weitergegeben**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ CIM-System**](cim-system.md).**Name**")
</dt> </dl>

Der Name des Bereichssystems.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md)
</dt> </dl>

 

