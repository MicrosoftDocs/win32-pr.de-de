---
title: Selectallnetworkadapters-Methode der Win32_TSNetworkAdapterSetting-Klasse
description: Mit der selectallnetworkadapters-Methode werden alle Netzwerkadapter ausgewählt.
ms.assetid: e0bd60c3-55c3-4be9-be2d-3b97db3047d9
ms.tgt_platform: multiple
keywords:
- Selectallnetworkadapters-Methode Remotedesktopdienste
- Selectallnetworkadapters-Methode Remotedesktopdienste, Win32_TSNetworkAdapterSetting-Klasse
- Win32_TSNetworkAdapterSetting-Klasse Remotedesktopdienste, selectallnetworkadapters-Methode
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
ms.openlocfilehash: f68245c30fbdbf0721d138d1fc0386c779efe111
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340867"
---
# <a name="selectallnetworkadapters-method-of-the-win32_tsnetworkadaptersetting-class"></a>Selectallnetworkadapters-Methode der Win32- \_ Klasse "znetworkadaptersetting"

Mit der **selectallnetworkadapters** -Methode werden alle Netzwerkadapter ausgewählt.

## <a name="syntax"></a>Syntax


```mof
uint32 SelectAllNetworkAdapters();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

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

 

