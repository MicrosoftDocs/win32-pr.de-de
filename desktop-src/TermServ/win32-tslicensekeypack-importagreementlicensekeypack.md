---
title: ImportAgreementLicenseKeyPack-Methode der Win32_TSLicenseKeyPack-Klasse
description: Importiert von einem anderen Remotedesktop Lizenzserver ein Remotedesktopdienste Lizenzschlüsselpaket, das über einen Lizenzvertrag erworben wurde und automatisch eine Verbindung über das Internet herstellt, um die Key Pack-Lizenz zu überprüfen.
ms.assetid: 3C29E691-3734-4D39-A89F-F381F285DC9E
ms.tgt_platform: multiple
keywords:
- ImportAgreementLicenseKeyPack-Methode Remotedesktopdienste
- ImportAgreementLicenseKeyPack-Methode Remotedesktopdienste , Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste , ImportAgreementLicenseKeyPack-Methode
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
ms.openlocfilehash: 3b911a722f4f26aaf83debcb70413cb9dad2b40d2ca12b4ad3310aee4510ca1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603803"
---
# <a name="importagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>ImportAgreementLicenseKeyPack-Methode der Win32 \_ TSLicenseKeyPack-Klasse

Importiert von einem anderen Remotedesktop Lizenzserver ein Remotedesktopdienste Lizenzschlüsselpaket, das über einen Lizenzvertrag erworben wurde und automatisch eine Verbindung über das Internet herstellt, um die Key Pack-Lizenz zu überprüfen.

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

*AgreementType* \[ In\]
</dt> <dd>

Vereinbarungstyp.

<dt>

0
</dt> <dd>

Das Lizenzschlüsselpaket stammt aus einem Volumenlizenzvertrag auswählen (für Kunden mit 250 oder mehr Computern). Der *sAgreementNumber-Parameter* ist die Registrierungsnummer (sieben numerische Ziffern), die im Formular für die signierte Vereinbarung gefunden wurde.

</dd> <dt>

1
</dt> <dd>

Das Lizenzschlüsselpaket stammt aus einem Enterprise Volumenlizenzvertrag für Kunden mit 250 oder mehr Computern. Der *sAgreementNumber-Parameter* ist die Registrierungsnummer (sieben numerische Ziffern), die im Formular für die signierte Vereinbarung gefunden wurde.

</dd> <dt>

2
</dt> <dd>

Das Lizenzschlüsselpaket stammt aus einem Campus-Volumenlizenzvertrag für eine Höhere Bildungseinrichtung. Der *sAgreementNumber-Parameter* ist die Registrierungsnummer (sieben numerische Ziffern), die im Formular für die signierte Vereinbarung gefunden wurde.

</dd> <dt>

3
</dt> <dd>

Das Lizenzschlüsselpaket stammt aus einem Lizenzvertrag für das Schulvolumen für primäre und sekundäre Einrichtungen. Der *sAgreementNumber-Parameter* ist die Registrierungsnummer (sieben numerische Ziffern), die im Formular für die signierte Vereinbarung gefunden wurde.

</dd> <dt>

4
</dt> <dd>

Das Lizenzschlüsselpaket stammt aus einem Dienstanbieter-Lizenzvertrag für Dienstanbieter, mit dem Microsoft-Software monatlich lizenziert wird. Der *sAgreementNumber-Parameter* ist die Registrierungsnummer (sieben numerische Ziffern), die im Formular für die signierte Vereinbarung gefunden wurde.

</dd> <dt>

5
</dt> <dd>

Das Lizenzschlüsselpaket stammt aus einem anderen Lizenzvertrag, z. B. Open Value, Multi-Year Open License und Open Subscription License. Der *sAgreementNumber-Parameter* ist die Vertragsnummer, die mit Ihren Programminformationen bereitgestellt wird.

</dd> </dl> </dd> <dt>

*sAgreementNumber* \[ In\]
</dt> <dd>

Vertragsnummer oder Registrierungsnummer. Der *sAgreementNumber-Parameter* ist eine siebenstellige numerische Zeichenfolge ohne Bindestriche.

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

Der Produkttyp Remotedesktopdienste Lizenzschlüsselpakets ist pro Gerät. Daher muss jedes Gerät, das eine Verbindung mit dem RD-Sitzungshost-Server herstellt, über eine Lizenz verfügen.

</dd> <dt>

1
</dt> <dd>

Der Produkttyp Remotedesktopdienste Lizenzschlüsselpakets ist pro Benutzer. Daher muss jeder Benutzer, der eine Verbindung mit dem RD-Sitzungshost-Server herstellt, über eine Lizenz verfügen.

</dd> <dt>

2
</dt> <dd>

Dieser Produkttyp ist ungültig.

</dd> </dl> </dd> <dt>

*LicenseCount* \[ In\]
</dt> <dd>

Anzahl der zu importierende Lizenzen.

</dd> <dt>

*sSourceLSName* \[ In\]
</dt> <dd>

Der Name der Quelle Remotedesktop Lizenzservers. Dies ist entweder der vollqualifizierte Distinguished Name oder die IP-Adresse des Servers.

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

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

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

 

 





