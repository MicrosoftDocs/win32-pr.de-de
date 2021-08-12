---
title: ChangeMode-Methode der Win32_TerminalServiceSetting Klasse
description: Die ChangeMode-Methode legt den Lizenzierungstyp des aktuellen Remotedesktop-Sitzungshost (RD-Sitzungshost) fest.
ms.assetid: 293483ee-51ce-4cd4-ba13-6c7c02bbdbbf
ms.tgt_platform: multiple
keywords:
- ChangeMode-Remotedesktopdienste
- ChangeMode-Methode Remotedesktopdienste , Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting klasse Remotedesktopdienste , ChangeMode-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.ChangeMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2812dd459e13922b1745e55355972092091b4fd9521bc41a46da40769c02021d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604039"
---
# <a name="changemode-method-of-the-win32_terminalservicesetting-class"></a>ChangeMode-Methode der Win32 \_ TerminalServiceSetting-Klasse

Die **ChangeMode-Methode** legt den Lizenzierungstyp des aktuellen Remotedesktop-Sitzungshost (RD-Sitzungshost) fest.

## <a name="syntax"></a>Syntax


```mof
uint32 ChangeMode(
  [in] uint32 LicensingType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LicensingType* \[ In\]
</dt> <dd>

Der Lizenzierungstyp, der basierend auf dem serverbasierten RD-Sitzungshost festgelegt werden soll.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Persönlicher RD-Sitzungshost Server.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Remotedesktop für die Verwaltung.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Pro Gerät/pro Platz. Gültig für Anwendungsserver.

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Pro Benutzer. Gültig für Anwendungsserver.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Remotedesktopdienste finden Sie unter [Fehlercodes](terminal-services-wmi-provider-error-codes.md) für WMI-Anbieter.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

