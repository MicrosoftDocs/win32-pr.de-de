---
title: SetPriority-Methode der Win32_SessionDirectoryVMMPlugin-Klasse
description: Legt die Priorität des Plug-Ins fest.
ms.assetid: ddcf30cd-b87c-4869-80fc-ec92092e0df3
ms.tgt_platform: multiple
keywords:
- SetPriority-Methode Remotedesktopdienste
- SetPriority-Methode Remotedesktopdienste , Win32_SessionDirectoryVMMPlugin-Klasse
- Win32_SessionDirectoryVMMPlugin-Klasse Remotedesktopdienste , SetPriority-Methode
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetPriority
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dfe18b5998a1b8576cbd1a8f3c793e355469cfeff44f585dcb167a3b154803a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987740"
---
# <a name="setpriority-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>SetPriority-Methode der Win32 \_ SessionDirectoryVMMPlugin-Klasse

Legt die Priorität des Plug-Ins fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Priorität* \[ In\]
</dt> <dd>

Die Priorität des Plug-Ins. Je höher der Wert, desto höher ist die Priorität des Plug-Ins. Die Priorität ist standardmäßig 0 (null).

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

 

 





