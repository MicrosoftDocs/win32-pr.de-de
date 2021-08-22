---
title: UninstallLicenseKeyPackWithId-Methode der Win32_TSLicenseKeyPack-Klasse
description: Deinstalliert das Remotedesktopdienste Lizenzschlüsselpaket mit dem angegebenen Schlüsselpaketbezeichner.
ms.assetid: ECB622AB-FAB4-4C5D-A007-E3ABA8E1D3E7
ms.tgt_platform: multiple
keywords:
- UninstallLicenseKeyPackWithId-Remotedesktopdienste
- UninstallLicenseKeyPackWithId-Methode Remotedesktopdienste , Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack klasse Remotedesktopdienste , UninstallLicenseKeyPackWithId-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.UninstallLicenseKeyPackWithId
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1218ce51beac9e20dd04e2a56d9075b6732d65e17689afaba5ce4d8f6669b1ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008440"
---
# <a name="uninstalllicensekeypackwithid-method-of-the-win32_tslicensekeypack-class"></a>UninstallLicenseKeyPackWithId-Methode der Win32 \_ TSLicenseKeyPack-Klasse

Deinstalliert das Remotedesktopdienste Lizenzschlüsselpaket mit dem angegebenen Schlüsselpaketbezeichner.

## <a name="syntax"></a>Syntax


```mof
uint32 UninstallLicenseKeyPackWithId(
  [in] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*KeyPackId* \[ In\]
</dt> <dd>

Der Bezeichner des zu deinstallierenden Schlüsselpakets.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





