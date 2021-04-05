---
title: Removelsfromspecifiedlicenseserverlist-Methode der Win32_TerminalServiceSetting-Klasse
description: Entfernt den angegebenen Lizenzserver aus der Liste der angegebenen Lizenzserver.
ms.assetid: c25eebf9-3a21-41a0-bb7d-c3f909cd8087
ms.tgt_platform: multiple
keywords:
- Removelsfromspecifiedlicenseserverlist-Methode Remotedesktopdienste
- Removelsfromspecifiedlicenseserverlist-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, removelsfromspecifiedlicenseserverlist-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.RemoveLSFromSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 901c2676748e819290855df2de51e5d7936dc793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858900"
---
# <a name="removelsfromspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a>Removelsfromspecifiedlicenseserverlist-Methode der Win32 \_ terminalservicesetts-Klasse

Entfernt den angegebenen Lizenzserver aus der Liste der angegebenen Lizenzserver.

## <a name="syntax"></a>Syntax


```mof
uint32 RemoveLSFromSpecifiedLicenseServerList(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Licenseservername* \[ in\]
</dt> <dd>

Der Name des zu entfernenden Lizenzservers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ terminalservicesetts**](win32-terminalservicesetting.md)
</dt> <dt>

[**Addlstospecifiedlicenseserverlist**](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**Emptyspecifiedlicenseserverlist**](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**Getspecifiedlicenseserverlist**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[**Setspecifiedlicenseserverlist**](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





