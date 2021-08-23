---
description: Windows Das Installationsprogramm kann digitale Signaturen verwenden, um beschädigte Ressourcen zu erkennen.
ms.assetid: fc982813-583b-4fcd-88d8-9de227994e7b
title: Msicert.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede88930cdb6cc616d8c39fb400f0c67c31eecd01d6d1a7d1832421cb394bcc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534544"
---
# <a name="msicertexe"></a>Msicert.exe

Windows Das Installationsprogramm kann digitale Signaturen verwenden, um beschädigte Ressourcen zu erkennen. Ein Signiererzertifikat kann mit dem Signiererzertifikat einer externen Ressource verglichen werden, die vom Paket installiert werden soll. Weitere Informationen finden Sie unter [Digitale Signaturen und Windows Installer.](digital-signatures-and-windows-installer.md)

MsiCert.exe ist ein Befehlszeilenprogramm, mit dem die [Tabelle MsiDigitalSignature](msidigitalsignature-table.md) und die [Tabelle MsiDigitalCertificate](msidigitalcertificate-table.md) mit den Digitalen Signaturinformationen einer externen Cab-Datei aufgefüllt werden können. Die Cab-Datei muss digital signiert und in der [Medientabelle](media-table.md)aufgeführt werden. MsiCert.exe verwendet die Signaturzertifikatinformationen aus dem digital signierten Schränk und erstellt die Tabellen MsiDigitalSignature und MsiDigitalCertificate und fügt sie der Datenbank hinzu, sofern sie noch nicht vorhanden sind.

## <a name="syntax"></a>Syntax

**msicert -d** *{database}* **-m** *{medieneintrag}* **-c** *{cabinet}* **\[ -h \]**

## <a name="command-line-options"></a>Befehlszeilenoptionen

Bei den Befehlszeilenoptionen wird die Groß-/Kleinschreibung nicht beachtet, und anstelle eines Bindestrichs können Schrägstrichtrennzeichen verwendet werden.



| Option | Parameter        | Beschreibung                                                                                             |
|--------|------------------|---------------------------------------------------------------------------------------------------------|
| -d     | <database> | Die Datenbank (.msi-Datei), die aktualisiert wird.                                                         |
| -M     | <media Id> | Der Eintrag im Feld DiskId der [Medientabelle](media-table.md) im Datensatz für die Cab-Datei. |
| -c     | <cabinet>  | Der Pfad zur digital signierten Cab-Datei.                                                          |
| -H     |                  | Fügen Sie den Hash der digitalen Signatur ein. Dies ist optional.                                            |



 

Dieses Tool ist nur in den [Windows SDK-Komponenten für Windows Installer-Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Installationsentwicklungstools](windows-installer-development-tools.md)
</dt> <dt>

[Veröffentlichte Versionen, Tools und Redistributables](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



