---
title: SelectNetworkAdapterIP-Methode der Win32_TSNetworkAdapterSetting-Klasse
description: Wählt einen Netzwerkadapter basierend auf der IP-Adresse des Adapters aus.
ms.assetid: 7f89fb83-8abe-421b-a48b-876c093e3a3d
ms.tgt_platform: multiple
keywords:
- SelectNetworkAdapterIP-Methode Remotedesktopdienste
- SelectNetworkAdapterIP-Methode Remotedesktopdienste , Win32_TSNetworkAdapterSetting-Klasse
- Win32_TSNetworkAdapterSetting-Klasse Remotedesktopdienste , SelectNetworkAdapterIP-Methode
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SelectNetworkAdapterIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4a88c4820e4537d9c0fb1833b67eb2660a7fb5618189023dfe2217f222efa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008370"
---
# <a name="selectnetworkadapterip-method-of-the-win32_tsnetworkadaptersetting-class"></a>SelectNetworkAdapterIP-Methode der Win32 \_ TSNetworkAdapterSetting-Klasse

Wählt einen Netzwerkadapter basierend auf der IP-Adresse des Adapters aus.

## <a name="syntax"></a>Syntax


```mof
uint32 SelectNetworkAdapterIP(
  [in] string NetworkAdapterIP
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NetworkAdapterIP* \[ In\]
</dt> <dd>

Die IP-Adresse des festzulegende Netzwerkadapters.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn die angegebene IP-Adresse gültig ist, und gibt einen WMI-Fehlercode zurück, wenn die IP-Adresse ungültig ist oder nicht vorhanden ist. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Hinweise

Sie können die IP-Adresse eines Netzwerkadapters abrufen, indem Sie die Eigenschaften der [**Win32 \_ TSNetworkAdapterListSetting-Klasse**](win32-tsnetworkadapterlistsetting.md) auflisten.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

