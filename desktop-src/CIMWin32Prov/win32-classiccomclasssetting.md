---
description: Stellt die Einstellungen einer Component Object Model (COM) dar.
ms.assetid: 18d9ddf2-184d-4680-8d56-f012c608ff7d
ms.tgt_platform: multiple
title: Win32_ClassicCOMClassSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClassSetting
- Win32_ClassicCOMClassSetting.Caption
- Win32_ClassicCOMClassSetting.Description
- Win32_ClassicCOMClassSetting.SettingID
- Win32_ClassicCOMClassSetting.AppID
- Win32_ClassicCOMClassSetting.AutoConvertToClsid
- Win32_ClassicCOMClassSetting.AutoTreatAsClsid
- Win32_ClassicCOMClassSetting.ComponentId
- Win32_ClassicCOMClassSetting.Control
- Win32_ClassicCOMClassSetting.DefaultIcon
- Win32_ClassicCOMClassSetting.InprocHandler
- Win32_ClassicCOMClassSetting.InprocHandler32
- Win32_ClassicCOMClassSetting.InprocServer
- Win32_ClassicCOMClassSetting.InprocServer32
- Win32_ClassicCOMClassSetting.Insertable
- Win32_ClassicCOMClassSetting.JavaClass
- Win32_ClassicCOMClassSetting.LocalServer
- Win32_ClassicCOMClassSetting.LocalServer32
- Win32_ClassicCOMClassSetting.LongDisplayName
- Win32_ClassicCOMClassSetting.ProgId
- Win32_ClassicCOMClassSetting.ShortDisplayName
- Win32_ClassicCOMClassSetting.ThreadingModel
- Win32_ClassicCOMClassSetting.ToolBoxBitmap32
- Win32_ClassicCOMClassSetting.TreatAsClsid
- Win32_ClassicCOMClassSetting.TypeLibraryId
- Win32_ClassicCOMClassSetting.Version
- Win32_ClassicCOMClassSetting.VersionIndependentProgId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4aa3a60b68902bbcf7728866d24e5cedd831eac35ba629a3e2516a885a28efaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118418241"
---
# <a name="win32_classiccomclasssetting-class"></a>Win32 \_ ClassicCOMClassSetting-Klasse

Die **WMI-Klasse Win32 \_ ClassicCOMClassSetting** stellt die Einstellungen einer Component Object Model (COM)-Komponente dar. [](/windows/desktop/WmiSdk/retrieving-a-class)

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A562-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClassSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  string  AutoConvertToClsid;
  string  AutoTreatAsClsid;
  string  ComponentId;
  boolean Control;
  string  DefaultIcon;
  string  InprocHandler;
  string  InprocHandler32;
  string  InprocServer;
  string  InprocServer32;
  boolean Insertable;
  boolean JavaClass;
  string  LocalServer;
  string  LocalServer32;
  string  LongDisplayName;
  string  ProgId;
  string  ShortDisplayName;
  string  ThreadingModel;
  string  ToolBoxBitmap32;
  string  TreatAsClsid;
  string  TypeLibraryId;
  string  Version;
  string  VersionIndependentProgId;
};
```

## <a name="members"></a>Member

Die **Win32 \_ ClassicCOMClassSetting-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ ClassicCOMClassSetting-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AppID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ AppID \] ")
</dt> </dl>

GuiD (Globally Unique Identifier) für die COM-Anwendung, die diese COM-Komponente verwendet.

</dd> <dt>

**AutoConvertToClsid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ AutoConvertTo Default \[ \] ")
</dt> </dl>

GUID der COM-Klasse, in die diese COM-Komponente automatisch konvertiert wird.

</dd> <dt>

**AutoTreatAsClsid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ AutoTreatAs Default \[ \] ")
</dt> </dl>

GUID für die COM-Komponente, die automatisch Instanzen dieser Klasse emuliert.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Kurze Textbeschreibung des aktuellen Objekts.

Diese Eigenschaft wird von der [**CIM-Einstellung \_ geerbt.**](cim-setting.md)

</dd> <dt>

**ComponentId**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} Default \[ \] ")
</dt> </dl>

GUID dieser COM-Komponente.

</dd> <dt>

**Steuerung**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ Control")
</dt> </dl>

Die COM-Komponente ist ein OLE-Steuerelement.

</dd> <dt>

**DefaultIcon**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ DefaultIcon Default \[ \] ")
</dt> </dl>

Pfad zur ausführbaren Datei und ressourcenbezeichner des Standardsymbols, das von der -Klasse verwendet wird.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des aktuellen -Objekts.

Diese Eigenschaft wird von der [**CIM-Einstellung \_ geerbt.**](cim-setting.md)

</dd> <dt>

**InprocHandler**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler Default \[ \] ")
</dt> </dl>

Vollständiger Pfad einschließlich Dateiname oder nur Dateiname zu einem benutzerdefinierten 16-Bit-Handler für die COM-Komponente. Der Anbieter gibt nicht immer den vollständigen Pfad zurück.

</dd> <dt>

**InprocHandler32**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler32 Default \[ \] ")
</dt> </dl>

Vollständiger Pfad einschließlich Dateiname oder nur Dateiname zu einem benutzerdefinierten 32-Bit-Handler für die COM-Komponente. Der Anbieter gibt nicht immer den vollständigen Pfad zurück.

</dd> <dt>

**InprocServer**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer Default \[ \] ")
</dt> </dl>

Vollständiger Pfad einschließlich Dateiname oder nur Dateiname zu einer 16-Bit-Prozessserver-DLL für diese COM-Komponente. Der Anbieter gibt nicht immer den vollständigen Pfad zurück.

</dd> <dt>

**Inprocserver32**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 Default \[ \] ")
</dt> </dl>

Vollständiger Pfad einschließlich Dateiname oder nur Dateiname zu einer 32-Bit-Prozessserver-DLL für diese COM-Komponente. Der Anbieter gibt nicht immer den vollständigen Pfad zurück.

</dd> <dt>

**Insertierbaren**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ Insertable")
</dt> </dl>

Die COM-Komponente kann in OLE-Containeranwendungen eingefügt werden.

</dd> <dt>

**JavaClass**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ JavaClass \] ")
</dt> </dl>

Die COM-Komponente ist eine Java-Komponente.

</dd> <dt>

**LocalServer**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer Default \[ \] ")
</dt> </dl>

Vollständiger Pfad einschließlich Dateiname oder nur Dateiname zu einer lokalen 16-Bit-Serveranwendung. Der Anbieter gibt nicht immer den vollständigen Pfad zurück.

</dd> <dt>

**LocalServer32**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer32 Default \[ \] ")
</dt> </dl>

Vollständiger Pfad einschließlich Dateiname oder nur Dateiname zu einer lokalen 32-Bit-Serveranwendung. Der Anbieter gibt nicht immer den vollständigen Pfad zurück.

</dd> <dt>

**LongDisplayName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ AuxUserType \\ \\ 3 Default \[ \] ")
</dt> </dl>

Vollständiger Name der COM-Anwendung. Sie wird in Bereichen wie dem Feld **Ergebnisse** des Dialogfelds **OLE Paste Special** verwendet.

</dd> <dt>

**Progid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ ProgID Default \[ \] ")
</dt> </dl>

Programmgesteuerter Bezeichner, der der COM-Komponente zugeordnet ist. Das Format einer ProgID lautet <Vendor.<Component.<Version. Dieser Bezeichner ist nicht garantiert eindeutig.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Bezeichner, durch den das aktuelle Objekt bekannt ist.

Diese Eigenschaft wird von [**cim \_ setting**](cim-setting.md)geerbt.

</dd> <dt>

**ShortDisplayName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ AuxUserType \\ \\ 2 Default \[ \] ")
</dt> </dl>

Kurzname der COM-Anwendung (wird in Menüs und Popups verwendet).

</dd> <dt>

**ThreadingModel**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ ThreadingModel \] ")
</dt> </dl>

Threadingmodell, das von prozessübergreifenden COM-Klassen verwendet wird. Wenn diese Eigenschaft **NULL** ist, wird kein Threadingmodell verwendet. Die Komponente wird im Hauptthread des Clients erstellt, und Aufrufe von anderen Threads werden an diesen Thread gemarshallt.

Das Apartment-Modell gibt an, dass Komponenten von nur einem Thread eingegeben werden können. Allgemeine Daten, die von diesen Objektservertypen gespeichert werden, müssen vor Threadkonflikten geschützt werden, da der Objektserver mehrere Komponenten unterstützt. Jede Komponente kann gleichzeitig von verschiedenen Threads eingegeben werden.

Das Free-Modell gibt an, dass Komponenten keine Einschränkungen hinsichtlich der Threads und der Anzahl von Threads, die in das Objekt gelangen können, unterliegen. Das -Objekt darf keine threadspezifischen Daten enthalten und muss seine Daten vor dem gleichzeitigen Zugriff durch mehrere Threads schützen. Auf Freethreadkomponenten kann jedoch nicht direkt von Apartmentthreads zugegriffen werden, und Aufrufe an sie werden über das Clientapartment gemarshallt.

Wenn Beide angegeben ist, können Komponenten entweder im Apartmentthreadmodus oder im Freethreadmodus verwendet werden. Diese Komponenten können von mehreren Threads eingegeben werden, schützen ihre Daten vor Threadkonflikten und enthalten keine threadspezifischen Daten.

Die Werte sind:

<dl> <dd>"Apartment"</dd> <dd>"Free"</dd> <dd>"Beide"</dd> </dl>

<dt>

<span id="Apartment"></span><span id="apartment"></span><span id="APARTMENT"></span>

**Apartment** ("Apartment")


</dt> <dd></dd> <dt>

<span id="Free"></span><span id="free"></span><span id="FREE"></span>

**Free** ("Free")


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

**Beide** ("beide")


</dt> <dd></dd> </dl>

</dd> <dt>

**ToolBoxBitmap32**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ ToolBoxBitmap32 Default \[ \] ")
</dt> </dl>

Modulname und Ressourcenbezeichner für eine kleine Bitmap (16 x 16), die für das Gesicht einer Symbolleisten- oder Toolboxschaltfläche verwendet wird. Wird verwendet, wenn die COM-Komponente ein OLE- oder ActiveX-Steuerelement ist.

</dd> <dt>

**TreatAsClsid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ TreatAs Default \[ \] ")
</dt> </dl>

GUID einer COM-Komponente, die Instanzen dieser Komponente emulieren kann.

</dd> <dt>

**TypeLibraryId**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ TypeLib Default \[ \] ")
</dt> </dl>

GUID für die Typbibliothek für diese COM-Komponente.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} Version Default \\ \\ \[ \] ")
</dt> </dl>

Versionsnummer dieser COM-Klasse.

</dd> <dt>

**VersionIndependentProgId**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \\ \\ VersionIndependentProgId Default \[ \] ")
</dt> </dl>

Programmbezeichner, der für alle Versionen desselben Programms konsistent ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ ClassicCOMClassSetting-Klasse** wird von [**Win32 \_ COMSetting**](win32-comsetting.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ COMSetting**](win32-comsetting.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

