---
description: Stellt die Low-Level-Software dar, die in einen nicht flüchtigen Speicher geladen und zum Starten und Konfigurieren eines Computersystems (CIM \_ ComputerSystem) verwendet wird.
ms.assetid: e34c9b00-2723-4858-805e-5e3e51a5dfd2
title: CIM_BIOSElement -Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSElement
- CIM_BIOSElement.Version
- CIM_BIOSElement.Manufacturer
- CIM_BIOSElement.PrimaryBIOS
- CIM_BIOSElement.ListOfLanguages
- CIM_BIOSElement.CurrentLanguage
- CIM_BIOSElement.LoadedStartingAddress
- CIM_BIOSElement.LoadedEndingAddress
- CIM_BIOSElement.LoadUtilityInformation
- CIM_BIOSElement.ReleaseDate
- CIM_BIOSElement.RegistryURIs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 78f2433d2b75e2c348fdf6e7a8ff35db56c9a0c8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879879"
---
# <a name="cim_bioselement-class-hyper-v-management"></a>CIM_BIOSElement -Klasse (Hyper-V-Verwaltung)

Stellt die Low-Level-Software dar, die in einen nicht flüchtigen Speicher geladen und zum Starten und Konfigurieren eines Computersystems [**\_ (CIM-ComputerSystem) verwendet wird.**](cim-computersystem.md)

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.17.0"), UMLPackagePath("CIM::Application::BIOS"), AMENDMENT]
class CIM_BIOSElement : CIM_SoftwareElement
{
  string   Version;
  string   Manufacturer;
  boolean  PrimaryBIOS;
  string   ListOfLanguages[];
  string   CurrentLanguage;
  uint64   LoadedStartingAddress;
  uint64   LoadedEndingAddress;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
};
```

## <a name="members"></a>Member

Die **CIM \_ BIOSElement-Klasse** verfügt über diese Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ BIOSElement-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BIOSElement**.**ListOfLanguages**")
</dt> </dl>

Die derzeit ausgewählte Sprache für das BIOS. Diese Informationen können aus dem System Management BIOS (SMBIOS) mithilfe des Current Language-Attributs der Type 13-Struktur für die Indizierung in die Zeichenfolgenliste nach der -Struktur ermittelt werden. Diese Eigenschaft wird mithilfe des ISO 639-Sprachnamens formatiert und kann vom ISO 3166-Gebietsnamen und der Codierungsmethode gefolgt werden.

</dd> <dt>

**ListOfLanguages**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Liste der installierbaren Sprachen für das BIOS. Diese Informationen können aus SMBIOS aus der Zeichenfolgenliste ermittelt werden, die der Type 13-Struktur folgt. Ein ISO 639-Sprachname sollte verwendet werden, um die installierbaren Sprachen des BIOS anzugeben. Der ISO 3166-Gebietsname und die Codierungsmethode können auch nach dem Sprachnamen angegeben werden.

</dd> <dt>

**LoadedEndingAddress**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System BIOS \| 001.6")
</dt> </dl>

Die Endadresse des Arbeitsspeichers, der vom BIOS belegt wird.

</dd> <dt>

**LoadedStartingAddress**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System BIOS \| 001.5")
</dt> </dl>

Die Startadresse des Arbeitsspeichers, der vom BIOS belegt wird.

</dd> <dt>

**LoadUtilityInformation**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System BIOS \| 001.7")
</dt> </dl>

Eine freie Formularzeichenfolge, die das BIOS-Hilfsprogramm für Flash/Load beschreibt, das zum Aktualisieren des **CIM \_ BIOSElement-Objekts erforderlich** ist. Version und andere Informationen können in dieser Eigenschaft angegeben werden.

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System BIOS \| 001.2")
</dt> </dl>

Der Hersteller des Softwareelements.

</dd> <dt>

**PrimaryBIOS**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System BIOS \| 001.9")
</dt> </dl>

True, wenn dies das primäre BIOS des Computersystems ist; andernfalls FALSE.

</dd> <dt>

**RegistryURIs**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Veröffentlichungsspeicherort der BIOS-Attributregister, denen die BIOS-Implementierung entspricht.

</dd> <dt>

**Released**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System BIOS \| 001.8")
</dt> </dl>

Das Datum, an dem dieses BIOS veröffentlicht wurde.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System BIOS \| 001.3")
</dt> </dl>

Die Version des Vorgangs. Die Version des Vorgangs sollte in einer der folgenden Formen sein:

-   *&lt; Haupt- &gt;*.*&lt; neben &gt; .* *&lt; Revision &gt;*
-   *&lt; Haupt- &gt;*.*&lt; &gt; &lt; &gt; &lt; Nebenbuchstabenrevision &gt;*

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ SoftwareElement**](cim-softwareelement.md)
</dt> </dl>

 

