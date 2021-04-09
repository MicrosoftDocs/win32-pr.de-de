---
title: Importagreementlicenskeypack-Methode der Win32_TSLicenseKeyPack-Klasse
description: Importe von einem anderen Remotedesktop Lizenzserver, ein Remotedesktopdienste Lizenzschlüssel Paket, das über einen Lizenzvertrag gekauft wurde, und die automatische Verbindung über das Internet, um die Key Pack-Lizenz zu überprüfen.
ms.assetid: 3C29E691-3734-4D39-A89F-F381F285DC9E
ms.tgt_platform: multiple
keywords:
- Importagreementlicenskeypack-Methode Remotedesktopdienste
- Importagreementlicenskeypack-Methode Remotedesktopdienste, Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste, importagreementlicenskeypack-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff61d022f9cf195eb357817f7733f4ec49e2986f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106076"
---
# <a name="importagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Importagreementlicenskeypack-Methode der Win32-Klasse "" der \_ Klasse "zlicenabkeypack"

Importe von einem anderen Remotedesktop Lizenzserver, ein Remotedesktopdienste Lizenzschlüssel Paket, das über einen Lizenzvertrag gekauft wurde, und die automatische Verbindung über das Internet, um die Key Pack-Lizenz zu überprüfen.

## <a name="syntax"></a>Syntax


```mof
uint32 ImportAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
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

*Agreementtype* \[ in\]
</dt> <dd>

Vertragstyp.

<dt>

0
</dt> <dd>

Das Lizenzschlüssel Paket wird von einem SELECT-Volumenlizenzvertrag (für Kunden mit 250 oder mehr Computern) abgeleitet. Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular.

</dd> <dt>

1
</dt> <dd>

Das Lizenzschlüssel Paket basiert auf einem Enterprise-Volumenlizenzvertrag für Kunden mit 250 oder mehr Computern. Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular.

</dd> <dt>

2
</dt> <dd>

Das Lizenzschlüssel Paket basiert auf einem Campus-Volumenlizenzvertrag für eine höhere Bildungseinrichtung. Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular.

</dd> <dt>

3
</dt> <dd>

Das Lizenzschlüssel Paket wird von einem Schul-Volumenlizenzvertrag für primäre und sekundäre Einrichtungen abgeleitet. Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular.

</dd> <dt>

4
</dt> <dd>

Das Lizenzschlüssel Paket wird von einem Dienstanbieter-Lizenzvertrag für Dienstanbieter zum Lizenzieren von Microsoft-Software auf monatlicher Basis. Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular.

</dd> <dt>

5
</dt> <dd>

Das Lizenzschlüssel Paket ist aus einem anderen Lizenzvertrag, wie z. b. Open Value, Open-Year-Lizenz und Open-Abonnement-Lizenz. Der *sagreementnumber* -Parameter ist die Vertragsnummer, die mit ihren Programminformationen bereitgestellt wird.

</dd> </dl> </dd> <dt>

*sagreementnumber* \[ in\]
</dt> <dd>

Vertragsnummer oder Registrierungsnummer. Der *sagreementnumber* -Parameter ist eine siebenstellige numerische Zeichenfolge ohne Bindestriche.

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

Anzahl der zu importierenden Lizenzen.

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

 

 





