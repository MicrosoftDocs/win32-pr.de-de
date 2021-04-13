---
title: Setservicelokation-Methode der Win32_SessionDirectoryVMMPlugin-Klasse
description: Legt den Dienst Speicherort für das Plug-in fest.
ms.assetid: e886a40b-9ea9-4159-a2ea-776160559410
ms.tgt_platform: multiple
keywords:
- Setservicelokation-Methode Remotedesktopdienste
- Setservicelokation-Methode Remotedesktopdienste, Win32_SessionDirectoryVMMPlugin-Klasse
- Win32_SessionDirectoryVMMPlugin-Klasse Remotedesktopdienste, setservicelokation-Methode
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
ms.openlocfilehash: 64c16a6bbe802052f53d28d4cd8cc2b9ab559b61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518164"
---
# <a name="setservicelocation-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Setservicelokation-Methode der Win32- \_ Klasse "sessiondirectoryvmmplugin"

Legt den Dienst Speicherort für das Plug-in fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetServiceLocation(
  [in] string sServiceLocation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sservicelokation* \[ in\]
</dt> <dd>

Der Dienst Speicherort, den das Plug-in kontaktieren soll.

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

 

 





