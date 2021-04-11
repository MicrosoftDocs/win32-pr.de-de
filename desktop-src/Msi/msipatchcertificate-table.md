---
description: Gibt die möglichen Signatur Geber Zertifikate an, die zum digitalen Signieren von Patches verwendet werden.
ms.assetid: 8f76c27d-92f1-4de7-a69c-fba877e0325d
title: MsiPatchCertificate-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01648e792931fd856a1231a5d876c7db843479df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042388"
---
# <a name="msipatchcertificate-table"></a>MsiPatchCertificate-Tabelle

Die MsiPatchCertificate-Tabelle gibt Aufschluss über die möglichen Signatur Geber Zertifikate, mit denen Patches digital signiert werden. Die MsiPatchCertificate-Tabelle enthält die Informationen, die erforderlich sind, um das [Patchen von Benutzerkontensteuerung (UAC)](user-account-control--uac--patching.md) für eine Anwendung zu aktivieren.

Die MsiPatchCertificate-Tabelle weist die folgenden Spalten auf:



| Spalte               | Typ                         | Schlüssel | Nullwerte zulässig |
|----------------------|------------------------------|-----|----------|
| Patchzertifikat     | [Bezeichner](identifier.md) | J   | N        |
| Digitalcertificate\_ | [Bezeichner](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="PatchCertificate"></span><span id="patchcertificate"></span><span id="PATCHCERTIFICATE"></span>Patchzertifikat
</dt> <dd>

Der eindeutige Bezeichner für diese Zeile in der MsiPatchCertificate-Tabelle.

</dd> <dt>

<span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>Digitalcertificate
</dt> <dd>

Ein externer Schlüssel in die erste Spalte der [msidigitalcertificate-Tabelle](msidigitalcertificate-table.md). Die in der Tabelle "msidigitalcertificate" angegebene Zeile enthält die binäre Darstellung des Signatur Geber Zertifikats.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Patches werden immer anhand der MsiPatchCertificate-Tabelle ausgewertet, die zum Zeitpunkt der Anwendung des Patches aktuell ist. Ein Patch kann die MsiPatchCertificate-Tabelle ändern, indem Einträge hinzugefügt oder entfernt werden. Dies ermöglicht es einem Patch, die Auswertung zukünftiger Patches zu ändern, die später in der patchingsequenz angewendet werden. In der Tabelle können mehrere Zertifikate vorhanden sein, und der Patch muss mindestens einem anzuwendenden Zertifikat entsprechen.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE81](ice81.md)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Disableluapatching](disableluapatching.md)
</dt> <dt>

[Patching der Benutzerkontensteuerung (User Account Control, UAC)](user-account-control--uac--patching.md)
</dt> <dt>

[**Msidisableluapatching**](msidisableluapatching.md)
</dt> <dt>

[Digitale Signaturen und Windows Installer](digital-signatures-and-windows-installer.md)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



