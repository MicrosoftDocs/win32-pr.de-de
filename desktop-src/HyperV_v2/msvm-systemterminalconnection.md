---
description: Ordnet eine virtuelle Maschine einer Terminal Verbindung zu.
ms.assetid: 31979FB8-3870-44D9-9720-AD99237C5268
title: Msvm_SystemTerminalConnection-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemTerminalConnection
- Msvm_SystemTerminalConnection.Antecedent
- Msvm_SystemTerminalConnection.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 368c25b8505ec7ddd29da3b95d95fc842602119e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350389"
---
# <a name="msvm_systemterminalconnection-class"></a>MSVM \_ systemterminalconnection-Klasse

Ordnet eine virtuelle Maschine einer Terminal Verbindung zu.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemTerminalConnection : CIM_HostedDependency
{
  Msvm_ComputerSystem     REF Antecedent;
  Msvm_TerminalConnection REF Dependent;
};
```

## <a name="members"></a>Member

Die **MSVM \_ systemterminalconnection** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ systemterminalconnection** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ Computersystem**](msvm-computersystem.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Der virtuelle Computer, an den die Verbindung angefügt wird.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ terminalconnection**](msvm-terminalconnection.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")
</dt> </dl>

Die Verbindung mit dem virtuellen Computer.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM \_ systemterminalconnection** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ hubabhängigkeit**](cim-hosteddependency.md)
</dt> <dt>

[**CIM- \_ hubabhängigkeit**](/previous-versions//cc136861(v=vs.85))
</dt> <dt>

[Video Klassen](video-classes.md)
</dt> </dl>

 

