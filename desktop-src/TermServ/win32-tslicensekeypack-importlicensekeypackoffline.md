---
title: Importlicenabkeypackoffline-Methode der Win32_TSLicenseKeyPack-Klasse
description: Importe von einem anderen Remotedesktop Lizenzserver, ein Remotedesktopdienste License Key Pack, das eine Lizenz-ID verwendet, die über das Internet oder das Telefon empfangen wurde.
ms.assetid: 69D65917-8B82-4C24-AFFA-BBE529D3883C
ms.tgt_platform: multiple
keywords:
- Importlicenabkeypackoffline-Methode Remotedesktopdienste
- Importlicenabkeypackoffline-Methode Remotedesktopdienste, Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste, importlicenabkeypackoffline-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de474cce6eb91cdc605588f7f4a63d97f985769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517870"
---
# <a name="importlicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a>Importlicenabkeypackoffline-Methode der Win32-Klasse "-Klasse". \_

Importe von einem anderen Remotedesktop Lizenzserver, ein Remotedesktopdienste License Key Pack, das eine Lizenz-ID verwendet, die über das Internet oder das Telefon empfangen wurde.

## <a name="syntax"></a>Syntax


```mof
uint32 ImportLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*slicenabkeypackid* \[ in\]
</dt> <dd>

Enthält den Lizenzcode mit 35 Zeichen. Nur die alphanumerische Zeichenfolge mit 35 Zeichen muss als Eingabe angegeben werden. Es sollten keine Bindestriche hinzugefügt werden.

</dd> <dt>

*ssourcelsname* \[ in\]
</dt> <dd>

Der Name der Quelle Remotedesktop Lizenzservers. Dies ist entweder der voll qualifizierte Distinguished Name oder die IP-Adresse des Servers.

</dd> <dt>

*ssourcelsproductid* \[ in\]
</dt> <dd>

Der Bezeichner des Remotedesktop-Lizenzservers. Bei handelt es sich um eine alphanumerische Zeichenfolge mit 35 Zeichen, die keine Bindestriche enthalten kann.

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

 

 





