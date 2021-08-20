---
title: ImportLicenseKeyPackOffline-Methode der Win32_TSLicenseKeyPack Klasse
description: Importiert von einem anderen Remotedesktop-Lizenzserver ein Remotedesktopdienste-Lizenzschlüsselpaket, das eine Lizenz-ID verwendet, die über das Internet oder das Telefon empfangen wurde.
ms.assetid: 69D65917-8B82-4C24-AFFA-BBE529D3883C
ms.tgt_platform: multiple
keywords:
- ImportLicenseKeyPackOffline-Remotedesktopdienste
- ImportLicenseKeyPackOffline-Methode Remotedesktopdienste , Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack klasse Remotedesktopdienste , ImportLicenseKeyPackOffline-Methode
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
ms.openlocfilehash: 5c7d5be5dc8cfd9f654c09d989149a423351689f420a52ca1756fb197260e800
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348631"
---
# <a name="importlicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a>ImportLicenseKeyPackOffline-Methode der Win32 \_ TSLicenseKeyPack-Klasse

Importiert von einem anderen Remotedesktop-Lizenzserver ein Remotedesktopdienste-Lizenzschlüsselpaket, das eine Lizenz-ID verwendet, die über das Internet oder das Telefon empfangen wurde.

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

*sLicenseKeyPackId* \[ In\]
</dt> <dd>

Enthält den Lizenzcode mit 35 Zeichen. Als Eingabe sollte nur die alphanumerische Zeichenfolge mit 35 Zeichen angegeben werden. Es sollten keine Bindestriche hinzugefügt werden.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





