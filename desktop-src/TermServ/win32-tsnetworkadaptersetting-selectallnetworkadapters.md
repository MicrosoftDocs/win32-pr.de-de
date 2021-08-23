---
title: SelectAllNetworkAdapters-Methode der Win32_TSNetworkAdapterSetting-Klasse
description: Die SelectAllNetworkAdapters-Methode wählt alle Netzwerkadapter aus.
ms.assetid: e0bd60c3-55c3-4be9-be2d-3b97db3047d9
ms.tgt_platform: multiple
keywords:
- SelectAllNetworkAdapters-Methode Remotedesktopdienste
- SelectAllNetworkAdapters-Methode Remotedesktopdienste , Win32_TSNetworkAdapterSetting-Klasse
- Win32_TSNetworkAdapterSetting Klasse Remotedesktopdienste , SelectAllNetworkAdapters-Methode
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SelectAllNetworkAdapters
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a359e3ea87c1c2f4567e752a714741c0f2617304f8d261e0baf811794d788895
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119420520"
---
# <a name="selectallnetworkadapters-method-of-the-win32_tsnetworkadaptersetting-class"></a>SelectAllNetworkAdapters-Methode der Win32 \_ TSNetworkAdapterSetting-Klasse

Die **SelectAllNetworkAdapters-Methode** wählt alle Netzwerkadapter aus.

## <a name="syntax"></a>Syntax


```mof
uint32 SelectAllNetworkAdapters();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode. Eine Liste dieser Werte finden Sie unter fehlercodes für [Remotedesktopdienste WMI-Anbieter.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation -Klassen (WMI). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

