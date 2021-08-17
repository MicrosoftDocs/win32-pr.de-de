---
title: Win32_TSVirtualDesktopServerSettings-Klasse
description: Enthält Konfigurationsinformationen für einen Remotedesktop Virtualization Host(RD Virtualization Host)-Server.
ms.assetid: 749018aa-a8aa-433e-985b-40b44ef8aa7f
ms.tgt_platform: multiple
keywords:
- Win32_TSVirtualDesktopServerSettings-Remotedesktopdienste
- Win32_TSVirtualDesktopServerSettings klasse Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- Win32_TSVirtualDesktopServerSettings
- Win32_TSVirtualDesktopServerSettings.SessionBrokerName
- Win32_TSVirtualDesktopServerSettings.PolicySourceSessionBrokerName
- Win32_TSVirtualDesktopServerSettings.Concurrency
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f40e7d51ee0c92e50afca023629bb92de9f506b3e47ee9e520aa16c09640375b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137463"
---
# <a name="win32_tsvirtualdesktopserversettings-class"></a>Win32 \_ TSVirtualDesktopServerSettings-Klasse

Enthält Konfigurationsinformationen für einen Remotedesktop Virtualization Host(RD Virtualization Host)-Server.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[singleton, dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVirtualDesktopServerSettings
{
  string SessionBrokerName;
  sint32 PolicySourceSessionBrokerName;
  uint32 Concurrency;
};
```

## <a name="members"></a>Member

Die **Win32 \_ TSVirtualDesktopServerSettings-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TSVirtualDesktopServerSettings-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Concurrency**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die maximal zulässige Anzahl gleichzeitiger Bereitstellungsanforderungen für diesen Virtual Desktop-Server.

</dd> <dt>

**PolicySourceSessionBrokerName**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wenn diese Einstellung auf 0 festgelegt ist, gibt an, dass die **SessionBrokerName-Eigenschaft** vom Server konfiguriert wird. Wenn auf 1 festgelegt, gibt an, dass die **SessionBrokerName-Eigenschaft** durch eine Gruppenrichtlinie konfiguriert wird.

</dd> <dt>

**SessionBrokerName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der vollqualifizierte Distinguished Name des Sitzungsbrokers für den RD-Virtualisierungshostserver.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                             |
| Namespace<br/>                | Root \\ CIMV2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost.mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

 





