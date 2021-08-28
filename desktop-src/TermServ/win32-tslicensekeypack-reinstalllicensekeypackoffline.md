---
title: ReinstallLicenseKeyPackOffline-Methode der Win32_TSLicenseKeyPack-Klasse
description: Installiert ein Remotedesktopdienste Lizenzschlüsselpaket neu, das den Lizenzbezeichner verwendet, der über das Internet oder das Telefon empfangen wurde.
ms.assetid: CFDB4C3B-C7C1-4670-BC87-92727057A500
ms.tgt_platform: multiple
keywords:
- ReinstallLicenseKeyPackOffline-Methode Remotedesktopdienste
- ReinstallLicenseKeyPackOffline-Methode Remotedesktopdienste , Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste , ReinstallLicenseKeyPackOffline-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45b72ad2175e0d97cba5733461431726781aebc9a53c1a23f408f7d14e75dd35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058328"
---
# <a name="reinstalllicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a>ReinstallLicenseKeyPackOffline-Methode der Win32 \_ TSLicenseKeyPack-Klasse

Installiert ein Remotedesktopdienste Lizenzschlüsselpaket neu, das den Lizenzbezeichner verwendet, der über das Internet oder das Telefon empfangen wurde.

## <a name="syntax"></a>Syntax


```mof
uint32 ReinstallLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sLicenseKeyPackId* \[ In\]
</dt> <dd>

Enthält den Lizenzcode mit 35 Zeichen. Nur die alphanumerische Zeichenfolge mit 35 Zeichen sollte als Eingabe angegeben werden. Es sollten keine Bindestriche hinzugefügt werden.

</dd> <dt>

*KeyPackId* \[ out\]
</dt> <dd>

Empfängt den Schlüsselpaketbezeichner.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

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

 

 





