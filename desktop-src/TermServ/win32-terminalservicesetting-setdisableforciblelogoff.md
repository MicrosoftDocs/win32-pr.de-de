---
title: SetDisableForcibleLogoff-Methode der Win32_TerminalServiceSetting-Klasse
description: 'SetDisableForcibleLogoff-Methode der Win32_TerminalServiceSetting-Klasse: Diese Methode wird nicht unterstützt.'
ms.assetid: 1b7ac0f2-c242-4ca8-bc4d-8111e63851eb
ms.tgt_platform: multiple
keywords:
- SetDisableForcibleLogoff-Methode Remotedesktopdienste
- SetDisableForcibleLogoff-Methode Remotedesktopdienste , Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste , SetDisableForcibleLogoff-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetDisableForcibleLogoff
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4be6ace10853ec282f5ab17b1f5f5921ef2c0d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103708"
---
# <a name="setdisableforciblelogoff-method-of-the-win32_terminalservicesetting-class"></a>SetDisableForcibleLogoff-Methode der Win32 \_ TerminalServiceSetting-Klasse

Diese Methode wird nicht unterstützt.

**Windows Vista und Windows Server 2008:** Aktiviert oder deaktiviert, ob ein bei der Konsole angemeldeter Administrator abgemeldet werden kann.

## <a name="syntax"></a>Syntax


```mof
uint32 SetDisableForcibleLogoff(
  [in] uint32 DisableForcibleLogoff
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DisableForcibleLogoff* \[ In\]
</dt> <dd>

Flag zum Deaktivieren oder Aktivieren der **DisableForcibleLogoff-Eigenschaft,** die bestimmt, ob ein Administrator, der bei der Konsole angemeldet ist, abgemeldet werden kann.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Deaktivieren Sie die -Eigenschaft. Der verbundene Administrator kann abgemeldet werden.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Aktivieren Sie die -Eigenschaft. Der verbundene Administrator kann nicht abgemeldet werden.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt Erfolg bei Erfolg zurück. andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie [unter Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Ende des Supports (Client)<br/>    | Windows Vista<br/>                                                                |
| Ende des Supports (Server)<br/>    | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

 





