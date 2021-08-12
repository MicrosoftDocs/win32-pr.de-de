---
title: SetName-Methode der Win32_SessionDirectoryVMMPlugin-Klasse
description: Legt den Namen des Plug-Ins fest.
ms.assetid: 8af4abca-f147-4027-91fb-4d669b58caa4
ms.tgt_platform: multiple
keywords:
- SetName-Methode Remotedesktopdienste
- SetName-Methode Remotedesktopdienste , Win32_SessionDirectoryVMMPlugin-Klasse
- Win32_SessionDirectoryVMMPlugin Klasse Remotedesktopdienste , SetName-Methode
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetName
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6960d08f39e7ce026a36d1644bebf49aec292a44d900974ebd8481379b00dcf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604639"
---
# <a name="setname-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>SetName-Methode der Win32 \_ SessionDirectoryVMMPlugin-Klasse

Legt den Namen des Plug-Ins fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetName(
  [in] string sName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sName* \[ In\]
</dt> <dd>

Der Name des Plug-Ins.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                      |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ SessionDirectoryVMMPlugin**](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





