---
title: Explizilogon-Methode der Win32_TSLogonSetting-Klasse
description: Die explizlogon-Methode legt die Anmelde Informationen fest, die für die Authentifizierung verwendet werden.
ms.assetid: cfd43396-0d66-4d5e-81c8-5c0e66422dc5
ms.tgt_platform: multiple
keywords:
- Explizlogon-Methode Remotedesktopdienste
- Explizitlogon-Methode Remotedesktopdienste, Win32_TSLogonSetting-Klasse
- Win32_TSLogonSetting-Klasse Remotedesktopdienste, explizilogon-Methode
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.ExplicitLogon
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef72b6b0f0ede0954a6fc74030a9f0f1d4976935
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392062"
---
# <a name="explicitlogon-method-of-the-win32_tslogonsetting-class"></a>Explizilogon-Methode der Win32- \_ Klasse "tlogonsetting"

Die **explizlogon** -Methode legt die Anmelde Informationen fest, die für die Authentifizierung verwendet werden.

## <a name="syntax"></a>Syntax


```mof
uint32 ExplicitLogon(
  [in] string UserName,
  [in] string Domain,
  [in] string Password
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Benutzername* \[ in\]
</dt> <dd>

Die Anmelde Informationen für den Benutzernamen.

</dd> <dt>

*Domäne* \[ in\]
</dt> <dd>

Anmelde Informationen für die Domäne.

</dd> <dt>

*Kennwort* \[ in\]
</dt> <dd>

Die Anmelde Informationen für die Kenn Wort Anmeldung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg Erfolg zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) . Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.

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

 

