---
title: Win32_SessionDirectoryVirtualDesktopServer-Klasse
description: Stellt einen Remotedesktop-Virtualisierungshost Server (RD-Virtualisierungshost) dar, der einem Sitzungs Broker hinzugefügt wurde.
ms.assetid: a09221bd-d1b1-465b-91bb-9ca400a796b1
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryVirtualDesktopServer-Klasse Remotedesktopdienste
- Win32_SessionDirectoryVirtualDesktopServer Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVirtualDesktopServer
- Win32_SessionDirectoryVirtualDesktopServer.Name
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2940679c13c5bd86f7d6b02340698f529e8149e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040326"
---
# <a name="win32_sessiondirectoryvirtualdesktopserver-class"></a>Win32 \_ sessiondirectoryvirtualdesktopserver-Klasse

Stellt einen Remotedesktop-Virtualisierungshost Server (RD-Virtualisierungshost) dar, der einem Sitzungs Broker hinzugefügt wurde.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_SDVirtualDesktopServer_Prov"), AMENDMENT]
class Win32_SessionDirectoryVirtualDesktopServer
{
  string Name;
};
```

## <a name="members"></a>Member

Die Win32-Klasse " **\_ sessiondirectoryvirtualdesktopserver** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse " **\_ sessiondirectoryvirtualdesktopserver** " verfügt über diese Eigenschaften.

<dl> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der DNS-Name des Remote Desktop-Virtualisierungshostservers. Dieser Name hat das Format "*MachineName*. *Domain*. com ".

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                      |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>"Tssdwmi. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

