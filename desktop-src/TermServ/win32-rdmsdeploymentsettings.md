---
title: Win32_RDMSDeploymentSettings-Klasse
description: Verwaltet die Bereitstellungs Einstellungen für eine Sammlung virtueller Desktops.
ms.assetid: c33563d5-a388-46d3-b23a-797aab9d472a
ms.tgt_platform: multiple
keywords:
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste
- Win32_RDMSDeploymentSettings Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6be75f74a71a82800bc6fdd7ba0c4bae5a85021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517624"
---
# <a name="win32_rdmsdeploymentsettings-class"></a>Win32 \_ rdmsdeploymentsettings-Klasse

Verwaltet die Bereitstellungs Einstellungen für eine Sammlung virtueller Desktops.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDeploymentSettings
{
};
```

## <a name="members"></a>Member

Die **Win32 \_ rdmsdeploymentsettings** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **Win32 \_ rdmsdeploymentsettings** -Klasse verfügt über diese Methoden.



| Methode                                                                                                  | BESCHREIBUNG                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**Getbasevhdpath**](getbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | Ruft den Basispfad zu dem Verzeichnis ab, in dem die VHDs der virtuellen Desktop Sammlung bereitgestellt werden.<br/>                 |
| [**GetConnectionString**](win32-rdmsdeploymentsettings-getconnectionstring.md)                         | Ruft die Datenbank-Verbindungs Zeichenfolge auf Bereitstellungs Ebene ab.<br/>                                                             |
| [**Getdiffvhdpath**](getdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | Ruft den Verzeichnispfad ab, in dem die differenzierenden Datenträger für eine Sammlung virtueller Desktops bereitgestellt werden.<br/>            |
| [**Getexportpath**](getexportpath-win32-rdmsdeploymentsettings.md)                                     | Ruft den Verzeichnispfad ab, in dem virtuelle Maschinen für eine Sammlung virtueller Desktops bereitgestellt werden.<br/>                  |
| [**GetInt32Property**](getint32property-win32-rdmsdeploymentsettings.md)                               | Ruft eine ganzzahlige Eigenschaft für die Bereitstellungs Einstellungen einer Sammlung virtueller Desktops ab.<br/>                             |
| [**Getsecondaryconnectionstring**](win32-rdmsdeploymentsettings-getsecondaryconnectionstring.md)       | Ruft die sekundäre Daten bankverbindungs Zeichenfolge auf Bereitstellungs Ebene ab, die zur Unterstützung des Kenn Wort Ablaufs verwendet werden kann.<br/> |
| [**Getsmbpath**](getsmbpath-win32-rdmsdeploymentsettings.md)                                           | Ruft den UNC-Pfad zur SMB-Freigabe ab, auf der virtuelle Maschinen der virtuellen Desktop Sammlung bereitgestellt werden.<br/>      |
| [**Getstringarraydeploymentsetting**](getstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | Ruft die Bereitstellungs Einstellungen für eine Sammlung virtueller Desktops ab.<br/>                                                    |
| [**GetStringProperty**](getstringproperty-win32-rdmsdeploymentsettings.md)                             | Ruft eine Zeichen folgen Eigenschaft für die Bereitstellungs Einstellungen einer Sammlung virtueller Desktops ab.<br/>                               |
| [**Removedeploymentsetting**](removedeploymentsetting-win32-rdmsdeploymentsettings.md)                 | Löscht die Bereitstellungs Einstellungen für eine Sammlung virtueller Desktops.<br/>                                                      |
| [**Setbasevhdpath**](setbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | Ruft den Basispfad zu dem Verzeichnis ab, in dem die VHDs der virtuellen Desktop Sammlung bereitgestellt werden.<br/>                 |
| [**SetConnectionString**](win32-rdmsdeploymentsettings-setconnectionstring.md)                         | Legt die Daten bankverbindungs Zeichenfolge auf Bereitstellungs Ebene fest.<br/>                                                                  |
| [**Setdiffvhdpath**](setdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | Aktualisiert den Verzeichnispfad, in dem die differenzierenden Datenträger für eine Sammlung virtueller Desktops bereitgestellt werden.<br/>              |
| [**"Stexportpath"**](setexportpath-win32-rdmsdeploymentsettings.md)                                     | Aktualisiert den Verzeichnispfad, in dem virtuelle Maschinen für eine Sammlung virtueller Desktops bereitgestellt werden.<br/>                    |
| [**SetInt32Property**](setint32property-win32-rdmsdeploymentsettings.md)                               | Aktualisiert eine ganzzahlige Eigenschaft für die Bereitstellungs Einstellungen einer Sammlung virtueller Desktops.<br/>                               |
| [**Setsecondaryconnectionstring**](win32-rdmsdeploymentsettings-setsecondaryconnectionstring.md)       | Legt die sekundäre Daten bankverbindungs Zeichenfolge auf Bereitstellungs Ebene fest.<br/>                                                        |
| [**Setsmbpath**](setsmbpath-win32-rdmsdeploymentsettings.md)                                           | Aktualisiert den UNC-Pfad zur SMB-Freigabe, auf der virtuelle Maschinen der virtuellen Desktop Sammlung bereitgestellt werden.<br/>        |
| [**Setstringarraydeploymentsetting**](setstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | Aktualisiert die Bereitstellungs Einstellungen für eine Sammlung virtueller Desktops.<br/>                                                      |
| [**SetStringProperty**](setstringproperty-win32-rdmsdeploymentsettings.md)                             | Aktualisiert eine Zeichen folgen Eigenschaft für die Bereitstellungs Einstellungen einer Sammlung virtueller Desktops.<br/>                                 |



 

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

 

 





