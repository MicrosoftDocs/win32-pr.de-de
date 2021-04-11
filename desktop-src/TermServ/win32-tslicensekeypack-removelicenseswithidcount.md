---
title: Removelicenseswithidcount-Methode der Win32_TSLicenseKeyPack-Klasse
description: Entfernt die angegebene Anzahl von Remotedesktopdienste Lizenzen aus dem angegebenen Schlüssel Paket.
ms.assetid: 36228659-7BE7-490A-A00C-A99FA66BFEB8
ms.tgt_platform: multiple
keywords:
- Removelicenseswithidcount-Methode Remotedesktopdienste
- Removelicenseswithidcount-Methode Remotedesktopdienste, Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste, removelicenseswithidcount-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.RemoveLicensesWithIdCount
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b2de1d1e0bfeed538e400436f8a88cd25ac563
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040198"
---
# <a name="removelicenseswithidcount-method-of-the-win32_tslicensekeypack-class"></a>Removelicenseswithidcount-Methode der Win32- \_ Klasse "zlicenserkeypack"

Entfernt die angegebene Anzahl von Remotedesktopdienste Lizenzen aus dem angegebenen Schlüssel Paket.

## <a name="syntax"></a>Syntax


```mof
uint32 RemoveLicensesWithIdCount(
  [in] uint32 KeyPackId,
  [in] uint32 LicenseCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Keypackid* \[ in\]
</dt> <dd>

Der Bezeichner des Schlüssel Pakets, das die zu entfernenden Lizenzen enthält.

</dd> <dt>

*Lizenz Anzahl* \[ in\]
</dt> <dd>

Die Anzahl der zu deinstallierenden Lizenzen.

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

 

 





