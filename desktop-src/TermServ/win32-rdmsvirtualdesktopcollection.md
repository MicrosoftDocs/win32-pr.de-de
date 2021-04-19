---
title: Win32_RDMSVirtualDesktopCollection-Klasse
description: Erstellt und verwaltet eine Sammlung virtueller Desktops.
ms.assetid: fe0a484e-f9e3-4b99-8e69-da8f337ae957
ms.tgt_platform: multiple
keywords:
- Win32_RDMSVirtualDesktopCollection-Klasse Remotedesktopdienste
- Win32_RDMSVirtualDesktopCollection Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection.Alias
- Win32_RDMSVirtualDesktopCollection.Type
- Win32_RDMSVirtualDesktopCollection.IsManaged
- Win32_RDMSVirtualDesktopCollection.Name
- Win32_RDMSVirtualDesktopCollection.CollectionDescription
- Win32_RDMSVirtualDesktopCollection.SecurityDescriptor
- Win32_RDMSVirtualDesktopCollection.VmFarmSettings
- Win32_RDMSVirtualDesktopCollection.UserVHDSetting
- Win32_RDMSVirtualDesktopCollection.IconContents
- Win32_RDMSVirtualDesktopCollection.ShowInPortal
- Win32_RDMSVirtualDesktopCollection.IsHA
- Win32_RDMSVirtualDesktopCollection.IsUserAdmin
- Win32_RDMSVirtualDesktopCollection.RollbackEnabled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a6da0c13b6ab223afc7afe6e92039a5388c6204
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341600"
---
# <a name="win32_rdmsvirtualdesktopcollection-class"></a>Win32 \_ rdmsvirtualdesktopcollection-Klasse

Erstellt und verwaltet eine Sammlung virtueller Desktops.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktopCollection
{
  string  Alias;
  uint32  Type;
  boolean IsManaged;
  string  Name;
  string  CollectionDescription;
  string  SecurityDescriptor;
  string  VmFarmSettings;
  string  UserVHDSetting;
  uint8   IconContents[];
  boolean ShowInPortal;
  boolean IsHA;
  boolean IsUserAdmin;
  boolean RollbackEnabled;
};
```

## <a name="members"></a>Member

Die **Win32 \_ rdmsvirtualdesktopcollection** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ rdmsvirtualdesktopcollection** -Klasse verfügt über diese Methoden.



| Methode                                                                                            | BESCHREIBUNG                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Addvirtualdesktop**](addvirtualdesktop-win32-rdmsvirtualdesktopcollection.md)                 | Fügt einer Sammlung virtueller Desktops einen virtuellen Desktop hinzu.<br/>                                                                              |
| [**Cancelpatch**](cancelpatch-win32-rdmsvirtualdesktopcollection.md)                             | Bricht einen Bereitstellungs Auftrag für Software Updates für die virtuellen Computer in einer Sammlung virtueller Desktops ab.<br/>                                 |
| [**GetInt32Property**](getint32property-win32-rdmsvirtualdesktopcollection.md)                   | Ruft einen ganzzahligen Eigenschafts Wert aus einer Sammlung virtueller Desktops ab.<br/>                                                               |
| [**Getpatchproperties**](getpatchproperties-win32-rdmsvirtualdesktopcollection.md)               | Ruft die Eigenschaften eines Bereitstellungs Auftrags für Software Updates für die virtuellen Computer in einer Sammlung virtueller Desktops ab.<br/>             |
| [**GetStringProperty**](getstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | Ruft einen Zeichen folgen Eigenschafts Wert aus einer Sammlung virtueller Desktops ab.<br/>                                                                 |
| [**Provisioningenvereratejobs**](provisioningenumeratejobs-win32-rdmsvirtualdesktopcollection.md) | Listet die Bereitstellungs Aufträge virtueller Desktops für diesen Dienst auf.<br/>                                                                       |
| [**Provisioningjobcancel**](provisioningjobcancel-win32-rdmsvirtualdesktopcollection.md)         | Bricht einen Bereitstellungs Auftrag für virtuelle Desktops ab.<br/>                                                                                          |
| [**Provisioningjobexecute**](provisioningjobexecute-win32-rdmsvirtualdesktopcollection.md)       | Führt einen Bereitstellungs Auftrag für virtuelle Desktops aus.<br/>                                                                                             |
| [**Provisioningjobgetreport**](provisioningjobgetreport-win32-rdmsvirtualdesktopcollection.md)   | Ruft einen Bericht zum Status eines virtuellen Desktop Bereitstellungs Auftrags ab.<br/>                                                                |
| [**Provisioningprepjob**](win32-rdmsvirtualdesktopcollection-provisioningprepjob.md)             | Erstellt einen Bereitstellungs Auftrag für virtuelle Desktops.<br/>                                                                                          |
| [**Removevirtualdesktop**](removevirtualdesktop-win32-rdmsvirtualdesktopcollection.md)           | Entfernt einen virtuellen Desktop aus einer Sammlung virtueller Desktops.<br/>                                                                         |
| [**Schedulepatch**](schedulepatch-win32-rdmsvirtualdesktopcollection.md)                         | Plant einen Bereitstellungs Auftrag für Software Updates, mit dem Software Updates auf den virtuellen Computern in einer Sammlung virtueller Desktops installiert werden.<br/> |
| [**SetInt32Property**](setint32property-win32-rdmsvirtualdesktopcollection.md)                   | Aktualisiert einen ganzzahligen Eigenschafts Wert einer Sammlung virtueller Desktops.<br/>                                                                   |
| [**SetStringProperty**](setstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | Aktualisiert den Wert einer Zeichen folgen Eigenschaft einer Sammlung virtueller Desktops.<br/>                                                                     |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ rdmsvirtualdesktopcollection** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Alias**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ruft den Alias der Auflistung ab oder legt ihn fest.

</dd> <dt>

**Collectiondescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ruft die Beschreibung der Auflistung ab oder legt Sie fest.

</dd> <dt>

**Iconcontent**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ruft ein Array von-Werten ab, die Symbole für die Auflistung angeben, oder legt dieses fest.

</dd> <dt>

**Isha**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft einen Wert ab, der angibt, ob die Auflistung hoch verfügbare VMS enthält, oder legt ihn fest. **True** , wenn die Sammlung hoch verfügbare VMS enthält. andernfalls **false**.

</dd> <dt>

**IsManaged**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft einen Wert ab, der angibt, ob die Auflistung verwaltet wird, oder legt ihn fest. **True** , wenn die Auflistung verwaltet wird. andernfalls **false**.

</dd> <dt>

**Isuseradmin**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft einen Wert ab, der angibt, ob ein Benutzer ein Administrator auf einem virtuellen Computer ist, oder legt ihn fest. **True** , wenn der Benutzer ein Administrator auf einem virtuellen Computer ist. andernfalls **false**.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft den Namen der Auflistung ab oder legt ihn fest.

</dd> <dt>

**Rollback aktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft einen Wert ab, der angibt, ob ein virtueller Computer mit einer VM-Momentaufnahme erstellt wurde. **True** , wenn die VM mit einer VM-Momentaufnahme erstellt wurde. andernfalls **false**.

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Dient zum Abrufen oder Festlegen einer Sicherheits Beschreibung, die die SSDL-Sicherheit steuert, die den Zugriff auf die Auflistung steuert.

</dd> <dt>

**Showinportal**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft einen Wert ab, der angibt, ob die Auflistung in terminaldiensteWebzugriff (TS Webzugriff) angezeigt wird, oder legt ihn fest. **True** zum Anzeigen der Auflistung in TS Webzugriff; andernfalls **false**.

</dd> <dt>

**Type**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft einen Wert ab, der den Typ der von der Auflistung gehosteten Sitzungen von virtuellen Maschinen angibt, oder legt diesen fest.

Diese Eigenschaft enthält einen der folgenden Werte:

<dt>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>**Tempvm** (1)


</dt> <dd>

Temporäre virtuelle Computer.

</dd> <dt>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>**Manualpersonalvm** (2)


</dt> <dd>

Manuell erstellte virtuelle Computer.

</dd> <dt>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>**Autopersonalvm** (3)


</dt> <dd>

Automatisch generierte virtuelle Computer.

</dd> </dl>

</dd> <dt>

**Uservhdsetting**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ruft die Einstellung für die Benutzerdaten-VHD für die Auflistung ab oder legt Sie fest.

</dd> <dt>

**Vmfarmsettings**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ruft die Desktop Einstellungen für die virtuellen Maschinen in der Auflistung ab oder legt Sie fest.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | Root \\ CIMV2 \\ RDMs<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Rdmanagement. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remotedesktop Management Services-Anbieter](rdms-api-reference.md)
</dt> </dl>

 

