---
title: Setnetworkadapterlanaid-Methode der Win32_TSNetworkAdapterSetting-Klasse
description: Gibt die Nummer des lokalen Netzwerkadapters (Lana) des festzulegenden Netzwerkadapters an.
ms.assetid: a12c7f06-4ecf-40bd-98c5-a2583dd1754a
ms.tgt_platform: multiple
keywords:
- Setnetworkadapterlanaid-Methode Remotedesktopdienste
- Setnetworkadapterlanaid-Methode Remotedesktopdienste, Win32_TSNetworkAdapterSetting-Klasse
- Win32_TSNetworkAdapterSetting-Klasse Remotedesktopdienste, setnetworkadapterlanaid-Methode
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
ms.openlocfilehash: 00675ae6378041e6c06b82a7de3c1ccf27620f4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743496"
---
# <a name="setnetworkadapterlanaid-method-of-the-win32_tsnetworkadaptersetting-class"></a>Setnetworkadapterlanaid-Methode der Win32- \_ Klasse "znetworkadaptersetting"

Die **setnetworkadapterlanaid** -Methode gibt die Nummer des lokalen Netzwerkadapters (Lana) des festzulegenden Netzwerkadapters an. Wenn die angegebene Lana-ID ungültig ist oder nicht vorhanden ist, wird ein Fehler zurückgegeben. Die Liste der verfügbaren Lana-IDs wird durch Aufzählen der **deviceidlist** -Eigenschaft in der Win32-Klasse " [**\_ tnetworkadaptersetting**](win32-tsnetworkadaptersetting.md) " abgerufen.

## <a name="syntax"></a>Syntax


```mof
uint32 SetNetworkAdapterLanaID(
  [in] uint32 NetworkAdapterLanaID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Networkadapterlanaid* \[ in\]
</dt> <dd>

Lana-Nummer des festzulegenden Netzwerkadapters.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Bemerkungen

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

 

