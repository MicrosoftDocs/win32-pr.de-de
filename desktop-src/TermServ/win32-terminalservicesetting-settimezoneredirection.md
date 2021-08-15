---
title: SetTimeZoneRedirection-Methode der Win32_TerminalServiceSetting-Klasse
description: Die SetTimeZoneRedirection-Methode legt die TimeZoneRedirection-Eigenschaft fest, mit der der Clientcomputer seine Zeitzoneneinstellungen an die Remotedesktopdienste Sitzung umleiten kann.
ms.assetid: 4ae149b7-b7de-4530-a142-7253dd1e0d07
ms.tgt_platform: multiple
keywords:
- SetTimeZoneRedirection-Methode Remotedesktopdienste
- SetTimeZoneRedirection-Methode Remotedesktopdienste , Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste , SetTimeZoneRedirection-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetTimeZoneRedirection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 802cd4741f4ea30f378492075f69dfa21dfce54688fbc7ff9e72b957689d7c7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755641"
---
# <a name="settimezoneredirection-method-of-the-win32_terminalservicesetting-class"></a>SetTimeZoneRedirection-Methode der Win32 \_ TerminalServiceSetting-Klasse

Die **SetTimeZoneRedirection-Methode** legt die **TimeZoneRedirection-Eigenschaft** fest, mit der der Clientcomputer seine Zeitzoneneinstellungen an die Remotedesktopdienste Sitzung umleiten kann.

## <a name="syntax"></a>Syntax


```mof
uint32 SetTimeZoneRedirection(
  [in] uint32 TimeZoneRedirection
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TimeZoneRedirection* \[ In\]
</dt> <dd>

Der neue Wert für die **TimeZoneRedirection-Eigenschaft.**

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Deaktiviert die **TimeZoneRedirection-Eigenschaft.** Es erfolgt keine Zeitzonenumleitung.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Aktiviert die **TimeZoneRedirection-Eigenschaft.** Die Zeitzone des Clients wird an die Zeitzone der Sitzung umgeleitet.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück. andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Standardmäßig entspricht die Zeitzone für die Remotedesktopdienste Sitzung der Zeitzone für den Remotedesktop-Sitzungshost -Server (RD-Sitzungshost). Clientcomputer können Zeitzoneninformationen nicht umleiten.

Wenn die Zeitzonenumleitung deaktiviert ist, erben neue Sitzungen die Serverzeitzone. Wenn eine Sitzung erneut verbunden wird, behält die Sitzung die Zeitzone bei, die sie vor dem Trennen der Verbindung hatte.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe des Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

