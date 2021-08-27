---
description: Windows Das Installationsprogramm kann digitale Signaturen als Mittel zum Erkennen beschädigter Ressourcen verwenden.
ms.assetid: fc982813-583b-4fcd-88d8-9de227994e7b
title: Msicert.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1dbe8366093418e74ed4ab1cb8e8c23fb8036eb
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879739"
---
# <a name="msicertexe"></a>Msicert.exe

Windows Das Installationsprogramm kann digitale Signaturen als Mittel zum Erkennen beschädigter Ressourcen verwenden. Ein Signatorzertifikat kann mit dem Signatorzertifikat einer externen Ressource verglichen werden, die vom Paket installiert werden soll. Weitere Informationen finden Sie unter [Digitale Signaturen und Windows Installer](digital-signatures-and-windows-installer.md).

MsiCert.exe ist ein Befehlszeilenprogramm, das verwendet werden kann, um die [Tabelle MsiDigitalSignature](msidigitalsignature-table.md) und [msiDigitalCertificate](msidigitalcertificate-table.md) mit den digitalen Signaturinformationen einer externen Schränkdatei zu füllen. Die Schränkdatei muss digital signiert und in der [Media-Tabelle aufgeführt sein.](media-table.md) MsiCert.exe verwendet die Signaturzertifikatinformationen aus der digital signierten Schränkung und erstellt und fügt die Tabellen MsiDigitalSignature und MsiDigitalCertificate der Datenbank hinzu, sofern sie noch nicht vorhanden sind.

## <a name="syntax"></a>Syntax

**msicert -d** *{database}* **-m** *{Medieneintrag}* **-c** *{cabinet}* **\[ -h \]**

## <a name="command-line-options"></a>Befehlszeilenoptionen

Bei den Befehlszeilenoptionen wird die Groß-/Kleinschreibung nicht beachtet, und anstelle eines Bindestrichs können Schrägstrichtrennzeichen verwendet werden.



| Option | Parameter        | Beschreibung                                                                                             |
|--------|------------------|---------------------------------------------------------------------------------------------------------|
| -d     | &lt;database&gt; | Die Datenbank (.msi Datei), die aktualisiert wird.                                                         |
| -M     | <media Id> | Der Eintrag im Feld DiskId der [Media-Tabelle](media-table.md) im Datensatz für die Schränkdatei. |
| -c     | &lt;Kabinett&gt;  | Der Pfad zur digital signierten Schränkdatei.                                                          |
| -h     |                  | Schließen Sie den Hash der digitalen Signatur ein. Diese Eingabe ist optional.                                            |



 

Dieses Tool ist nur in Windows [SDK-Komponenten für Windows Installer-Entwickler verfügbar.](platform-sdk-components-for-windows-installer-developers.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Installer-Entwicklungstools](windows-installer-development-tools.md)
</dt> <dt>

[Veröffentlichte Versionen, Tools und Redistributables](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



