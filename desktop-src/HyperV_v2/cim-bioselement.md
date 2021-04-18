---
description: Stellt die Software auf niedriger Ebene dar, die in einen nicht flüchtigen Speicher geladen und zum Starten und Konfigurieren eines Computer Systems (CIM \_ Computersystem) verwendet wird.
ms.assetid: e34c9b00-2723-4858-805e-5e3e51a5dfd2
title: CIM_BIOSElement-Klasse (Hyper-V-Verwaltung)
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
ms.openlocfilehash: f97cbb495fb8105be012c44942aeedb39377e3d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366244"
---
# <a name="cim_bioselement-class-hyper-v-management"></a>CIM_BIOSElement-Klasse (Hyper-V-Verwaltung)

Stellt die Software auf niedriger Ebene dar, die in einen nicht flüchtigen Speicher geladen und zum Starten und Konfigurieren eines Computer Systems ([**CIM \_ Computersystem**](cim-computersystem.md)) verwendet wird.

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

Die CIM-Klasse " **\_ bioselements** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die CIM-Klasse " **\_ bioselements** " verfügt über diese Eigenschaften.

<dl> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ bioseless**".**ListOf-Sprachen**")
</dt> </dl>

Die aktuell für das BIOS ausgewählte Sprache. Diese Informationen können aus dem Systemverwaltungs-BIOS (Systemverwaltungs-BIOS) abgerufen werden, wobei das aktuelle sprach Attribut der Type 13-Struktur verwendet wird, um in die Zeichen folgen Liste zu indizieren, die der Struktur folgt. Diese Eigenschaft wird mit dem Namen der ISO 639-Sprache formatiert, gefolgt vom ISO 3166 Territory-Namen und der Codierungsmethode.

</dd> <dt>

**ListOf-Sprachen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Liste installier barer Sprachen für das BIOS. Diese Informationen können aus der Zeichen folgen Liste abgerufen werden, die der Struktur des Typs 13 folgt. Der Name der ISO 639-Sprache sollte zum Angeben der installierbaren BIOS-Sprachen verwendet werden. Der Name des Gebiets namens ISO 3166 und die Codierungsmethode können auch nach dem Namen der Sprache angegeben werden.

</dd> <dt>

**Loadedendingaddress**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System-BIOS \| 001,6 ")
</dt> </dl>

Die Endadresse des vom BIOS belegten Speichers.

</dd> <dt>

**Loadedstartingaddress**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System-BIOS \| 001,5 ")
</dt> </dl>

Die Startadresse des vom BIOS belegten Speichers.

</dd> <dt>

**Loadutilityinformation**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System-BIOS \| 001,7 ")
</dt> </dl>

Eine frei Form Zeichenfolge, die das BIOS-Hilfsprogramm für Flash/Ladevorgang beschreibt, das zum Aktualisieren des **CIM \_** -Objekts für die Objekt Verwaltung erforderlich ist Die Version und andere Informationen können in dieser Eigenschaft angegeben werden.

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hersteller"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System-BIOS \| 001,2 ")
</dt> </dl>

Der Hersteller des Software Elements.

</dd> <dt>

**Primarybios**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System-BIOS \| 001,9 ")
</dt> </dl>

True, wenn dies das primäre BIOS des Computer Systems ist. andernfalls false.

</dd> <dt>

**Registryuris**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Veröffentlichungs Speicherort der BIOS-Attribut Registrierungen, denen die BIOS-Implementierung entspricht.

</dd> <dt>

**ReleaseDate**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System-BIOS \| 001,8 ")
</dt> </dl>

Das Datum, an dem dieses BIOS freigegeben wurde.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System-BIOS \| 001,3 ")
</dt> </dl>

Die Version des Vorgangs. Die Version des Vorgangs sollte eine der folgenden Formen aufweisen:

-   *<major>*.*<minor>*.*<revision>*
-   *<major>*.*<minor><letter><revision>*

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

[**CIM- \_ Softwareelement**](cim-softwareelement.md)
</dt> </dl>

 

