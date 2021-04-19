---
title: Win32_RdvhManagement-Klasse
description: Beschreibt einen Remotedesktop den Verwaltungsdienst für virtuelle Hosts (RDVH).
ms.assetid: 2a81786c-e772-4596-9846-a46828f9b48b
ms.tgt_platform: multiple
keywords:
- Win32_RdvhManagement-Klasse Remotedesktopdienste
- Win32_RdvhManagement Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RdvhManagement
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01e2cde81173035d00587782dc45d9ddeb66fcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345900"
---
# <a name="win32_rdvhmanagement-class"></a>Win32 \_ rdvhmanagement-Klasse

Beschreibt einen Remotedesktop den Verwaltungsdienst für virtuelle Hosts (RDVH).

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_RdvhManagement
{
};
```

## <a name="members"></a>Member

Die **Win32- \_ rdvhmanagement** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **Win32- \_ rdvhmanagement** -Klasse verfügt über diese Methoden.



| Methode                                                                                  | BESCHREIBUNG                                                                                                                                                             |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Rdvkreateuserdisktemplate**](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | Erstellt die Vorlage für Benutzer Datenträger mit der angegebenen maximalen Größe und am angegebenen Speicherort. Alle erstellten Benutzer Datenträger verfügen über maximale Größe, die der maximalen Größe der Vorlage entspricht.<br/> |
| [**RdvMigrateVmToDifferentHost**](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | Initiiert eine Live Migration virtueller Computer in VDI-Szenarios.<br/>                                                                                               |
| [**Rdvcopybasevmlokal**](rdvcopybasevmlocally-win32-rdvhmanagement.md)               | Kopiert den Basis-VM-Speicherort lokal auf RDV-Host Server<br/>                                                                                                           |
| [**Rdvkreateuserdisktemplate**](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | Erstellt die Vorlage für Benutzer Datenträger mit der angegebenen maximalen Größe und am angegebenen Speicherort. Alle erstellten Benutzer Datenträger verfügen über maximale Größe, die der maximalen Größe der Vorlage entspricht.<br/> |
| [**RdvMigrateVmToDifferentHost**](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | Initiiert eine Live Migration virtueller Computer in VDI-Szenarien.<br/>                                                                                              |
| [**Rdvsetupvm-Berechtigungen**](rdvsetupvmpermissions-win32-rdvhmanagement.md)             | Legt Berechtigungen für die VM für den Aufrufer fest.<br/>                                                                                                                        |
| [**Rdvundovm-Berechtigungen**](rdvundovmpermissions-win32-rdvhmanagement.md)               | Kehrt die Berechtigungen in der von rdvsetupvmberechtigungs Gruppe festgelegten VM zurück.<br/>                                                                                                       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                             |
| Namespace<br/>                | Root \\ CIMV2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>"Zvmhost. mof"</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

 





