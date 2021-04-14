---
title: Registervmmplugin-Methode der Win32_SessionDirectoryVMMPlugin-Klasse
description: Registriert ein neues VMM-Plug-in.
ms.assetid: 8fa6109e-6320-4ad1-b313-f100d8383f85
ms.tgt_platform: multiple
keywords:
- Registervmmplugin-Methode Remotedesktopdienste
- Registervmmplugin-Methode Remotedesktopdienste, Win32_SessionDirectoryVMMPlugin-Klasse
- Win32_SessionDirectoryVMMPlugin-Klasse Remotedesktopdienste, registervmmplugin-Methode
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.RegisterVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381be34f9398147b323fa99093479da48adfd480
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391722"
---
# <a name="registervmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Registervmmplugin-Methode der Win32- \_ Klasse sessiondirectoryvmmplugin

Registriert ein neues VMM-Plug-in.

## <a name="syntax"></a>Syntax


```mof
uint32 RegisterVMMPlugin(
  [in] string  sName,
  [in] string  sProvider,
  [in] string  sServiceLocation,
  [in] string  sClassID,
  [in] sint32  Priority = ,
  [in] boolean Enabled = 
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sname* \[ in\]
</dt> <dd>

Der Name des Plug-ins.

</dd> <dt>

*sprovider* \[ in\]
</dt> <dd>

Der Name des Plug-in-Anbieters.

</dd> <dt>

*sservicelokation* \[ in\]
</dt> <dd>

Der Dienst Speicherort, den das Plug-in kontaktieren soll.

</dd> <dt>

*sclassid* \[ in\]
</dt> <dd>

Der Klassen Bezeichner des Plug-ins.

</dd> <dt>

*Priorität* \[ in\]
</dt> <dd>

Die Priorität des Plug-ins. Je höher der Wert ist, desto höher ist die Priorität des Plug-ins.

</dd> <dt>

*Aktiviert* \[ in\]
</dt> <dd>

Gibt an, ob das Plug-in aktiviert oder deaktiviert ist. **True** , wenn das Plug-in aktiviert ist, andernfalls **false** .

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

 

 





