---
title: PingLicenseServer-Methode der Win32_TerminalServiceSetting-Klasse
description: PingLicenseServer ist nicht mehr verfügbar.
ms.assetid: d2a9f273-1ff9-4391-889b-a3b9c9f95c3b
ms.tgt_platform: multiple
keywords:
- PingLicenseServer-Remotedesktopdienste
- PingLicenseServer-Methode Remotedesktopdienste , Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting klasse Remotedesktopdienste , PingLicenseServer-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.PingLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5a52268073a076c5dada44b7f34c6a6b3e0c820c0b9819f65d23081f4f6c37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866100"
---
# <a name="pinglicenseserver-method-of-the-win32_terminalservicesetting-class"></a>PingLicenseServer-Methode der Win32 \_ TerminalServiceSetting-Klasse

\[**PingLicenseServer** ist ab Windows Server 2008 R2 nicht mehr verfügbar.\]

**Windows Server 2008:** Pingt den Lizenzserver, um zu ermitteln, ob es sich um einen gültigen Lizenzserver handelt.

## <a name="syntax"></a>Syntax


```mof
uint32 PingLicenseServer(
  [in] string ServerName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ServerName* \[ In\]
</dt> <dd>

Name des Lizenzservers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

<dl> <dt>

**S \_ OK**
</dt> <dd>

Der Server ist ein gültiger Lizenzserver.

</dd> <dt>

**S \_ FALSE**
</dt> <dd>

Der Lizenzserver ist ungültig.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Ende des Supports (Client)<br/>    | Nicht unterstützt<br/>                                                               |
| Ende des Supports (Server)<br/>    | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

