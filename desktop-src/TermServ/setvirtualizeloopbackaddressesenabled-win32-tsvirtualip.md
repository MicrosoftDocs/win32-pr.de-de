---
title: Setvirtualizeloopbackaddressesaktivierte Methode der Win32_TSVirtualIP-Klasse
description: Legt den Wert der virtualizeloopbackaddressesaktivierten Eigenschaft fest.
ms.assetid: 84A4FF36-82B3-462A-9D2E-C15DD99524E4
ms.tgt_platform: multiple
keywords:
- Setvirtualizeloopbackaddressesaktivierte Methode Remotedesktopdienste
- Setvirtualizeloopbackaddressesaktivierte Methode Remotedesktopdienste, Win32_TSVirtualIP-Klasse
- Win32_TSVirtualIP Klasse Remotedesktopdienste, setvirtualizeloopbackaddressesaktivierte Methode
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
ms.openlocfilehash: ed74e74a9f0fcbcd070a50743e6182649c2dca08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339316"
---
# <a name="setvirtualizeloopbackaddressesenabled-method-of-the-win32_tsvirtualip-class"></a>Setvirtualizeloopbackaddressesaktivierte Methode der Win32- \_ Klasse "tvirtualip"

Legt den Wert der **virtualizeloopbackaddressesaktivierten** Eigenschaft fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetVirtualizeLoopbackAddressesEnabled(
  [in] uint32 VirtualizeLoopbackAddressesEnabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Virtualizeloopbackaddressesaktivierte* \[ in\]
</dt> <dd>

Gibt an, ob die Loopback adressvirtualisierung aktiviert werden soll. Dies kann einer der folgenden Werte sein:

<dt>

0
</dt> <dd>

Aktivieren Sie die Loopback adressvirtualisierung nicht.

</dd> <dt>

1
</dt> <dd>

Aktivieren der Loopback adressvirtualisierung.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) . Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ virtualialip**](win32-tsvirtualip.md)
</dt> </dl>

 

 





