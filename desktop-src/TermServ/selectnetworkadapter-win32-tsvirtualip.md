---
title: SelectNetworkAdapter-Methode der Win32_TSVirtualIP-Klasse
description: Legt die MAC-Adresse des Netzwerkadapters fest, der für die IP-Virtualisierung verwendet werden soll.
ms.assetid: ad67445c-6a8b-4980-997a-56aceb70965f
ms.tgt_platform: multiple
keywords:
- SelectNetworkAdapter-Methode Remotedesktopdienste
- SelectNetworkAdapter-Methode Remotedesktopdienste , Win32_TSVirtualIP-Klasse
- Win32_TSVirtualIP Klasse Remotedesktopdienste , SelectNetworkAdapter-Methode
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
ms.openlocfilehash: 7d27df38f8314720c4ed16d675cdbd06424611d2ccd127a45069586875c82d77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865520"
---
# <a name="selectnetworkadapter-method-of-the-win32_tsvirtualip-class"></a>SelectNetworkAdapter-Methode der Win32 \_ TSVirtualIP-Klasse

Legt die MAC-Adresse des Netzwerkadapters fest, der für die IP-Virtualisierung verwendet werden soll.

## <a name="syntax"></a>Syntax


```mof
uint32 SelectNetworkAdapter(
  [in] string NetworkAdapterMacAddress
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NetworkAdapterMacAddress* \[ In\]
</dt> <dd>

Typ: **Zeichenfolge**

Gibt die MAC-Adresse des Netzwerkadapters an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

Wenn die MAC-Adresse ungültig ist oder nicht vorhanden ist oder der IP-Virtualisierungsmodus pro Sitzung erfolgt, wird ein Fehler zurückgegeben.

Die -Methode gibt einen Fehler zurück, wenn die Einstellung der Gruppenrichtliniensteuerung unterliegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)
</dt> </dl>

 

 





