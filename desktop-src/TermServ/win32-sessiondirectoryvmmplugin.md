---
title: Win32_SessionDirectoryVMMPlugin-Klasse
description: Stellt ein VMM-Plug-In (Virtual Machine Manager) dar, das bei einem Sitzungsbroker registriert ist.
ms.assetid: b5c5deb1-6c1b-4547-a24a-db3ce6654144
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryVMMPlugin-Klassen-Remotedesktopdienste
- Win32_SessionDirectoryVMMPlugin-Klasse Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin.sName
- Win32_SessionDirectoryVMMPlugin.sProvider
- Win32_SessionDirectoryVMMPlugin.sClassID
- Win32_SessionDirectoryVMMPlugin.sServiceLocation
- Win32_SessionDirectoryVMMPlugin.Priority
- Win32_SessionDirectoryVMMPlugin.Enabled
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7481022951664b49b912b854e96e2d30895b0716ee67b6eb01ce1a9f1b1561ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422360"
---
# <a name="win32_sessiondirectoryvmmplugin-class"></a>Win32 \_ SessionDirectoryVMMPlugin-Klasse

Stellt ein VMM-Plug-In (Virtual Machine Manager) dar, das bei einem Sitzungsbroker registriert ist.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYVMMPLUGIN_Prov"), AMENDMENT]
class Win32_SessionDirectoryVMMPlugin
{
  string  sName;
  string  sProvider;
  string  sClassID;
  string  sServiceLocation;
  sint32  Priority = 0;
  boolean Enabled = FALSE;
};
```

## <a name="members"></a>Member

Die **Win32 \_ SessionDirectoryVMMPlugin-Klasse** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ SessionDirectoryVMMPlugin-Klasse** verfügt über diese Methoden.



| Methode                                                                             | Beschreibung                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------|
| [**GetCurrentVMMPlugin**](getcurrentvmmplugin-win32-sessiondirectoryvmmplugin.md) | Ruft das Plug-In mit der höchsten Priorität ab, das aktiviert ist.<br/> |
| [**RegisterVMMPlugin**](registervmmplugin-win32-sessiondirectoryvmmplugin.md)     | Registriert ein neues VMM-Plug-In.<br/>                       |
| [**SetEnabled**](setenabled-win32-sessiondirectoryvmmplugin.md)                   | Aktiviert oder deaktiviert das Plug-In.<br/>                   |
| [**SetName**](setname-win32-sessiondirectoryvmmplugin.md)                         | Legt den Namen des Plug-Ins fest.<br/>                      |
| [**SetPriority**](setpriority-win32-sessiondirectoryvmmplugin.md)                 | Legt die Priorität des Plug-Ins fest.<br/>                  |
| [**SetProvider**](setprovider-win32-sessiondirectoryvmmplugin.md)                 | Legt den Anbieternamen des Plug-Ins fest.<br/>             |
| [**SetServiceLocation**](setservicelocation-win32-sessiondirectoryvmmplugin.md)   | Legt den Dienstspeicherort des Plug-Ins fest.<br/>          |
| [**UnregisterVMMPlugin**](unregistervmmplugin-win32-sessiondirectoryvmmplugin.md) | Aufheben der Registrierung des Plug-Ins.<br/>                           |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ SessionDirectoryVMMPlugin-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das Plug-In aktiviert oder deaktiviert ist. **True,** wenn das Plug-In aktiviert ist, **andernfalls FALSE.** Das Plug-In ist standardmäßig deaktiviert.

</dd> <dt>

**Priority**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Die Priorität des Plug-Ins. Je höher der Wert, desto höher ist die Priorität des Plug-Ins. Die Priorität ist standardmäßig 0 (null).

</dd> <dt>

**sClassID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Klassenbezeichner des Plug-Ins.

</dd> <dt>

**sName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Plug-Ins.

</dd> <dt>

**sProvider**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Plug-In-Anbieters.

</dd> <dt>

**sServiceLocation**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Dienststandort, an den das Plug-In sich wenden soll.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                      |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

