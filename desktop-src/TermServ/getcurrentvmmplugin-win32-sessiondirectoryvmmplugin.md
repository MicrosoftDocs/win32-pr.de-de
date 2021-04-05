---
title: Getcurrentvmmplugin-Methode der Win32_SessionDirectoryVMMPlugin-Klasse
description: Ruft das Plug-in mit der höchsten Priorität ab, das aktiviert ist.
ms.assetid: 7712573f-2252-4a3c-820c-b679be5dfd46
ms.tgt_platform: multiple
keywords:
- Getcurrentvmmplugin-Methode Remotedesktopdienste
- Getcurrentvmmplugin-Methode Remotedesktopdienste, Win32_SessionDirectoryVMMPlugin-Klasse
- Win32_SessionDirectoryVMMPlugin-Klasse Remotedesktopdienste, getcurrentvmmplugin-Methode
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.GetCurrentVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7162322f4e5e3939309d64e27c93cf8d20da540c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859265"
---
# <a name="getcurrentvmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Getcurrentvmmplugin-Methode der Win32- \_ Klasse sessiondirectoryvmmplugin

Ruft das Plug-in mit der höchsten Priorität ab, das aktiviert ist.

## <a name="syntax"></a>Syntax


```mof
uint32 GetCurrentVMMPlugin(
  [out] string  sName,
  [out] string  sProvider,
  [out] string  sServiceLocation,
  [out] string  sClassID,
  [out] sint32  Priority,
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sname* \[ vorgenommen\]
</dt> <dd>

Der Name des Plug-ins.

</dd> <dt>

*sprovider* \[ vorgenommen\]
</dt> <dd>

Der Name des Plug-in-Anbieters.

</dd> <dt>

*sservicelokation* \[ vorgenommen\]
</dt> <dd>

Der Dienst Speicherort, den das Plug-in kontaktieren soll.

</dd> <dt>

*sclassid* \[ vorgenommen\]
</dt> <dd>

Der Klassen Bezeichner des Plug-ins.

</dd> <dt>

*Priorität* \[ vorgenommen\]
</dt> <dd>

Die Priorität des Plug-ins. Je höher der Wert ist, desto höher ist die Priorität des Plug-ins.

</dd> <dt>

*Aktiviert* \[ vorgenommen\]
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

 

 





