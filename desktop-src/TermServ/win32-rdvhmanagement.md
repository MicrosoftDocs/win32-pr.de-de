---
title: Win32_RdvhManagement-Klasse
description: Beschreibt einen Remotedesktop virtuellen Host (RDVH).
ms.assetid: 2a81786c-e772-4596-9846-a46828f9b48b
ms.tgt_platform: multiple
keywords:
- Win32_RdvhManagement-Remotedesktopdienste
- Win32_RdvhManagement klasse Remotedesktopdienste , beschrieben
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
ms.openlocfilehash: 4ea403621aa23cb999bdf2fe692e2d4e053866492608e71346d978cb764ab005
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422580"
---
# <a name="win32_rdvhmanagement-class"></a>Win32 \_ RdvhManagement-Klasse

Beschreibt einen Remotedesktop virtuellen Host (RDVH).

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_RdvhManagement
{
};
```

## <a name="members"></a>Member

Die **Win32 \_ RdvhManagement-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **Win32 \_ RdvhManagement-Klasse** verfügt über diese Methoden.



| Methode                                                                                  | Beschreibung                                                                                                                                                             |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RdvCreateUserDiskTemplate**](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | Erstellt eine Benutzerdatenträgervorlage mit der angegebenen maximalen Größe und am angegebenen Speicherort. Alle erstellten Benutzerdatenträger verfügen über maximale Größen, die mit der maximalen Größe der Vorlage übereinstimmen.<br/> |
| [**RdvMigrateVmToDifferentHost**](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | Initiiert eine Livemigration des virtuellen Computers in VDI-Szenarien<br/>                                                                                               |
| [**RdvCopyBaseVmLocally**](rdvcopybasevmlocally-win32-rdvhmanagement.md)               | Kopiert den Standort des virtuellen Basiscomputers lokal auf RDV-Host Server.<br/>                                                                                                           |
| [**RdvCreateUserDiskTemplate**](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | Erstellt eine Benutzerdatenträgervorlage mit der angegebenen maximalen Größe und am angegebenen Speicherort. Alle erstellten Benutzerdatenträger verfügen über maximale Größen, die mit der maximalen Größe der Vorlage übereinstimmen.<br/> |
| [**RdvMigrateVmToDifferentHost**](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | Initiiert eine Livemigration des virtuellen Computers in VDI-Szenarien.<br/>                                                                                              |
| [**RdvSetupVMPermissions**](rdvsetupvmpermissions-win32-rdvhmanagement.md)             | Legt Berechtigungen auf dem virtuellen Computer für den Aufrufer fest.<br/>                                                                                                                        |
| [**RdvUndoVMPermissions**](rdvundovmpermissions-win32-rdvhmanagement.md)               | Bricht Berechtigungen auf virtuellen Computer zurück, die von RdvSetupVMPermissions festgelegt wurden<br/>                                                                                                       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                             |
| Namespace<br/>                | Root \\ cimv2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost.mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

 





