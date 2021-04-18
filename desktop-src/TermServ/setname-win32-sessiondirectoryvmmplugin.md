---
title: SetName-Methode der Win32_SessionDirectoryVMMPlugin-Klasse
description: Legt den Namen des Plug-ins fest.
ms.assetid: 8af4abca-f147-4027-91fb-4d669b58caa4
ms.tgt_platform: multiple
keywords:
- SetName-Methode Remotedesktopdienste
- SetName-Methode Remotedesktopdienste, Win32_SessionDirectoryVMMPlugin-Klasse
- Win32_SessionDirectoryVMMPlugin-Klasse Remotedesktopdienste, SetName-Methode
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
ms.openlocfilehash: 2dc9902e8d5931f0800dc6c62d36815f4f78db73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340667"
---
# <a name="setname-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>SetName-Methode der Win32- \_ Klasse "sessiondirectoryvmmplugin"

Legt den Namen des Plug-ins fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetName(
  [in] string sName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sname* \[ in\]
</dt> <dd>

Der Name des Plug-ins.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                      |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>"Tssdwmi. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ sessiondirector yvmmplugin**](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





