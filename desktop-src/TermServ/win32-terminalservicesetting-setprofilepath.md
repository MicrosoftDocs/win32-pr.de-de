---
title: SetProfilePath-Methode der Win32_TerminalServiceSetting Klasse
description: Die SetProfilePath-Methode legt die ProfilePath-Eigenschaft für die -Klasse fest.
ms.assetid: a0dfe6a4-929c-45ec-bd31-7e0ffb6ce5de
ms.tgt_platform: multiple
keywords:
- SetProfilePath-Remotedesktopdienste
- SetProfilePath-Methode Remotedesktopdienste , Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting klasse Remotedesktopdienste , SetProfilePath-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetProfilePath
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fafbd3c4556899ad2602f0b7ca1897a7aff4a4db98e4773ea56d2405b9423f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119514330"
---
# <a name="setprofilepath-method-of-the-win32_terminalservicesetting-class"></a>SetProfilePath-Methode der Win32 \_ TerminalServiceSetting-Klasse

Die **SetProfilePath-Methode** legt die **ProfilePath-Eigenschaft** für die -Klasse fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetProfilePath(
  [in] string ProfilePath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ProfilePath* \[ In\]
</dt> <dd>

Der neue Wert für die **ProfilePath-Eigenschaft,** der den Profilpfad für den Computer angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt Success bei Erfolg zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Remotedesktopdienste finden Sie unter [Fehlercodes](terminal-services-wmi-provider-error-codes.md) für WMI-Anbieter.

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

