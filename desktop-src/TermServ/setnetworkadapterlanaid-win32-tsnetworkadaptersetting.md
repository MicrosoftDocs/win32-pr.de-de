---
title: SetNetworkAdapterLanaID-Methode der Win32_TSNetworkAdapterSetting-Klasse
description: Gibt die LANA-Nummer (Local Area Network Adapter) des festzulegenden Netzwerkadapters an.
ms.assetid: a12c7f06-4ecf-40bd-98c5-a2583dd1754a
ms.tgt_platform: multiple
keywords:
- SetNetworkAdapterLanaID-Methode Remotedesktopdienste
- SetNetworkAdapterLanaID-Methode Remotedesktopdienste , Win32_TSNetworkAdapterSetting-Klasse
- Win32_TSNetworkAdapterSetting-Klasse Remotedesktopdienste , SetNetworkAdapterLanaID-Methode
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SetNetworkAdapterLanaID
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b5ffe976da794714f01e711913c01216d6b9bfad30c8c337da1fbd4c796e5f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008960"
---
# <a name="setnetworkadapterlanaid-method-of-the-win32_tsnetworkadaptersetting-class"></a>SetNetworkAdapterLanaID-Methode der Win32 \_ TSNetworkAdapterSetting-Klasse

Die **SetNetworkAdapterLanaID-Methode** gibt die LANA-Nummer (Local Area Network Adapter) des festzulegenden Netzwerkadapters an. Wenn die angegebene LANA-ID ungültig ist oder nicht vorhanden ist, wird ein Fehler zurückgegeben. Die verfügbare Liste der LANA-IDs wird durch Auflisten der Eigenschaft **DeviceIDList** in der [**Win32 \_ TSNetworkAdapterSetting-Klasse**](win32-tsnetworkadaptersetting.md) abgerufen.

## <a name="syntax"></a>Syntax


```mof
uint32 SetNetworkAdapterLanaID(
  [in] uint32 NetworkAdapterLanaID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NetworkAdapterLanaID* \[ In\]
</dt> <dd>

LANA-Nummer des festzulegende Netzwerkadapters.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für WMI-Klassen (Windows Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

