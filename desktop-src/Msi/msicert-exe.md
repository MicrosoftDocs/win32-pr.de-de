---
description: Windows Installer können digitale Signaturen als Mittel zum erkennen beschädigter Ressourcen verwenden.
ms.assetid: fc982813-583b-4fcd-88d8-9de227994e7b
title: Msicert.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0a4df800bbcfa9ed2fb0d016794b3ebcf1535be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218534"
---
# <a name="msicertexe"></a>Msicert.exe

Windows Installer können digitale Signaturen als Mittel zum erkennen beschädigter Ressourcen verwenden. Ein Signatur Geber Zertifikat kann mit dem Signatur Geber Zertifikat einer externen Ressource verglichen werden, die vom Paket installiert werden soll. Weitere Informationen finden Sie unter [digitale Signaturen und Windows Installer](digital-signatures-and-windows-installer.md).

MsiCert.exe ist ein Befehlszeilen-Hilfsprogramm, das verwendet werden kann, um die [msidigitalsignature-Tabelle](msidigitalsignature-table.md) und die [msidigitalcertificate-Tabelle](msidigitalcertificate-table.md) mit den digitalen Signatur Informationen einer externen CAB-Datei aufzufüllen. Die CAB-Datei muss digital signiert und in der [Medien Tabelle](media-table.md)aufgeführt werden. MsiCert.exe verwendet die Signatur Geber Zertifikat Informationen aus der digital signierten CAB-Datei und erstellt und fügt die msidigitalsignature-und msidigitalcertificate-Tabellen der Datenbank hinzu, wenn diese nicht bereits vorhanden sind.

## <a name="syntax"></a>Syntax

**msicert-d** *{Database}* **-m** *{Medien Eintrag}* **-c** *{CAB}* **\[ -h \]**

## <a name="command-line-options"></a>Befehlszeilenoptionen

Bei den Befehlszeilenoptionen wird die Groß-/Kleinschreibung nicht beachtet, und es können Schrägstriche anstelle eines Bindestrichs verwendet werden.



| Option | Parameter        | BESCHREIBUNG                                                                                             |
|--------|------------------|---------------------------------------------------------------------------------------------------------|
| -d     | <database> | Die zu Aktualisier Ende Datenbank (MSI-Datei).                                                         |
| -M     | <media Id> | Der Eintrag im DiskId-Feld der [Medien Tabelle](media-table.md) im Datensatz für die CAB-Datei. |
| -c     | <cabinet>  | Der Pfad zur digital signierten CAB-Datei.                                                          |
| -h     |                  | Fügen Sie den Hash der digitalen Signatur ein. Diese Eingabe ist optional.                                            |



 

Dieses Tool ist nur in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwicklungs Tools für Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Veröffentlichte Versionen, Tools und verteilbare Dateien](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



