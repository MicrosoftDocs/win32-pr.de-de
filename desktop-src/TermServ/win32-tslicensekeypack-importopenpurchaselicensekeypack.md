---
title: ImportOpenPurchaseLicenseKeyPack-Methode der Win32_TSLicenseKeyPack Klasse
description: Importiert von einem anderen Remotedesktop-Lizenzserver ein Open License Remotedesktopdienste License Key Pack.
ms.assetid: FE1923FF-5292-4080-AB51-88B8A6B2322C
ms.tgt_platform: multiple
keywords:
- ImportOpenPurchaseLicenseKeyPack-Remotedesktopdienste
- ImportOpenPurchaseLicenseKeyPack-Methode Remotedesktopdienste , Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack klasse Remotedesktopdienste , ImportOpenPurchaseLicenseKeyPack-Methode
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
ms.openlocfilehash: 768961bda04776a73d0aa74422ce0ed5088e041ee41e4732becd72914dcabf04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008470"
---
# <a name="importopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>ImportOpenPurchaseLicenseKeyPack-Methode der Win32 \_ TSLicenseKeyPack-Klasse

Importiert von einem anderen Remotedesktop-Lizenzserver ein Open License Remotedesktopdienste License Key Pack.

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

*sLicenseNumber* \[ In\]
</dt> <dd>

Numerische Zeichenfolge mit acht Zeichen, die mit dem Lizenzschlüsselpaket bereitgestellt wird. Der *sLicenseNumber-Parameter* darf keine Bindestriche enthalten.

</dd> <dt>

*sAuthorizationNumber* \[ In\]
</dt> <dd>

Alphanumerische Zeichenfolge mit 15 Zeichen, die mit dem Lizenzschlüssel bereitgestellt wird. Der *sAuthorizationNumber-Parameter* darf keine Bindestriche enthalten.

</dd> <dt>

*ProductVersion* \[ In\]
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

*ProductType* \[ In\]
</dt> <dd>

Produkttyp.

<dt>

0
</dt> <dd>

Der Remotedesktopdienste Lizenzschlüsselpaket-Produkttyp gilt pro Gerät. Daher muss jedes Gerät, das eine Verbindung mit RD-Sitzungshost Server herstellt, über eine Lizenz verfügen.

</dd> <dt>

1
</dt> <dd>

Der Remotedesktopdienste Lizenzschlüsselpaket-Produkttyp ist pro Benutzer. Daher muss jeder Benutzer, der eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen.

</dd> <dt>

2
</dt> <dd>

Dieser Produkttyp ist ungültig.

</dd> </dl> </dd> <dt>

*LicenseCount* \[ In\]
</dt> <dd>

Die Anzahl der zu importierenden Lizenzen

</dd> <dt>

*sSourceLSName* \[ In\]
</dt> <dd>

Der Name des Quell- Remotedesktop Lizenzservers. Dies ist entweder der vollqualifizierte Distinguished Name oder die IP-Adresse des Servers.

</dd> <dt>

*sSourceLSProductId* \[ In\]
</dt> <dd>

Der Remotedesktop Lizenzserverbezeichner. ist eine alphanumerische Zeichenfolge mit 35 Zeichen, die keine Bindestriche enthalten darf.

</dd> <dt>

*KeyPackId* \[ out\]
</dt> <dd>

Empfängt den Schlüsselpaketbezeichner.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





