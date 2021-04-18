---
title: Selectnetworkadapterip-Methode der Win32_TSNetworkAdapterSetting-Klasse
description: Wählt einen Netzwerkadapter auf der Grundlage der IP-Adresse des Adapters aus.
ms.assetid: 7f89fb83-8abe-421b-a48b-876c093e3a3d
ms.tgt_platform: multiple
keywords:
- Selectnetworkadapterip-Methode Remotedesktopdienste
- Selectnetworkadapterip-Methode Remotedesktopdienste, Win32_TSNetworkAdapterSetting-Klasse
- Win32_TSNetworkAdapterSetting-Klasse Remotedesktopdienste, selectnetworkadapterip-Methode
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
ms.openlocfilehash: 9590bab26b3cda2e20a3dc74c5e201a2f7f86f94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339144"
---
# <a name="selectnetworkadapterip-method-of-the-win32_tsnetworkadaptersetting-class"></a>Selectnetworkadapterip-Methode der Win32- \_ Klasse "tnetworkadaptersetting"

Wählt einen Netzwerkadapter auf der Grundlage der IP-Adresse des Adapters aus.

## <a name="syntax"></a>Syntax


```mof
uint32 SelectNetworkAdapterIP(
  [in] string NetworkAdapterIP
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Network adapterip* \[ in\]
</dt> <dd>

Die IP-Adresse des festzulegenden Netzwerkadapters.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn die angegebene IP-Adresse gültig ist, und gibt einen WMI-Fehlercode zurück, wenn die IP-Adresse ungültig oder nicht vorhanden ist. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Bemerkungen

Sie können die IP-Adresse eines Netzwerkadapters abrufen, indem Sie die Eigenschaften der Win32-Klasse "t Network [**\_ adapterlistsetting**](win32-tsnetworkadapterlistsetting.md) " auflisten.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32-Datei "t-Network \_ adaptersetting"**](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

