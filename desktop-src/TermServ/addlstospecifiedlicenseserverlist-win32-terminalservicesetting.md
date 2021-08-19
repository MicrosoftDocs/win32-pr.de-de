---
title: AddLSToSpecifiedLicenseServerList-Methode der Win32_TerminalServiceSetting-Klasse
description: Fügt den angegebenen Lizenzserver am Ende der Liste der angegebenen Lizenzserver hinzu.
ms.assetid: 2aebe7c0-5ec2-4c2d-9887-7ecd2d6ec02a
ms.tgt_platform: multiple
keywords:
- AddLSToSpecifiedLicenseServerList-Methode Remotedesktopdienste
- AddLSToSpecifiedLicenseServerList-Methode Remotedesktopdienste , Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste , AddLSToSpecifiedLicenseServerList-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.AddLSToSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c747233cdb04bdacd78f7c799196262ecc9d2e5f3088d84db2837f21df8c06b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118856557"
---
# <a name="addlstospecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a>AddLSToSpecifiedLicenseServerList-Methode der Win32 \_ TerminalServiceSetting-Klasse

Fügt den angegebenen Lizenzserver am Ende der Liste der angegebenen Lizenzserver hinzu.

## <a name="syntax"></a>Syntax


```mof
uint32 AddLSToSpecifiedLicenseServerList(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LicenseServerName* \[ In\]
</dt> <dd>

Der Name des hinzuzufügende Lizenzservers.

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
</dt> <dt>

[**EmptySpecifiedLicenseServerList**](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**RemoveLSFromSpecifiedLicenseServerList**](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**SetSpecifiedLicenseServerList**](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





