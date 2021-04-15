---
title: Convertlicenses-Methode der Win32_TSLicenseKeyPack-Klasse
description: Konvertiert die Lizenzen im aktuellen Schlüssel Paket.
ms.assetid: 38600144-8fa2-4f9a-b7a4-7fafc304e7cb
ms.tgt_platform: multiple
keywords:
- Convertlicenses-Methode Remotedesktopdienste
- Convertlicenses-Methode Remotedesktopdienste, Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste, convertlicenses-Methode
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
ms.openlocfilehash: 54f37b1d9804c5f14f89a7ff6b48f5f8fcbdc60b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391623"
---
# <a name="convertlicenses-method-of-the-win32_tslicensekeypack-class"></a>Convertlicenses-Methode der Win32- \_ Klasse "zlicenabkeypack"

Konvertiert die Lizenzen im aktuellen Schlüssel Paket. Wenn die Lizenz eine benutzerspezifische Lizenz ist, wird Sie in eine pro-Gerät-Lizenz konvertiert. Wenn die Lizenz eine pro-Gerät-Lizenz ist, wird Sie in eine benutzerspezifische Lizenz konvertiert.

## <a name="syntax"></a>Syntax


```mof
uint32 ConvertLicenses(
  [in]  uint32 Count,
  [out] uint32 KeypackID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anzahl* \[ in\]
</dt> <dd>

Die Anzahl der zu konvertierenden Lizenzen.

</dd> <dt>

*Keypackid* \[ vorgenommen\]
</dt> <dd>

Der Bezeichner des resultierenden Schlüssel Pakets.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                            |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>Tltaumiprov. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





