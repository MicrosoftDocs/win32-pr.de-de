---
title: SetPromptForPassword-Methode der Win32_TSLogonSetting-Klasse
description: Die SetPromptForPassword-Methode legt die PromptForPassword-Eigenschaft fest.
ms.assetid: eeeed374-4a8a-4014-833c-d931be3ef455
ms.tgt_platform: multiple
keywords:
- SetPromptForPassword-Remotedesktopdienste
- SetPromptForPassword-Methode Remotedesktopdienste , Win32_TSLogonSetting-Klasse
- Win32_TSLogonSetting der Remotedesktopdienste , SetPromptForPassword-Methode
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
ms.openlocfilehash: 90ea5202b0cfdfb624a05240deb042a88a8c73c8ea994cd810e1d9680ac0ddc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769520"
---
# <a name="setpromptforpassword-method-of-the-win32_tslogonsetting-class"></a>SetPromptForPassword-Methode der Win32 \_ TSLogonSetting-Klasse

Die **SetPromptForPassword-Methode legt** die **PromptForPassword-Eigenschaft** fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetPromptForPassword(
  [in] uint32 PromptForPassword
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PromptForPassword* \[ In\]
</dt> <dd>

Flag zum Deaktivieren oder Aktivieren der **PromptForPassword-Eigenschaft.**

<dt>

0
</dt> <dd>

Deaktiviert die Kennwortaufforderung.

</dd> <dt>

1
</dt> <dd>

Aktiviert die Kennwortaufforderung.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt Success bei Erfolg zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Remotedesktopdienste finden Sie unter [Fehlercodes](terminal-services-wmi-provider-error-codes.md) für WMI-Anbieter. Die -Methode gibt einen Fehler zurück, wenn sich die Einstellung unter der Gruppenrichtliniensteuerung befindet.

<dl> <dt>

**FALSE** (0)
</dt> <dt>

**TRUE** (1)
</dt> </dl>

## <a name="remarks"></a>Hinweise

Managed Object Format (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSLogonSetting**](win32-tslogonsetting.md)
</dt> </dl>

 

