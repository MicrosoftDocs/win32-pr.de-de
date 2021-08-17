---
title: ReinstallOpenPurchaseLicenseKeyPack-Methode der Win32_TSLicenseKeyPack-Klasse
description: Installiert ein Open License Remotedesktopdienste-Lizenzschlüsselpaket neu.
ms.assetid: 3E70711E-284A-466E-A733-1219F5E0B741
ms.tgt_platform: multiple
keywords:
- ReinstallOpenPurchaseLicenseKeyPack-Methode Remotedesktopdienste
- ReinstallOpenPurchaseLicenseKeyPack-Methode Remotedesktopdienste , Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack Klasse Remotedesktopdienste , ReinstallOpenPurchaseLicenseKeyPack-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6519e6eedc187b6db2ee93a776843b0f305430df7ae55e4356ebce4de5ad31d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137823"
---
# <a name="reinstallopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>ReinstallOpenPurchaseLicenseKeyPack-Methode der Win32 \_ TSLicenseKeyPack-Klasse

Installiert ein Open License Remotedesktopdienste-Lizenzschlüsselpaket neu.

## <a name="syntax"></a>Syntax


```mof
uint32 ReinstallOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sLicenseNumber* \[ In\]
</dt> <dd>

8-stellige numerische Zeichenfolge, die mit dem Lizenzschlüsselpaket bereitgestellt wird. Der *sLicenseNumber-Parameter* darf keine Bindestriche enthalten.

</dd> <dt>

*sAuthorizationNumber* \[ In\]
</dt> <dd>

15-zeichenige alphanumerische Zeichenfolge, die mit dem Lizenzschlüssel bereitgestellt wird. Der *sAuthorizationNumber-Parameter* darf keine Bindestriche enthalten.

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

Die Anzahl der zu installierende Lizenzen.

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

 

 





