---
description: Msitran.exe verwendet MsiDatabaseGenerateTransform, MsiCreateTransformSummaryInfo und MsiDatabaseApplyTransform, um eine Transformationsdatei zu generieren oder anzuwenden. Dieses Tool ist nur in Windows SDK-Komponenten für Windows Installer-Entwickler verfügbar.
ms.assetid: cfc7b907-78d7-4a78-bab4-ede9012d5a36
title: Msitran.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e09803623024bb593897411a5e852aa953335c31fd88f9e2e1922b89b53e9abf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944268"
---
# <a name="msitranexe"></a>Msitran.exe

Msitran.exe verwendet [**MsiDatabaseGenerateTransform,**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma) [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)und [**MsiDatabaseApplyTransform,**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) um eine Transformationsdatei zu generieren oder anzuwenden.

Dieses Tool ist nur in Windows [SDK-Komponenten für Windows Installer-Entwickler verfügbar.](platform-sdk-components-for-windows-installer-developers.md)

## <a name="syntax"></a>Syntax

Verwenden Sie die folgende Syntax, um eine Transformation zu generieren.

**msitran -g** *{Basisdatenbank}{ref db}{Name der Transformationsdatei} \[ {Fehlerbedingungen/Validierungsbedingungen} \]*

Verwenden Sie die folgende Syntax, um eine Transformation anzuwenden.

**msitran -a** *{transform}{database} \[ {error conditions} \]*

## <a name="command-line-options"></a>Befehlszeilenoptionen

Msitran.exe verwendet die folgenden Befehlszeilenoptionen, bei der die Groß-/Kleinschreibung nicht beachtet wird. Ein Schrägstrichtrennzeichen kann auch statt eines Bindestrichs verwendet werden.



| Option | BESCHREIBUNG            |
|--------|------------------------|
| -g     | Transformationsgenerierung.  |
| -a     | Transformieren der Anwendung. |



 

Die folgenden Fehler können beim Anwenden einer Transformation unterdrückt werden. Um einen Fehler zu unterdrücken, schließen Sie das entsprechende Zeichen in das {error conditions}-Argument ein. Bedingungen, die mit -g angegeben werden, werden in den Zusammenfassungsinformationen der Transformation platziert, werden jedoch nicht verwendet, wenn eine Transformation mit -a angewendet wird. Weitere Informationen finden Sie unter [**MsiDatabaseApplyTransform.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)



| Option | Unterdrückter Fehler           |
|--------|----------------------------|
| a      | Fügen Sie eine vorhandene Zeile hinzu.          |
| b      | Löschen Sie nicht vorhandene Zeilen.   |
| c      | Fügen Sie eine vorhandene Tabelle hinzu.        |
| d      | Löschen Sie eine nicht vorhandene Tabelle. |
| e      | Ändern Sie die vorhandene Zeile.       |
| f      | Codepage ändern.           |



 

Die folgenden Validierungsbedingungen können verwendet werden, um anzugeben, wann eine Transformation auf ein Paket angewendet werden kann. Diese Bedingungen können mit -g angegeben werden, aber nicht mit -a.



| Option | Validierungsbedingung                                  |
|--------|-------------------------------------------------------|
| g      | Überprüfen Sie den Upgradecode.                                   |
| l      | Überprüfen Sie die Sprache.                                       |
| p      | Überprüfen Sie die Plattform.                                       |
| r      | Überprüfen Sie das Produkt.                                        |
| s      | Überprüfen Sie nur die Hauptversion.                             |
| t      | Überprüfen Sie nur haupt- und nebenversionen.                  |
| u      | Überprüfen Sie Hauptversionen, Nebenversionen und Upgradeversionen.             |
| v      | Angewendete Datenbankversion < Basisdatenbankversion.  |
| w      | Angewendete Datenbankversion <= Basisdatenbankversion. |
| x      | Angewendete Datenbankversion = Basisdatenbankversion.     |
| y      | Angewendete Datenbankversion >= Basisdatenbankversion. |
| z      | Angewendete Datenbankversion > Basisdatenbankversion.  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Installer-Entwicklungstools](windows-installer-development-tools.md)
</dt> <dt>

[Datenbanktransformationen](database-transforms.md)
</dt> <dt>

[Beispiel für eine Anpassungstransformation](a-customization-transform-example.md)
</dt> <dt>

[Veröffentlichte Versionen, Tools und Redistributables](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



