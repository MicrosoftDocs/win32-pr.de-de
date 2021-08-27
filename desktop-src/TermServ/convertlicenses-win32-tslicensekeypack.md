---
title: ConvertLicenses-Methode der Win32_TSLicenseKeyPack Klasse
description: Konvertiert die Lizenzen im aktuellen Schlüsselpaket.
ms.assetid: 38600144-8fa2-4f9a-b7a4-7fafc304e7cb
ms.tgt_platform: multiple
keywords:
- ConvertLicenses-Remotedesktopdienste
- ConvertLicenses-Methode Remotedesktopdienste , Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack klasse Remotedesktopdienste , ConvertLicenses-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ConvertLicenses
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edfb65ea7429af14e633c8dee655b4977427e3a685e1404856fd9b5f2daf2ce4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099570"
---
# <a name="convertlicenses-method-of-the-win32_tslicensekeypack-class"></a>ConvertLicenses-Methode der Win32 \_ TSLicenseKeyPack-Klasse

Konvertiert die Lizenzen im aktuellen Schlüsselpaket. Wenn es sich bei der Lizenz um eine Benutzerlizenz handelt, wird sie in eine Gerätelizenz konvertiert. Wenn es sich bei der Lizenz um eine Gerätelizenz pro Gerät handelt, wird sie in eine Benutzerlizenz konvertiert.

## <a name="syntax"></a>Syntax


```mof
uint32 ConvertLicenses(
  [in]  uint32 Count,
  [out] uint32 KeypackID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anzahl* \[ In\]
</dt> <dd>

Die Anzahl der lizenzen, die konvertiert werden sollen.

</dd> <dt>

*KeypackID* \[ out\]
</dt> <dd>

Der Bezeichner des resultierenden Schlüsselpakets.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter Remotedesktopdienste [WMI-Anbieterfehlercodes](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





