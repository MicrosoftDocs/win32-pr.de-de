---
title: Pinglicenseserver-Methode der Win32_TerminalServiceSetting-Klasse
description: Pinglicenseserver ist nicht mehr verfügbar.
ms.assetid: d2a9f273-1ff9-4391-889b-a3b9c9f95c3b
ms.tgt_platform: multiple
keywords:
- Pinglicenseserver-Methode Remotedesktopdienste
- Pinglicenseserver-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, pinglicenseserver-Methode
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
ms.openlocfilehash: 2fe7277b3130c88c1aec7716c1a3bf560b81db64
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391870"
---
# <a name="pinglicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Pinglicenseserver-Methode der Win32 \_ terminalservicesetts-Klasse

\[**Pinglicenseserver** ist nicht mehr für die Verwendung ab Windows Server 2008 R2 verfügbar.\]

**Windows Server 2008:** Pings an den Lizenzserver, um zu ermitteln, ob es sich um einen gültigen Lizenzserver handelt.

## <a name="syntax"></a>Syntax


```mof
uint32 PingLicenseServer(
  [in] string ServerName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Servername* \[ in\]
</dt> <dd>

Der Name des Lizenzservers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

<dl> <dt>

**S \_ OK**
</dt> <dd>

Der Server ist ein gültiger Lizenzserver.

</dd> <dt>

**S \_ false**
</dt> <dd>

Der Lizenzserver ist ungültig.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Ende des Supports (Client)<br/>    | Nicht unterstützt<br/>                                                               |
| Ende des Supports (Server)<br/>    | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ terminalservicesetts**](win32-terminalservicesetting.md)
</dt> </dl>

 

