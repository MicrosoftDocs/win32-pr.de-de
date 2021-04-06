---
title: Win32_TSVirtualDesktopServerSettings-Klasse
description: Enthält Konfigurationsinformationen für einen Remotedesktop-Virtualisierungshost Server (RD-Virtualisierungshost).
ms.assetid: 749018aa-a8aa-433e-985b-40b44ef8aa7f
ms.tgt_platform: multiple
keywords:
- Win32_TSVirtualDesktopServerSettings-Klasse Remotedesktopdienste
- Win32_TSVirtualDesktopServerSettings Klasse Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: c39635aee7b32430ace0ead0e3b007051a3c049d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743265"
---
# <a name="win32_tsvirtualdesktopserversettings-class"></a>Win32- \_ Klasse "tvirtualdesktopserversettings"

Enthält Konfigurationsinformationen für einen Remotedesktop-Virtualisierungshost Server (RD-Virtualisierungshost).

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

Die Win32-Klasse " **\_ tvirtualdesktopserversettings** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse " **\_ tvirtualdesktopserversettings** " verfügt über diese Eigenschaften.

<dl> <dt>

**Parallelität**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die maximal zulässigen gleichzeitigen Bereitstellungs Anforderungen für diesen virtuellen Desktop Server.

</dd> <dt>

**Policysourcesessionbrokername**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wenn der Wert auf 0 festgelegt ist, wird angegeben, dass die **sessionbrokername** -Eigenschaft vom Server konfiguriert wird. Wenn der Wert auf 1 festgelegt ist, wird die Eigenschaft **sessionbrokername** von einer Gruppenrichtlinie konfiguriert.

</dd> <dt>

**Sessionbrokername**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der voll qualifizierte Distinguished Name des Sitzungs Brokers für den RD-Virtualisierungshostserver.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                             |
| Namespace<br/>                | Root \\ CIMV2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>"Zvmhost. mof"</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

 





