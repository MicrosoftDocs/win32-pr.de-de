---
title: Widerruf-Methode der Win32_TSIssuedLicense-Klasse
description: Widerruft die Remotedesktopdienste pro Geräte-Client Zugriffs Lizenzen (RDS \ 160; Pro-Gerät-CALs), die durch das Win32- \_ Objekt "tsissuedlicense" dargestellt werden. Dabei handelt es sich nicht um eine statische Funktion.
ms.assetid: b1eb7448-5d8e-4c2d-ba52-9363e8e0297a
ms.tgt_platform: multiple
keywords:
- Methode widerrufen Remotedesktopdienste
- Methode Remotedesktopdienste widerrufen, Win32_TSIssuedLicense Klasse
- Win32_TSIssuedLicense Klasse Remotedesktopdienste, Methode widerrufen
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense.Revoke
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63993ede5346f5b3cb56fcfa458d4cdce7dd58b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743624"
---
# <a name="revoke-method-of-the-win32_tsissuedlicense-class"></a>Widerruf-Methode der Win32- \_ Klasse "tsissuedlicense"

Widerruft die Remotedesktopdienste pro Geräte-Client Zugriffs Lizenzen (RDS pro Gerät CALs), die durch das Win32-Objekt " [**\_ tsissuedlicense**](win32-tsissuedlicense.md) " dargestellt werden. Dabei handelt es sich nicht um eine statische Funktion.

## <a name="syntax"></a>Syntax


```mof
uint32 Revoke(
  [out] uint32   RevokableCals,
  [out] DATETIME NextRevokeAllowedOn
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Revokablecals* \[ vorgenommen\]
</dt> <dd>

Anzahl der RDS-CALs desselben Typs wie das aktuelle Objekt, das widerrufen werden kann.

</dd> <dt>

*Nextrevokezuweisung* \[ vorgenommen\]
</dt> <dd>

Datum, an dem der Administrator das nächste Mal versuchen kann, Lizenzen aufzuheben. Dieser Parameter enthält nur gültige Daten, wenn der **Widerruf** Methoden Aufrufwert fehlgeschlagen ist, da die maximale Anzahl von Sperren erreicht wurde.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

Nur RDS-CALs pro Gerät können widerrufen werden.

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

[**Win32-" \_ tsissuedlicense"**](win32-tsissuedlicense.md)
</dt> </dl>

 

