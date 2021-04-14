---
title: ChangeMode-Methode der Win32_TerminalServiceSetting-Klasse
description: Die ChangeMode-Methode legt den Lizenztyp des aktuellen Remotedesktop-Sitzungshost (RD-Sitzungshost)-Servers fest.
ms.assetid: 293483ee-51ce-4cd4-ba13-6c7c02bbdbbf
ms.tgt_platform: multiple
keywords:
- ChangeMode-Methode Remotedesktopdienste
- ChangeMode-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, ChangeMode-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.ChangeMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880fcab8aa68e49c6b3c00278b90635686de6168
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391856"
---
# <a name="changemode-method-of-the-win32_terminalservicesetting-class"></a>ChangeMode-Methode der Win32 \_ terminalservicesetts-Klasse

Die **ChangeMode** -Methode legt den Lizenztyp des aktuellen Remotedesktop-Sitzungshost (RD-Sitzungshost)-Servers fest.

## <a name="syntax"></a>Syntax


```mof
uint32 ChangeMode(
  [in] uint32 LicensingType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LicensingType* \[ in\]
</dt> <dd>

Der Lizenzierungstyp, der basierend auf dem RD-Sitzungshost Server Modus festgelegt werden soll.

<dt>

<span id="0"></span>

<span id="0"></span>**1,0**


</dt> <dd>

Persönlicher RD-Sitzungshost Server.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Remote Desktop für die Verwaltung.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Pro Gerät/pro Arbeitsplatz. Gültig für Anwendungsserver.

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Pro Benutzer. Gültig für Anwendungsserver.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Bemerkungen

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

 

