---
description: Stellt die Einstellungen einer Component Object Model-Komponente (com) dar.
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
ms.openlocfilehash: 5f263a888ce9dea80444023faff57998bc3f2c1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344969"
---
# <a name="win32_classiccomclasssetting-class"></a>Win32 \_ classiccomclasssetting-Klasse

Die **Win32 \_ classiccomclasssetting** - [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) stellt die Einstellungen einer Component Object Model (com)-Komponente dar.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die **Win32 \_ classiccomclasssetting** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ classiccomclasssetting** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**AppID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \[ AppID \] ")
</dt> </dl>

GUID (Global Unique Identifier) für die COM-Anwendung, die diese COM-Komponente verwendet.

</dd> <dt>

**Autoconvertumclsid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ autoconvertto \[ Default \] ")
</dt> </dl>

GUID der com-Klasse, in die diese COM-Komponente automatisch konvertiert wird.

</dd> <dt>

**AutoTreatAsClsid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ AutoTreatAs \[ Default \] ")
</dt> </dl>

GUID für die COM-Komponente, die Instanzen dieser Klasse automatisch emuliert.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Kurze Textbeschreibung des aktuellen-Objekts.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**ComponentId**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes Software Classes \\ \\ CLSID \\ \\ {GUID} \[ Default \] ")
</dt> </dl>

GUID dieser COM-Komponente.

</dd> <dt>

**Steuerung**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID}- \\ \\ Steuerelement")
</dt> </dl>

COM-Komponente ist ein OLE-Steuerelement.

</dd> <dt>

**DefaultIcon**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ DefaultIcon \[ Default \] ")
</dt> </dl>

Pfad zur ausführbaren Datei und zum Ressourcen Bezeichner des Standard Symbols, das von der-Klasse verwendet wird.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des aktuellen-Objekts.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**InprocHandler**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler \[ Default \] ")
</dt> </dl>

Vollständiger Pfad, einschließlich Dateiname oder nur Dateiname zu einem benutzerdefinierten 16-Bit-Handler für die COM-Komponente Der Anbieter gibt nicht immer den vollständigen Pfad zurück.

</dd> <dt>

**InprocHandler32**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler32 \[ Default \] ")
</dt> </dl>

Vollständiger Pfad, einschließlich Dateiname oder nur Dateiname zu einem benutzerdefinierten 32-Bit-Handler für die COM-Komponente Der Anbieter gibt nicht immer den vollständigen Pfad zurück.

</dd> <dt>

**InprocServer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer \[ Default \] ")
</dt> </dl>

Vollständiger Pfad, einschließlich Dateiname oder nur Dateiname zu einer 16-Bit-Prozess internen Server-DLL für diese COM-Komponente. Der Anbieter gibt nicht immer den vollständigen Pfad zurück.

</dd> <dt>

**InprocServer32**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InProcServer32 \[ Default \] ")
</dt> </dl>

Vollständiger Pfad, einschließlich Dateiname oder nur Dateiname zu einer 32-Bit-Prozess internen Server-DLL für diese COM-Komponente. Der Anbieter gibt nicht immer den vollständigen Pfad zurück.

</dd> <dt>

**Einfügbar**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ Insertable")
</dt> </dl>

COM-Komponente kann in OLE-Container Anwendungen eingefügt werden.

</dd> <dt>

**JAVACLASS**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InProcServer32 \[ JAVACLASS \] ")
</dt> </dl>

Die COM-Komponente ist eine Java-Komponente.

</dd> <dt>

**LocalServer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer \[ Default \] ")
</dt> </dl>

Vollständiger Pfad, einschließlich Dateiname oder nur Dateiname für eine 16-Bit-Anwendung für einen lokalen Der Anbieter gibt nicht immer den vollständigen Pfad zurück.

</dd> <dt>

**LocalServer32**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer32 \[ Default \] ")
</dt> </dl>

Vollständiger Pfad, einschließlich Dateiname oder nur Dateiname für eine lokale 32-Bit-Serveranwendung. Der Anbieter gibt nicht immer den vollständigen Pfad zurück.

</dd> <dt>

**LongDisplayName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ auxusertype \\ \\ 3 \[ Default \] ")
</dt> </dl>

Der vollständige Name der com-Anwendung. Sie wird in Bereichen wie dem **Ergebnis** Feld des OLE-Dialog Felds " **speziell einfügen** " verwendet.

</dd> <dt>

**ProgID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ ProgID \[ Default \] ")
</dt> </dl>

Programm Bezeichner, der der COM-Komponente zugeordnet ist. Das Format einer ProgID ist <Vendor. <Component. <Version. Es ist nicht garantiert, dass dieser Bezeichner eindeutig ist.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**ShortDisplayName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ auxusertype \\ \\ 2 \[ Default \] ")
</dt> </dl>

Kurzname der com-Anwendung (wird in Menüs und Popups verwendet).

</dd> <dt>

**ThreadingModel**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InProcServer32 \[ ThreadingModel \] ")
</dt> </dl>

Threading Modell, das von in-Process-COM-Klassen verwendet wird. Wenn diese Eigenschaft **null** ist, wird kein Threading Modell verwendet. Die Komponente wird im Haupt Thread des Clients erstellt, und Aufrufe von anderen Threads werden an diesen Thread gemarshallt.

Das Apartment Modell gibt an, dass Komponenten nur von einem einzigen Thread eingegeben werden dürfen. Allgemeine Daten, die von diesen Objekt Server Typen gespeichert werden, müssen vor Thread Kollisionen geschützt werden, da der Objekt Server mehrere Komponenten unterstützt. Jede Komponente kann gleichzeitig von verschiedenen Threads eingegeben werden.

Das kostenlose Modell gibt an, dass die Komponenten keine Einschränkungen für die Threads oder die Anzahl der Threads haben, die das Objekt eingeben können. Das Objekt kann keine Thread spezifischen Daten enthalten und muss seine Daten vor gleichzeitigem Zugriff durch mehrere Threads schützen. Auf frei Thread Komponenten kann jedoch nicht direkt von Apartment Threads zugegriffen werden, und Aufrufe an diese Komponenten werden über das Client Apartment gemarshallt.

Wenn beides angegeben ist, können Komponenten entweder im Apartment Thread-oder im Free Thread-Modus verwendet werden. Diese Komponenten können von mehreren Threads eingegeben werden, Ihre Daten vor Thread Kollisionen schützen und keine Thread spezifischen Daten enthalten.

Die Werte sind:

<dl> <dd>Apartment</dd> <dd>Kosten</dd> <dd>Zwar</dd> </dl>

<dt>

<span id="Apartment"></span><span id="apartment"></span><span id="APARTMENT"></span>

**Apartment** ("Apartment")


</dt> <dd></dd> <dt>

<span id="Free"></span><span id="free"></span><span id="FREE"></span>

**Kostenlos** ("kostenlos")


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

**Beides** ("beides")


</dt> <dd></dd> </dl>

</dd> <dt>

**ToolBoxBitmap32**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ ToolBoxBitmap32 \[ Default \] ")
</dt> </dl>

Modulname und Ressourcen Bezeichner für eine kleine (16x16) Bitmap, die für das Gesicht einer Symbolleiste oder Toolbox Schaltfläche verwendet wird. Wird verwendet, wenn die COM-Komponente ein OLE-oder ActiveX-Steuerelement ist.

</dd> <dt>

**TreatAsClsid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ TreatAs \[ Default \] ")
</dt> </dl>

GUID einer COM-Komponente, die Instanzen dieser Komponente emulieren kann.

</dd> <dt>

**TypeLibraryId**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ typelib \[ Default \] ")
</dt> </dl>

GUID für die Typbibliothek für diese COM-Komponente.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ Version \[ Default \] ")
</dt> </dl>

Versionsnummer dieser com-Klasse.

</dd> <dt>

**VersionIndependentProgId**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ VersionIndependentProgId \[ Default \] ")
</dt> </dl>

Programm Bezeichner, der für alle Versionen desselben Programms konsistent ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32 \_ classiccomclasssetting** -Klasse wird von [**Win32 \_ comsetting**](win32-comsetting.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ comsetting**](win32-comsetting.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

