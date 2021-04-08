---
title: Win32_SessionDirectoryVMMPlugin-Klasse
description: Stellt ein VMM-Plug-in (Virtual Machine Manager) dar, das bei einem Sitzungs Broker registriert ist.
ms.assetid: b5c5deb1-6c1b-4547-a24a-db3ce6654144
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryVMMPlugin-Klasse Remotedesktopdienste
- Win32_SessionDirectoryVMMPlugin Klasse Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: 6c5fc6b899eaa264357527eb107e11ad5a40ad67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949559"
---
# <a name="win32_sessiondirectoryvmmplugin-class"></a>Win32- \_ Klasse "sessiondirectoryvmmplugin"

Stellt ein VMM-Plug-in (Virtual Machine Manager) dar, das bei einem Sitzungs Broker registriert ist.

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

Die Win32-Klasse " **\_ sessiondirectoryvmmplugin** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die Win32-Klasse " **\_ sessiondirectoryvmmplugin** " verfügt über diese Methoden.



| Methode                                                                             | BESCHREIBUNG                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------|
| [**Getcurrentvmmplugin**](getcurrentvmmplugin-win32-sessiondirectoryvmmplugin.md) | Ruft das Plug-in mit der höchsten Priorität ab, das aktiviert ist.<br/> |
| [**Registervmmplugin**](registervmmplugin-win32-sessiondirectoryvmmplugin.md)     | Registriert ein neues VMM-Plug-in.<br/>                       |
| [**Abgeleitete**](setenabled-win32-sessiondirectoryvmmplugin.md)                   | Aktiviert oder deaktiviert das Plug-in.<br/>                   |
| [**SetName**](setname-win32-sessiondirectoryvmmplugin.md)                         | Legt den Namen des Plug-ins fest.<br/>                      |
| [**SetPriority**](setpriority-win32-sessiondirectoryvmmplugin.md)                 | Legt die Priorität des Plug-ins fest.<br/>                  |
| [**Setprovider**](setprovider-win32-sessiondirectoryvmmplugin.md)                 | Legt den Anbieter Namen des Plug-ins fest.<br/>             |
| [**Setservicelokation**](setservicelocation-win32-sessiondirectoryvmmplugin.md)   | Legt den Speicherort des Plug-Ins für den Dienst fest.<br/>          |
| [**Unregistervmmplugin**](unregistervmmplugin-win32-sessiondirectoryvmmplugin.md) | Hebt die Registrierung des Plug-Ins auf.<br/>                           |



 

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse " **\_ sessiondirectoryvmmplugin** " verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das Plug-in aktiviert oder deaktiviert ist. **True** , wenn das Plug-in aktiviert ist, andernfalls **false** . Das Plug-in ist standardmäßig deaktiviert.

</dd> <dt>

**Priority**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Die Priorität des Plug-ins. Je höher der Wert ist, desto höher ist die Priorität des Plug-ins. Der Standardwert ist 0 (null).

</dd> <dt>

**sclassid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Klassen Bezeichner des Plug-ins.

</dd> <dt>

**sName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Plug-ins.

</dd> <dt>

**sprovider**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Plug-in-Anbieters.

</dd> <dt>

**sservicelokation**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Dienst Speicherort, den das Plug-in kontaktieren soll.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                      |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>"Tssdwmi. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

