---
title: Installlicenskeypack-Methode der Win32_TSLicenseKeyPack-Klasse
description: Installiert ein Remotedesktopdienste Lizenzschlüssel Paket, das die über das Internet oder das Telefon empfangene Lizenz-ID verwendet.
ms.assetid: 1e545186-cc01-4700-857f-9390e1b73923
ms.tgt_platform: multiple
keywords:
- Installlicenskeypack-Methode Remotedesktopdienste
- Installlicenskeypack-Methode Remotedesktopdienste, Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste, installlicenerkeypack-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bee5e03de19783a20eeafa3f652dd60b99e871c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949561"
---
# <a name="installlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Installlicenskeypack-Methode der Win32-Klasse "-Klasse". \_

Installiert ein Remotedesktopdienste Lizenzschlüssel Paket, das die über das Internet oder das Telefon empfangene Lizenz-ID verwendet.

## <a name="syntax"></a>Syntax


```mof
uint32 InstallLicenseKeyPack(
  [in]  string sLicenseKeyPackId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*slicenabkeypackid* \[ in\]
</dt> <dd>

Enthält den Lizenzcode mit 35 Zeichen. Nur die alphanumerische Zeichenfolge mit 35 Zeichen muss als Eingabe angegeben werden. Es sollten keine Bindestriche hinzugefügt werden.

</dd> <dt>

*Keypackid* \[ vorgenommen\]
</dt> <dd>

Empfängt den Key Pack-Bezeichner.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück. Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

