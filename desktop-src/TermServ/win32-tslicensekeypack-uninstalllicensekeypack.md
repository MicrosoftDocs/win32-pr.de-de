---
title: UninstallLicenseKeyPack-Methode der Win32_TSLicenseKeyPack Klasse
description: Deinstalliert ein Remotedesktopdienste Lizenzschlüsselpaket.
ms.assetid: AF429AD7-C0DB-40AC-A4C6-591699FBF7E7
ms.tgt_platform: multiple
keywords:
- UninstallLicenseKeyPack-Remotedesktopdienste
- UninstallLicenseKeyPack-Methode Remotedesktopdienste , Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack klasse Remotedesktopdienste , UninstallLicenseKeyPack-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.UninstallLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb02ff8ecc84c346bef404071e8abb3988c0e7c8e70b54b288524e8ef790d5fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348621"
---
# <a name="uninstalllicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>UninstallLicenseKeyPack-Methode der Win32 \_ TSLicenseKeyPack-Klasse

Deinstalliert ein Remotedesktopdienste Lizenzschlüsselpaket.

## <a name="syntax"></a>Syntax


```mof
uint32 UninstallLicenseKeyPack(
  [in] unit32 ProductVersion,
  [in] unit32 ProductType,
  [in] uint32 LicenseCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ProductVersion* \[ In\]
</dt> <dd>

Produktversionsbezeichner für Remotedesktopdienste Lizenzschlüsselpaket.

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

Produkttyp des Remotedesktopdienste Lizenzschlüsselpakets.

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

Die Anzahl der zu deinstallierenden Lizenzen.

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

 

 





