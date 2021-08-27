---
title: GetCurrentVMMPlugin-Methode der Win32_SessionDirectoryVMMPlugin-Klasse
description: Ruft das Plug-In mit der höchsten Priorität ab, das aktiviert ist.
ms.assetid: 7712573f-2252-4a3c-820c-b679be5dfd46
ms.tgt_platform: multiple
keywords:
- GetCurrentVMMPlugin-Methode Remotedesktopdienste
- GetCurrentVMMPlugin-Methode Remotedesktopdienste , Win32_SessionDirectoryVMMPlugin-Klasse
- Win32_SessionDirectoryVMMPlugin-Klasse Remotedesktopdienste , GetCurrentVMMPlugin-Methode
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
ms.openlocfilehash: 4cc683275581aeb00c654a30e8c5aba7fd920f58248b480fc39caa96c885bb7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080110"
---
# <a name="getcurrentvmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>GetCurrentVMMPlugin-Methode der Win32 \_ SessionDirectoryVMMPlugin-Klasse

Ruft das Plug-In mit der höchsten Priorität ab, das aktiviert ist.

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

*sName* \[ out\]
</dt> <dd>

Der Name des Plug-Ins.

</dd> <dt>

*sProvider* \[ out\]
</dt> <dd>

Der Name des Plug-In-Anbieters.

</dd> <dt>

*sServiceLocation* \[ out\]
</dt> <dd>

Der Dienststandort, an den das Plug-In sich wenden soll.

</dd> <dt>

*sClassID* \[ out\]
</dt> <dd>

Der Klassenbezeichner des Plug-Ins.

</dd> <dt>

*Priorität* \[ out\]
</dt> <dd>

Die Priorität des Plug-Ins. Je höher der Wert, desto höher ist die Priorität des Plug-Ins.

</dd> <dt>

*Aktiviert* \[ out\]
</dt> <dd>

Gibt an, ob das Plug-In aktiviert oder deaktiviert ist. **True,** wenn das Plug-In aktiviert ist, **andernfalls FALSE.**

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ SessionDirectoryVMMPlugin**](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





