---
title: Setprovider-Methode der Win32_SessionDirectoryVMMPlugin-Klasse
description: Legt den Namen des Plug-in-Anbieters fest.
ms.assetid: fefb7c19-2bab-4ae3-b88b-20da5fd19ff3
ms.tgt_platform: multiple
keywords:
- Setprovider-Methode Remotedesktopdienste
- Setprovider-Methode Remotedesktopdienste, Win32_SessionDirectoryVMMPlugin-Klasse
- Win32_SessionDirectoryVMMPlugin-Klasse Remotedesktopdienste, setprovider-Methode
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetProvider
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205a88ecbd67dcf3b009577fa7384e074cc68487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741480"
---
# <a name="setprovider-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Setprovider-Methode der Win32- \_ Klasse "sessiondirectoryvmmplugin"

Legt den Namen des Plug-in-Anbieters fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetProvider(
  [in] string sProvider
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sprovider* \[ in\]
</dt> <dd>

Der Name des Plug-in-Anbieters.

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

 

 





