---
description: Stellt einen Satz von Komponenten dar, die als einzelne Entität auf hoher Ebene fungieren.
ms.assetid: 784cee32-e0ae-4632-8dac-e5110513f5c9
title: CIM_System-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_System
- CIM_System.CreationClassName
- CIM_System.Name
- CIM_System.NameFormat
- CIM_System.PrimaryOwnerName
- CIM_System.PrimaryOwnerContact
- CIM_System.Roles
- CIM_System.OtherIdentifyingInfo
- CIM_System.IdentifyingDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a51e56ad3e8f91200fbe5bc7e09ac2f14c4ee232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347926"
---
# <a name="cim_system-class-hyper-v-management"></a>CIM_System-Klasse (Hyper-V-Verwaltung)

Stellt einen Satz von Komponenten dar, die als einzelne Entität auf hoher Ebene fungieren.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_System : CIM_EnabledLogicalElement
{
  string CreationClassName;
  string Name;
  string NameFormat;
  string PrimaryOwnerName;
  string PrimaryOwnerContact;
  string Roles[];
  string OtherIdentifyingInfo[];
  string IdentifyingDescriptions[];
};
```

## <a name="members"></a>Member

Die **CIM- \_ System** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ System** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**"Name der Klassenname"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der Klassenname, der verwendet wird, um eine Instanz dieser Klasse zu erstellen. " **Kreationclassname** " wird mit anderen Schlüsseleigenschaften dieser Klasse kombiniert, um Instanzen dieser Klasse und ihrer Unterklassen eindeutig zu identifizieren.

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ System**".**"OtherIdentifyingInfo**")
</dt> </dl>

Ein Array, das Beschreibungen der Werte in der Eigenschaft " **OtherIdentifyingInfo** " enthält. Die Array Elemente in **identifyingbeschreibungen** entsprechen den Elementen in der **identifyingbeschreibungen** -Eigenschaft.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der Schlüssel dieser Instanz in einer Unternehmensumgebung.

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Die Namenskonvention, die von der Name-Eigenschaft verwendet wird, um sicherzustellen, dass die **namens** Werte eindeutig sind

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ System**".**Identifyingbeschreibungen**")
</dt> </dl>

Ein Array, das einen Satz zusätzlicher Daten enthält, die über Systemnamen Informationen hinausgehen und zur Identifizierung eines Computer Systems verwendet werden könnten.

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Allgemeine Informationen zu DMTF \| \| 001,4 ")
</dt> </dl>

Eine Zeichenfolge, die Informationen darüber bereitstellt, wie der primäre Systembesitzer erreicht werden kann (z. b. Telefonnummer, e-Mail-Adresse usw.).

</dd> <dt>

**Primaryownername**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Allgemeine Informationen zu DMTF \| \| 001,3 ")
</dt> </dl>

Der Name des primären Benutzers des Systems.

</dd> <dt>

**Rollen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ein Array, das die Rollen enthält, die vom System in einer Unternehmensumgebung ausgeführt werden.

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

[**CIM \_ enabledlogicalelement**](cim-enabledlogicalelement.md)
</dt> </dl>

 

