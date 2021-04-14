---
title: Enable-Methode der Win32_Terminal-Klasse
description: Mit der enable-Methode wird das Terminal deaktiviert oder aktiviert.
ms.assetid: f249563b-6fa0-413c-9fc7-01dd16d5c561
ms.tgt_platform: multiple
keywords:
- Methoden Remotedesktopdienste aktivieren
- Methoden Remotedesktopdienste aktivieren, Win32_Terminal Klasse
- Win32_Terminal Klasse Remotedesktopdienste, Methode aktivieren
topic_type:
- apiref
api_name:
- Win32_Terminal.Enable
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afedef572c65f249c48da850172bb9fc4d222c19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391656"
---
# <a name="enable-method-of-the-win32_terminal-class"></a>Enable-Methode der Win32- \_ Terminal Klasse

Mit der **enable** -Methode wird das Terminal deaktiviert oder aktiviert.

## <a name="syntax"></a>Syntax


```mof
uint32 Enable(
  [in] uint32 fEnableTerminal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fenableterminal* \[ in\]
</dt> <dd>

Flag, das das Terminal deaktiviert oder aktiviert.

<dt>

<span id="0"></span>

<span id="0"></span>**1,0**


</dt> <dd>

Das Terminal ist deaktiviert.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Das Terminal ist aktiviert.

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

[**Win32- \_ Terminal**](win32-terminal.md)
</dt> </dl>

 

