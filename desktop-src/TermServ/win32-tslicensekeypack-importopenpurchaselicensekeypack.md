---
title: Importopenpurchaselicenskeypack-Methode der Win32_TSLicenseKeyPack-Klasse
description: Importe von einem anderen Remotedesktop Lizenzserver, einem Open License Remotedesktopdienste License Key Pack.
ms.assetid: FE1923FF-5292-4080-AB51-88B8A6B2322C
ms.tgt_platform: multiple
keywords:
- Importopenpurchaselicenskeypack-Methode Remotedesktopdienste
- Importopenpurchaselicenskeypack-Methode Remotedesktopdienste, Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste, importopenpurchaselicenskeypack-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 944bb1ce63150caece2cbc247af24542fde2d4f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339597"
---
# <a name="importopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Importopenpurchaselicenskeypack-Methode der Win32-Klasse "Klasse". \_

Importe von einem anderen Remotedesktop Lizenzserver, einem Open License Remotedesktopdienste License Key Pack.

## <a name="syntax"></a>Syntax


```mof
uint32 ImportOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*slicensenum* \[ in\]
</dt> <dd>

numerische Zeichenfolge mit 8 Zeichen, die mit dem Lizenzschlüssel Paket bereitgestellt wird. Der *slicensenreber* -Parameter darf keine Bindestriche enthalten.

</dd> <dt>

*sauthorizationnumber* \[ in\]
</dt> <dd>

eine alphanumerische Zeichenfolge mit 15 Zeichen, die mit dem Lizenzschlüssel bereitgestellt wird. Der *sauthorizationnumber* -Parameter darf keine Bindestriche enthalten.

</dd> <dt>

*ProductVersion* \[ in\]
</dt> <dd>

Die Produktversion.

<dt>

0
</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

1
</dt> <dd>

Wird nicht unterstützt.

</dd> <dt>

2
</dt> <dd>

Windows Server 2008

</dd> </dl> </dd> <dt>

*ProductType* \[ in\]
</dt> <dd>

Produkttyp.

<dt>

0
</dt> <dd>

Der Produkttyp Remotedesktopdienste License Key Pack ist pro Gerät. Daher muss jedes Gerät, das eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen.

</dd> <dt>

1
</dt> <dd>

Der Product Type für Remotedesktopdienste License Key Pack ist pro Benutzer. Daher muss jeder Benutzer, der eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen.

</dd> <dt>

2
</dt> <dd>

Der Produkttyp ist ungültig.

</dd> </dl> </dd> <dt>

*Lizenz Anzahl* \[ in\]
</dt> <dd>

Die Anzahl der zu importierenden Lizenzen.

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

 

 





