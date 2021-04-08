---
title: Selectnetworkadapter-Methode der Win32_TSVirtualIP-Klasse
description: Legt die Mac-Adresse des Netzwerkadapters fest, der für die IP-Virtualisierung verwendet werden soll.
ms.assetid: ad67445c-6a8b-4980-997a-56aceb70965f
ms.tgt_platform: multiple
keywords:
- Selectnetworkadapter-Methode Remotedesktopdienste
- Selectnetworkadapter-Methode Remotedesktopdienste, Win32_TSVirtualIP-Klasse
- Win32_TSVirtualIP-Klasse Remotedesktopdienste, selectnetworkadapter-Methode
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SelectNetworkAdapter
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a362bea1a5cacbfd727f23504f19164c79ce65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949796"
---
# <a name="selectnetworkadapter-method-of-the-win32_tsvirtualip-class"></a>Selectnetworkadapter-Methode der Win32- \_ Klasse "tvirtualip"

Legt die Mac-Adresse des Netzwerkadapters fest, der für die IP-Virtualisierung verwendet werden soll.

## <a name="syntax"></a>Syntax


```mof
uint32 SelectNetworkAdapter(
  [in] string NetworkAdapterMacAddress
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Networkadaptermacaddress* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Gibt die Mac-Adresse des Netzwerkadapters an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .

Wenn die Mac-Adresse ungültig ist oder nicht vorhanden ist oder der IP-Virtualisierungsmodus pro Sitzung erfolgt, wird ein Fehler zurückgegeben.

Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ virtualialip**](win32-tsvirtualip.md)
</dt> </dl>

 

 





