---
title: Reinstallretailpurchaselicenskeypack-Methode der Win32_TSLicenseKeyPack-Klasse
description: Neuinstallation eines Remotedesktopdienste Lizenzschlüssel Pakets, das über einen einzelhandelskanal gekauft wurde.
ms.assetid: 19528726-8DEB-4D03-BFA6-647C8A612FA2
ms.tgt_platform: multiple
keywords:
- Reinstallretailpurchaselicenabkeypack-Methode Remotedesktopdienste
- Reinstallretailpurchaselicenabkeypack-Methode Remotedesktopdienste, Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste, reinstallretailpurchaselicensskeypack-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4caa8635eaf28ad823add500883832a7fe885b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040199"
---
# <a name="reinstallretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Reinstallretailpurchaselicenskeypack-Methode der Win32- \_ Klasse "zlicenabkeypack"

Neuinstallation eines Remotedesktopdienste Lizenzschlüssel Pakets, das über einen einzelhandelskanal gekauft wurde.

## <a name="syntax"></a>Syntax


```mof
uint32 ReinstallRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*slicensecode* \[ in\]
</dt> <dd>

Enthält den 25-stelligen Lizenzcode. Nur die alphanumerische Zeichenfolge mit 25 Zeichen muss als Eingabe angegeben werden. Es sollten keine Bindestriche hinzugefügt werden.

</dd> <dt>

*Keypackid* \[ vorgenommen\]
</dt> <dd>

Empfängt den Key Pack-Bezeichner.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Tltaumiprov. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





