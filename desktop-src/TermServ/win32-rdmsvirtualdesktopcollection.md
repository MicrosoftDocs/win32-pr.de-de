---
title: Win32_RDMSVirtualDesktopCollection-Klasse
description: Erstellt und verwaltet eine Sammlung virtueller Desktops.
ms.assetid: fe0a484e-f9e3-4b99-8e69-da8f337ae957
ms.tgt_platform: multiple
keywords:
- Win32_RDMSVirtualDesktopCollection-Klassen-Remotedesktopdienste
- Win32_RDMSVirtualDesktopCollection-Klasse Remotedesktopdienste beschrieben
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
ms.openlocfilehash: 580b5ae194a28726a06143dce0007eeedfbb8564b49a4cbc2e7c2d0d8507dfe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868070"
---
# <a name="win32_rdmsvirtualdesktopcollection-class"></a>Win32 \_ RDMSVirtualDesktopCollection-Klasse

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

Die **Win32 \_ RDMSVirtualDesktopCollection-Klasse** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ RDMSVirtualDesktopCollection-Klasse** verfügt über diese Methoden.



| Methode                                                                                            | BESCHREIBUNG                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddVirtualDesktop**](addvirtualdesktop-win32-rdmsvirtualdesktopcollection.md)                 | Fügt einer Sammlung virtueller Desktops einen virtuellen Desktop hinzu.<br/>                                                                              |
| [**CancelPatch**](cancelpatch-win32-rdmsvirtualdesktopcollection.md)                             | Bricht einen Auftrag zur Bereitstellung von Softwareupdates für die virtuellen Computer in einer Sammlung virtueller Desktops ab.<br/>                                 |
| [**GetInt32Property**](getint32property-win32-rdmsvirtualdesktopcollection.md)                   | Ruft einen ganzzahligen Eigenschaftswert aus einer Sammlung virtueller Desktops ab.<br/>                                                               |
| [**GetPatchProperties**](getpatchproperties-win32-rdmsvirtualdesktopcollection.md)               | Ruft die Eigenschaften eines Softwareupdatebereitstellungsauftrags für die virtuellen Computer in einer Sammlung virtueller Desktops ab.<br/>             |
| [**GetStringProperty**](getstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | Ruft einen Zeichenfolgeneigenschaftswert aus einer Sammlung virtueller Desktops ab.<br/>                                                                 |
| [**ProvisioningEnumerateJobs**](provisioningenumeratejobs-win32-rdmsvirtualdesktopcollection.md) | Listet Aufträge für die Bereitstellung virtueller Desktops für diesen Dienst auf.<br/>                                                                       |
| [**ProvisioningJobCancel**](provisioningjobcancel-win32-rdmsvirtualdesktopcollection.md)         | Bricht einen Bereitstellungsauftrag für virtuelle Desktops ab.<br/>                                                                                          |
| [**ProvisioningJobExecute**](provisioningjobexecute-win32-rdmsvirtualdesktopcollection.md)       | Führt einen Bereitstellungsauftrag für virtuelle Desktops aus.<br/>                                                                                             |
| [**ProvisioningJobGetReport**](provisioningjobgetreport-win32-rdmsvirtualdesktopcollection.md)   | Ruft einen Bericht über den Status eines Bereitstellungsauftrags für virtuelle Desktops ab.<br/>                                                                |
| [**ProvisioningPrepJob**](win32-rdmsvirtualdesktopcollection-provisioningprepjob.md)             | Erstellt einen Bereitstellungsauftrag für virtuelle Desktops.<br/>                                                                                          |
| [**RemoveVirtualDesktop**](removevirtualdesktop-win32-rdmsvirtualdesktopcollection.md)           | Entfernt einen virtuellen Desktop aus einer Sammlung virtueller Desktops.<br/>                                                                         |
| [**SchedulePatch**](schedulepatch-win32-rdmsvirtualdesktopcollection.md)                         | Plant einen Auftrag zur Bereitstellung von Softwareupdates, mit dem Softwareupdates auf den virtuellen Computern in einer Sammlung virtueller Desktops installiert werden.<br/> |
| [**SetInt32Property**](setint32property-win32-rdmsvirtualdesktopcollection.md)                   | Aktualisiert einen ganzzahligen Eigenschaftswert einer sammlung virtueller Desktops.<br/>                                                                   |
| [**SetStringProperty**](setstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | Aktualisiert einen Zeichenfolgeneigenschaftswert einer Sammlung virtueller Desktops.<br/>                                                                     |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ RDMSVirtualDesktopCollection-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Alias**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ruft den Alias der Auflistung ab oder legt den Alias fest.

</dd> <dt>

**CollectionDescription**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ruft die Beschreibung der Auflistung ab oder legt sie fest.

</dd> <dt>

**IconContents**
</dt> <dd> <dl> <dt>

Datentyp: **uint8-Array**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ruft ein Array von Werten ab, die Symbole für die Auflistung angeben, oder legt dieses fest.

</dd> <dt>

**Isha**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft einen Wert ab, der angibt, ob die Auflistung hoch verfügbare VMs enthält, oder legt diesen fest. **TRUE,** wenn die Sammlung hoch verfügbare VMs enthält. Andernfalls **FALSE**.

</dd> <dt>

**IsManaged**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft einen Wert ab, der angibt, ob die Auflistung verwaltet wird, oder legt diesen fest. **TRUE,** wenn die Sammlung verwaltet wird; Andernfalls **FALSE**.

</dd> <dt>

**IsUserAdmin**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft einen Wert ab, der angibt, ob ein Benutzer ein Administrator auf einem virtuellen Computer ist, oder legt diesen fest. **TRUE,** wenn der Benutzer ein Administrator auf einem virtuellen Computer ist; Andernfalls **FALSE**.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft den Namen der Auflistung ab oder legt ihn fest.

</dd> <dt>

**RollbackEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft einen Wert ab, der angibt, ob ein virtueller Computer mit einer VM-Momentaufnahme gerollt wurde, oder legt diesen fest. **TRUE,** wenn für den virtuellen Computer ein Rollback mit einer VM-Momentaufnahme ausgeführt wurde. Andernfalls **FALSE**.

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ruft einen SSDL-formatierten Sicherheitsdeskriptor ab, der den Zugriff auf die Auflistung steuert, oder legt diesen fest.

</dd> <dt>

**ShowInPortal**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft einen Wert ab, der angibt, ob die Auflistung in terminal services Webzugriff (TS Webzugriff) angezeigt wird, oder legt diesen fest. **TRUE,** um die Auflistung in TS Webzugriff anzuzeigen; Andernfalls **FALSE**.

</dd> <dt>

**Typ**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft einen Wert ab, der den Typ der von der Auflistung gehosteten VM-Sitzungen angibt, oder legt diesen fest.

Diese Eigenschaft enthält einen der folgenden Werte:

<dt>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>**TempVM** (1)


</dt> <dd>

Temporäre virtuelle Computer.

</dd> <dt>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>**ManualPersonalVM** (2)


</dt> <dd>

Manuell erstellte virtuelle Computer.

</dd> <dt>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>**AutoPersonalVM** (3)


</dt> <dd>

Automatisch generierte virtuelle Computer.

</dd> </dl>

</dd> <dt>

**UserVHDSetting**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ruft die VHD-Einstellung für Benutzerdaten für die Auflistung ab oder legt diese fest.

</dd> <dt>

**VmFarmSettings**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ruft die Desktopeinstellungen für die virtuellen Computer in der Auflistung ab oder legt diese fest.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | Root \\ cimv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remotedesktop Management Services-Anbieter](rdms-api-reference.md)
</dt> </dl>

 

