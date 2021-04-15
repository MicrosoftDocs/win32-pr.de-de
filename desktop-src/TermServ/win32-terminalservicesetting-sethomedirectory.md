---
title: Die Methode "" der Klasse "Win32_TerminalServiceSetting".
description: Legt die terminalserviceshomedirectory-Eigenschaft für die-Klasse fest.
ms.assetid: 8173cd5b-965e-41bc-97cf-70d8729b8cea
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode ""
- Methode Remotedesktopdienste der Methode Win32_TerminalServiceSetting Klasse
- Win32_TerminalServiceSetting Klasse Remotedesktopdienste, Methode "Methode"
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetHomeDirectory
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1be732cae76b0681afd77693a07f673ef37c4a12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517678"
---
# <a name="sethomedirectory-method-of-the-win32_terminalservicesetting-class"></a>Setup Directory-Methode der Win32 \_ terminalservicesetts-Klasse

Die **sethomedirectory** -Methode legt die **terminalserviceshomedirectory** -Eigenschaft für die-Klasse fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetHomeDirectory(
  [in] string HomeDirectory
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Homedirectory* \[ in\]
</dt> <dd>

Der neue Wert für die **terminalserviceshomedirectory** -Eigenschaft, die das Stammverzeichnis des Computers angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg Erfolg zurück. Andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste der WMI-Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieter-Fehlercodes](terminal-services-wmi-provider-error-codes.md).

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

[**Win32 \_ terminalservicesetts**](win32-terminalservicesetting.md)
</dt> </dl>

 

