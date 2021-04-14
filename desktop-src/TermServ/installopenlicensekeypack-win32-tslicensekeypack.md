---
title: Installopenlicenskeypack-Methode der Win32_TSLicenseKeyPack-Klasse
description: Installiert ein Open License Remotedesktopdienste License Key Pack.
ms.assetid: be50e25c-cda3-408b-934b-51ce343f3271
ms.tgt_platform: multiple
keywords:
- Installopenlicenskeypack-Methode Remotedesktopdienste
- Installopenlicenskeypack-Methode Remotedesktopdienste, Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste, installopenlicenabkeypack-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallOpenLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7335f25d3118c14f8cd0d27f72fd6a8d4cf1e0ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475945"
---
# <a name="installopenlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Installopenlicenerkeypack-Methode der Win32-Klasse "-Klasse". \_

Installiert ein Open License Remotedesktopdienste License Key Pack.

## <a name="syntax"></a>Syntax


```mof
uint32 InstallOpenLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a>Parameter

*slicensenum* \[ in\]

numerische Zeichenfolge mit 8 Zeichen, die mit dem Lizenzschlüssel Paket bereitgestellt wird. Der *slicensenreber* -Parameter darf keine Bindestriche enthalten.

*sauthorizationnumber* \[ in\]

eine alphanumerische Zeichenfolge mit 15 Zeichen, die mit dem Lizenzschlüssel bereitgestellt wird. Der *sauthorizationnumber* -Parameter darf keine Bindestriche enthalten.

*ProductVersion* \[ in\]

Die Produktversion.

| Wert | BESCHREIBUNG |
|-------|-------------|
| 0 | Nicht unterstützt |
| 1 | Nicht unterstützt |
| 2 | Windows Server 2008/Windows Server 2008 R2 |
| 4 | Windows Server 2012/Windows Server 2012 R2 |
| 5 | Windows Server 2016 |
| 6 | Windows Server 2019 |

*ProductType* \[ in\]
</dt> <dd>

Produkttyp.

| Wert | BESCHREIBUNG |
|-------|-------------|
| 0 | Der Produkttyp Remotedesktopdienste License Key Pack ist pro Gerät. Daher muss jedes Gerät, das eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen. |
| 1 | Der Product Type für Remotedesktopdienste License Key Pack ist pro Benutzer. Daher muss jeder Benutzer, der eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen. |
| 2 | Der Produkttyp ist ungültig. |

*Lizenz Anzahl* \[ in\]

Die Anzahl der zu installierenden Lizenzen.

*Keypackid* \[ vorgenommen\]

Empfängt den Key Pack-Bezeichner.

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

 

