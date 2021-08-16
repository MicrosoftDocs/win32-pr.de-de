---
title: SetServiceLocation-Methode der Win32_SessionDirectoryVMMPlugin-Klasse
description: Legt den Dienstspeicherort für das Plug-In fest.
ms.assetid: e886a40b-9ea9-4159-a2ea-776160559410
ms.tgt_platform: multiple
keywords:
- SetServiceLocation-Methode Remotedesktopdienste
- SetServiceLocation-Methode Remotedesktopdienste , Win32_SessionDirectoryVMMPlugin-Klasse
- Win32_SessionDirectoryVMMPlugin-Klasse Remotedesktopdienste , SetServiceLocation-Methode
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetServiceLocation
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 437de0ab08b5735c1a981e5d04e8958a930d6eab1bfef79ccd7befa844a499dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349401"
---
# <a name="setservicelocation-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>SetServiceLocation-Methode der Win32 \_ SessionDirectoryVMMPlugin-Klasse

Legt den Dienstspeicherort für das Plug-In fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetServiceLocation(
  [in] string sServiceLocation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sServiceLocation* \[ In\]
</dt> <dd>

Der Dienststandort, an den das Plug-In sich wenden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode. Eine Liste dieser Werte finden [Sie unter Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

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

 

 





