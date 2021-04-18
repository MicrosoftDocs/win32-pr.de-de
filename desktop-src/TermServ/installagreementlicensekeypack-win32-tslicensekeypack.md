---
title: Installagreementlicenskeypack-Methode der Win32_TSLicenseKeyPack-Klasse
description: Installiert ein Remotedesktopdienste Lizenzschlüssel Paket, das über einen Lizenzvertrag gekauft wurde, und stellt automatisch eine Verbindung über das Internet her, um die Key Pack-Lizenz zu überprüfen.
ms.assetid: 70a0aac3-2709-47ba-bf6a-549393c4c115
ms.tgt_platform: multiple
keywords:
- Installagreementlicenskeypack-Methode Remotedesktopdienste
- Installagreementlicenskeypack-Methode Remotedesktopdienste, Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste, installagreementlicenerkeypack-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb891469feae169c1267c12c04af6d21415c309
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340369"
---
# <a name="installagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Installagreementlicenskeypack-Methode der Win32- \_ Klasse "plicenabkeypack"

Installiert ein Remotedesktopdienste Lizenzschlüssel Paket, das über einen Lizenzvertrag gekauft wurde, und stellt automatisch eine Verbindung über das Internet her, um die Key Pack-Lizenz zu überprüfen.

## <a name="syntax"></a>Syntax


```mof
uint32 InstallAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a>Parameter

*Agreementtype* \[ in\]

Vertragstyp.

| Wert | BESCHREIBUNG |
|-------|-------------|
| 0 | Das Lizenzschlüssel Paket wird von einem SELECT-Volumenlizenzvertrag (für Kunden mit 250 oder mehr Computern) abgeleitet. Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular. |
| 1 | Das Lizenzschlüssel Paket basiert auf einem Enterprise-Volumenlizenzvertrag für Kunden mit 250 oder mehr Computern. Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular. |
| 2 | Das Lizenzschlüssel Paket basiert auf einem Campus-Volumenlizenzvertrag für eine höhere Bildungseinrichtung. Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular. |
| 3 | Das Lizenzschlüssel Paket wird von einem Schul-Volumenlizenzvertrag für primäre und sekundäre Einrichtungen abgeleitet. Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular. |
| 4 | Das Lizenzschlüssel Paket wird von einem Dienstanbieter-Lizenzvertrag für Dienstanbieter zum Lizenzieren von Microsoft-Software auf monatlicher Basis. Der *sagreementnumber* -Parameter ist die Registrierungsnummer (sieben numerische Ziffern) im signierten Vereinbarungs Formular. |
| 5 | Das Lizenzschlüssel Paket ist aus einem anderen Lizenzvertrag, wie z. b. Open Value, Open-Year-Lizenz und Open-Abonnement-Lizenz. Der *sagreementnumber* -Parameter ist die Vertragsnummer, die mit ihren Programminformationen bereitgestellt wird. |

*sagreementnumber* \[ in\]

Vertragsnummer oder Registrierungsnummer. Der *sagreementnumber* -Parameter ist eine siebenstellige numerische Zeichenfolge ohne Bindestriche.

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

Produkttyp.

| Wert | BESCHREIBUNG |
|-------|-------------|
| 0 | Der Produkttyp Remotedesktopdienste License Key Pack ist pro Gerät. Daher muss jedes Gerät, das eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen. |
| 1 | Der Product Type für Remotedesktopdienste License Key Pack ist pro Benutzer. Daher muss jeder Benutzer, der eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen. |
| 2 | Der Produkttyp ist ungültig. |

*Lizenz Anzahl* \[ in\]

Anzahl der zu installierenden Lizenzen.

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

 

