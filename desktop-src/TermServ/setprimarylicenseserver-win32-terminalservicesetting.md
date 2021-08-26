---
title: SetPrimaryLicenseServer-Methode der Win32_TerminalServiceSetting-Klasse
description: Legt den angegebenen Lizenzserver als ersten Eintrag in der Liste der angegebenen Lizenzserver fest.
ms.assetid: 8921e861-3b9a-49c5-a691-ded7be18ca0a
ms.tgt_platform: multiple
keywords:
- SetPrimaryLicenseServer-Methode Remotedesktopdienste
- SetPrimaryLicenseServer-Methode Remotedesktopdienste , Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting Klasse Remotedesktopdienste , SetPrimaryLicenseServer-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetPrimaryLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42eee8bbcab6494459ddde5c339f3836cab414ad3c2f5204399bac09e362c3ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008920"
---
# <a name="setprimarylicenseserver-method-of-the-win32_terminalservicesetting-class"></a>SetPrimaryLicenseServer-Methode der Win32 \_ TerminalServiceSetting-Klasse

Legt den angegebenen Lizenzserver als ersten Eintrag in der Liste der angegebenen Lizenzserver fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetPrimaryLicenseServer(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LicenseServerName* \[ In\]
</dt> <dd>

Der Name des Lizenzservers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode. Eine Liste dieser Werte finden [Sie unter Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

 





