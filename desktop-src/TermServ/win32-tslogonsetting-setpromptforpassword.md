---
title: Setpromptforpassword-Methode der Win32_TSLogonSetting-Klasse
description: Die setpromptforpassword-Methode legt die PromptForPassword-Eigenschaft fest.
ms.assetid: eeeed374-4a8a-4014-833c-d931be3ef455
ms.tgt_platform: multiple
keywords:
- Setpromptforpassword-Methode Remotedesktopdienste
- Setpromptforpassword-Methode Remotedesktopdienste, Win32_TSLogonSetting-Klasse
- Win32_TSLogonSetting-Klasse Remotedesktopdienste, setpromptforpassword-Methode
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.SetPromptForPassword
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f86dc065a143505ea81bce78d9bf787fae6b0a33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337528"
---
# <a name="setpromptforpassword-method-of-the-win32_tslogonsetting-class"></a>Setpromptforpassword-Methode der Win32- \_ Klasse "tlogonsetting"

Die **setpromptforpassword** -Methode legt die **PromptForPassword** -Eigenschaft fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetPromptForPassword(
  [in] uint32 PromptForPassword
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PromptForPassword* \[ in\]
</dt> <dd>

Flag zum Deaktivieren oder Aktivieren der **PromptForPassword** -Eigenschaft.

<dt>

0
</dt> <dd>

Deaktiviert die Kenn Wort Eingabeaufforderung.

</dd> <dt>

1
</dt> <dd>

Aktiviert die Kenn Wort Eingabeaufforderung.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg Erfolg zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) . Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.

<dl> <dt>

**False** (0)
</dt> <dt>

**True** (1)
</dt> </dl>

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

[**Win32-Anmelde \_ Einstellung**](win32-tslogonsetting.md)
</dt> </dl>

 

