---
description: Identifiziert die möglichen Signaturzertifikate, die zum digitalen Signieren von Patches verwendet werden.
ms.assetid: 8f76c27d-92f1-4de7-a69c-fba877e0325d
title: MsiPatchCertificate-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f39d2bc3a05c8b3fe3f23cd7dce01da36e14ce1f3984f24e827606bbc44c1a77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913310"
---
# <a name="msipatchcertificate-table"></a>MsiPatchCertificate-Tabelle

Die Tabelle MsiPatchCertificate identifiziert die möglichen Signaturzertifikate, die zum digitalen Signieren von Patches verwendet werden. Die Tabelle MsiPatchCertificate enthält die Informationen, die zum Aktivieren des Patchens der Benutzerkontensteuerung [(User Account Control, UAC)](user-account-control--uac--patching.md) für eine Anwendung erforderlich sind.

Die MsiPatchCertificate-Tabelle enthält die folgenden Spalten:



| Spalte               | Typ                         | Key | Nullwerte zulässig |
|----------------------|------------------------------|-----|----------|
| PatchCertificate     | [Identifier](identifier.md) | J   | N        |
| DigitalCertificate\_ | [Identifier](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="PatchCertificate"></span><span id="patchcertificate"></span><span id="PATCHCERTIFICATE"></span>PatchCertificate
</dt> <dd>

Der eindeutige Bezeichner für diese Zeile in der MsiPatchCertificate-Tabelle.

</dd> <dt>

<span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate
</dt> <dd>

Ein externer Schlüssel in der ersten Spalte der [MsiDigitalCertificate-Tabelle.](msidigitalcertificate-table.md) Die in der Tabelle MsiDigitalCertificate angegebene Zeile enthält die binäre Darstellung des Signiererzertifikats.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Patches werden immer anhand der MsiPatchCertificate-Tabelle ausgewertet, die zum Zeitpunkt der Anwendung des Patches aktuell ist. Ein Patch kann die MsiPatchCertificate-Tabelle ändern, indem Einträge hinzugefügt oder entfernt werden. Dadurch kann ein Patch die Auswertung zukünftiger Patches ändern, die später in der Patchsequenz angewendet werden. In der Tabelle können mehrere Zertifikate vorhanden sein, und der Patch muss mit mindestens einem Zertifikat übereinstimmen, das angewendet werden soll.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE81](ice81.md)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DisableLUAPatching](disableluapatching.md)
</dt> <dt>

[Patchen der Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md)
</dt> <dt>

[**MSIDISABLELUAPATCHING**](msidisableluapatching.md)
</dt> <dt>

[Digitale Signaturen und Windows Installer](digital-signatures-and-windows-installer.md)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



