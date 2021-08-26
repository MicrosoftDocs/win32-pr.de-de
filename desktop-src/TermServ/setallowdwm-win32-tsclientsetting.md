---
title: SetAllowDwm-Methode der Win32_TSClientSetting-Klasse
description: Legt die AllowDwm-Eigenschaft fest.
ms.assetid: c70d3dc9-c109-4d77-be50-20a0352282d6
ms.tgt_platform: multiple
keywords:
- SetAllowDwm-Methode Remotedesktopdienste
- SetAllowDwm-Methode Remotedesktopdienste , Win32_TSClientSetting-Klasse
- Win32_TSClientSetting-Klasse Remotedesktopdienste , SetAllowDwm-Methode
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetAllowDwm
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30e48373859e59464986aab85bf00d16a76a066bad12e3e38bf7b07275257016
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009030"
---
# <a name="setallowdwm-method-of-the-win32_tsclientsetting-class"></a>SetAllowDwm-Methode der Win32 \_ TSClientSetting-Klasse

Legt die **AllowDwm-Eigenschaft** fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetAllowDwm(
  [in] uint32 AllowDwm
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AllowDwm* \[ In\]
</dt> <dd>

Der neue **AllowDwm-Eigenschaftswert.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode. Eine Liste dieser Werte finden [Sie unter Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md) Die -Methode gibt einen Fehler zurück, wenn die Verbindungseinstellungen des Benutzers vom Server überschrieben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                       |
| Ende des Supports (Client)<br/>    | Nicht unterstützt<br/>                                                               |
| Ende des Supports (Server)<br/>    | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

 





