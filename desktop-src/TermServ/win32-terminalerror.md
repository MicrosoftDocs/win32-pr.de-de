---
title: Win32_TerminalError-Klasse
description: Stellt einen Terminal Fehler dar.
ms.assetid: d3f622cd-e4ce-4c7e-999e-940b67fd116c
ms.tgt_platform: multiple
keywords:
- Win32_TerminalError-Klasse Remotedesktopdienste
- Win32_TerminalError Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TerminalError
- Win32_TerminalError.Description
- Win32_TerminalError.Operation
- Win32_TerminalError.ParameterInfo
- Win32_TerminalError.ProviderName
- Win32_TerminalError.StatusCode
- Win32_TerminalError.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99724badc6c1ca7a2e4168e5c062b4dd1495ea6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103146"
---
# <a name="win32_terminalerror-class"></a>Win32 \_ terminalerror-Klasse

Stellt einen Terminal Fehler dar.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
class Win32_TerminalError : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string TerminalName;
};
```

## <a name="members"></a>Member

Die **Win32 \_ terminalerror** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ terminalerror** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine beliebige benutzerdefinierte Zeichenfolge, die einen Fehler-oder Betriebsstatus beschreibt.

Diese Eigenschaft wird von " [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus)" geerbt.

</dd> <dt>

**Vorgang**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Vorgang, der zum Zeitpunkt eines Fehlers oder einer Anomalieerkennung stattfindet. In der Regel wird diese Eigenschaft von WMI auf den Namen der com-API für die WMI-Methode festgelegt, wie z. b. die folgende: [**IWbemServices:: kreateinstanceenum**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).

Diese Eigenschaft wird von " [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus)" geerbt.

</dd> <dt>

**Parameter Info**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Parameter, die an einem Fehler oder einer Statusänderung beteiligt sind. Wenn eine Anwendung z. b. versucht, eine Klasse abzurufen, die nicht vorhanden ist, wird diese Eigenschaft auf den Namen der angreifenden Klasse festgelegt.

Diese Eigenschaft wird von " [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus)" geerbt.

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifiziert den Anbieter, der einen Fehler oder eine Statusänderung auslöst oder meldet. Wenn ein Anbieter nicht beteiligt ist, wird diese Zeichenfolge auf "Windows-Verwaltung" festgelegt.

Diese Eigenschaft wird von " [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus)" geerbt.

</dd> <dt>

**Statuscode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Enthält einen Fehler-oder Informations Code für einen Vorgang. Dies kann ein beliebiger Wert sein, der vom Anbieter definiert wird. der Wert 0 (null) ist jedoch normalerweise reserviert, um den Erfolg anzugeben. Diese Eigenschaft wird von [**\_ \_ notifystatus**](/windows/desktop/WmiSdk/--notifystatus)geerbt.

</dd> <dt>

**Terminal Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des endfehlers, bei dem der Fehler aufgetreten ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Erweiterdedstatus**](/windows/desktop/WmiSdk/--extendedstatus)
</dt> </dl>

 

