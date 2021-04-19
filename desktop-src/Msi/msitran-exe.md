---
description: Msitran.exe verwendet msidatabasegeneratetransform, msikreatetransformsummaryinfo und msidatabaseapplytransform, um eine Transformations Datei zu generieren oder anzuwenden. Dieses Tool ist nur in den Windows SDK Komponenten für Windows Installer Entwickler verfügbar.
ms.assetid: cfc7b907-78d7-4a78-bab4-ede9012d5a36
title: Msitran.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a69936155fb3880f43e0f7563bc6aabd59f53703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364144"
---
# <a name="msitranexe"></a>Msitran.exe

Msitran.exe verwendet [**msidatabasegeneratetransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma), [**msikreatetransformsummaryinfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)und [**msidatabaseapplytransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) , um eine Transformations Datei zu generieren oder anzuwenden.

Dieses Tool ist nur in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.

## <a name="syntax"></a>Syntax

Verwenden Sie die folgende Syntax, um eine Transformation zu generieren.

**MsiTran-g** *{Base DB} {Ref DB} {Transformations Dateiname} \[ {Fehlerbedingungen/Überprüfungs Bedingungen \] }*

Verwenden Sie die folgende Syntax, um eine Transformation anzuwenden:

**MsiTran-a** *{Transform} {Database} \[ {Fehlerbedingungen} \]*

## <a name="command-line-options"></a>Befehlszeilenoptionen

Msitran.exe verwendet die folgenden Befehlszeilenoptionen für die Groß-und Kleinschreibung. Ein Schrägstrich kann auch anstelle eines Bindestrichs verwendet werden.



| Option | BESCHREIBUNG            |
|--------|------------------------|
| -g     | Transformations Generierung.  |
| -a     | Transformieren Sie die Anwendung. |



 

Die folgenden Fehler können beim Anwenden einer Transformation unterdrückt werden. Um einen Fehler zu unterdrücken, schließen Sie das entsprechende Zeichen in das Argument {error Conditions} ein. Die mit-g angegebenen Bedingungen werden in die Zusammenfassungs Informationen der Transformation eingefügt, aber beim Anwenden einer Transformation mit-a nicht verwendet. Weitere Informationen finden Sie unter [**msidatabaseapplytransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma).



| Option | Unterdrückte Fehler           |
|--------|----------------------------|
| a      | Fügen Sie eine vorhandene Zeile hinzu.          |
| b      | Löschen Sie eine nicht vorhandene Zeile.   |
| c      | Fügen Sie eine vorhandene Tabelle hinzu.        |
| d      | Nicht vorhandene Tabelle löschen. |
| e      | Ändern Sie die vorhandene Zeile.       |
| f      | Ändern Sie die Codepage.           |



 

Die folgenden Validierungs Bedingungen können verwendet werden, um anzugeben, wann eine Transformation auf ein Paket angewendet werden kann. Diese Bedingungen können mit-g, jedoch nicht mit-a angegeben werden.



| Option | Validierungs Bedingung                                  |
|--------|-------------------------------------------------------|
| g      | Aktivieren Sie den UpgradeCode.                                   |
| l      | Sprache überprüfen.                                       |
| p      | Plattform überprüfen.                                       |
| r      | Überprüfen Sie Product.                                        |
| s      | Überprüfen Sie nur die Hauptversion.                             |
| t      | Überprüfen Sie nur die Haupt-und neben Versionen.                  |
| u      | Überprüfen Sie die Haupt-, neben-und upgradeversionen.             |
| v      | Die Version der Datenbankversion < Basisdaten Bank Version.  |
| w      | Angewendete Datenbankversion <= Basisdaten Bank Version. |
| x      | Angewendete Datenbankversion = Basisdaten Bank Version.     |
| Y      | Angewendete Datenbankversion >= Basisdaten Bank Version. |
| z      | Die Version der Datenbankversion > Basisdaten Bank Version.  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwicklungs Tools für Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Daten Bank Transformationen](database-transforms.md)
</dt> <dt>

[Beispiel für eine Anpassungs Transformation](a-customization-transform-example.md)
</dt> <dt>

[Veröffentlichte Versionen, Tools und verteilbare Dateien](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



