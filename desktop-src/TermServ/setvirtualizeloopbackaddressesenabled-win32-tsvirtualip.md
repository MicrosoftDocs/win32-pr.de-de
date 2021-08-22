---
title: SetVirtualizeLoopbackAddressesEnabled-Methode der Win32_TSVirtualIP-Klasse
description: Legt den VirtualizeLoopbackAddressesEnabled-Eigenschaftswert fest.
ms.assetid: 84A4FF36-82B3-462A-9D2E-C15DD99524E4
ms.tgt_platform: multiple
keywords:
- SetVirtualizeLoopbackAddressesEnabled-Remotedesktopdienste
- SetVirtualizeLoopbackAddressesEnabled-Methode Remotedesktopdienste , Win32_TSVirtualIP-Klasse
- Win32_TSVirtualIP klasse Remotedesktopdienste , SetVirtualizeLoopbackAddressesEnabled-Methode
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5168ddd271dcf013a7595be1e1bdf32cde91e8f9f3ce8cfebc3b9f39af1fa109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000489"
---
# <a name="setvirtualizeloopbackaddressesenabled-method-of-the-win32_tsvirtualip-class"></a>SetVirtualizeLoopbackAddressesEnabled-Methode der Win32 \_ TSVirtualIP-Klasse

Legt den **VirtualizeLoopbackAddressesEnabled-Eigenschaftswert** fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetVirtualizeLoopbackAddressesEnabled(
  [in] uint32 VirtualizeLoopbackAddressesEnabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VirtualizeLoopbackAddressesEnabled* \[ In\]
</dt> <dd>

Gibt an, ob loopback address virtualization aktiviert werden soll. Dies kann einer der folgenden Werte sein.

<dt>

0
</dt> <dd>

Aktivieren Sie die Loopback-Adressvirtualisierung nicht.

</dd> <dt>

1
</dt> <dd>

Aktivieren der Loopback-Adressvirtualisierung.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Remotedesktopdienste finden Sie unter [Fehlercodes](terminal-services-wmi-provider-error-codes.md) für WMI-Anbieter. Die -Methode gibt einen Fehler zurück, wenn sich die Einstellung unter der Gruppenrichtliniensteuerung befindet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                          |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)
</dt> </dl>

 

 





