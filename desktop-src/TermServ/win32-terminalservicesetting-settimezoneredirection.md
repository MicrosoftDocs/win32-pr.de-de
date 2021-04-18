---
title: Settimezoneredirection-Methode der Win32_TerminalServiceSetting-Klasse
description: Mit der settimezoneredirection-Methode wird die timezoneredirection-Eigenschaft festgelegt, die es dem Client Computer ermöglicht, seine Zeitzoneneinstellungen an die Remotedesktopdienste Sitzung umzuleiten.
ms.assetid: 4ae149b7-b7de-4530-a142-7253dd1e0d07
ms.tgt_platform: multiple
keywords:
- Settimezoneredirection-Methode Remotedesktopdienste
- Settimezoneredirection-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, settimezoneredirection-Methode
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
ms.openlocfilehash: 2761567c724abf129ac881188bc468b228d7fd11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340999"
---
# <a name="settimezoneredirection-method-of-the-win32_terminalservicesetting-class"></a>Settimezoneredirection-Methode der Win32 \_ terminalservicesetts-Klasse

Mit der **settimezoneredirection** -Methode wird die **timezoneredirection** -Eigenschaft festgelegt, die es dem Client Computer ermöglicht, seine Zeitzoneneinstellungen an die Remotedesktopdienste Sitzung umzuleiten.

## <a name="syntax"></a>Syntax


```mof
uint32 SetTimeZoneRedirection(
  [in] uint32 TimeZoneRedirection
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Timezoneredirection* \[ in\]
</dt> <dd>

Der neue Wert für die **timezoneredirection** -Eigenschaft.

<dt>

<span id="0"></span>

<span id="0"></span>**1,0**


</dt> <dd>

Deaktiviert die **timezoneredirection** -Eigenschaft. Es findet keine Zeit Zonen Umleitung statt.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Aktiviert die **timezoneredirection** -Eigenschaft. Die Zeitzone des Clients wird an die Zeitzone der Sitzung umgeleitet.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück. Andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Bemerkungen

Standardmäßig ist die Zeitzone für die Remotedesktopdienste Sitzung identisch mit der Zeitzone für den Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server. -Client Computer können keine Zeitzoneninformationen umleiten.

Wenn die Zeit Zonen Umleitung deaktiviert ist, erben neue Sitzungen die Zeitzone des Servers. Wenn eine Sitzung erneut eine Verbindung herstellt, behält die Sitzung die Zeitzone bei, die vor dem Trennen der Verbindung aufgetreten ist.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ terminalservicesetts**](win32-terminalservicesetting.md)
</dt> </dl>

 

