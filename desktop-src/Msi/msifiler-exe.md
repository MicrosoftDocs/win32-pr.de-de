---
description: MsiFiler.exe füllt die Dateitabelle mit Dateiversionen, Sprachen und Größen auf Grundlage eines Quell Verzeichnisses auf. Außerdem kann die msiflehash-Tabelle mit Dateihashes aktualisiert werden.
ms.assetid: cc3db60b-0b1d-4582-8b40-0b55f83e00be
title: Msifiler.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d7aeceae7abd8a9786079788e68c7d7bda35ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356735"
---
# <a name="msifilerexe"></a>Msifiler.exe

MsiFiler.exe füllt die [Dateitabelle](file-table.md) mit Dateiversionen, Sprachen und Größen auf Grundlage eines Quell Verzeichnisses auf. Außerdem kann die [msiflehash-Tabelle](msifilehash-table.md) mit Dateihashes aktualisiert werden.

## <a name="syntax"></a>Syntax

**msifiler.exe-d** *{Database}* **\[ -v \] \[ -h \] \[ -s altsource \]**

## <a name="command-line-options"></a>Befehlszeilenoptionen

Msifiler.exe verwendet die folgenden Befehlszeilenoptionen für die Groß-und Kleinschreibung. Ein Schrägstrich kann auch anstelle eines Bindestrichs verwendet werden.



| Option | Parameter   | BESCHREIBUNG                                                                                                                                                                  |
|--------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -d     | *database*  | Die zu Aktualisier Ende Datenbank (MSI-Datei).                                                                                                                              |
| -v     |             | Verwenden Sie den ausführlichen Modus.                                                                                                                                                            |
| -h     |             | Füllen Sie die [Tabelle "msiflehash](msifilehash-table.md)" auf. Dadurch wird die Tabelle erstellt, wenn Sie nicht bereits vorhanden ist. Die msiflehash-Tabelle kann nur mit Dateien ohne Versions Angabe verwendet werden. |
| -S     | *Altsource* | Altsource gibt ein alternatives Verzeichnis an, in dem die Dateien gefunden werden.                                                                                                              |



 

Dieses Tool ist nur in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwicklungs Tools für Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Verwenden der Verzeichnis Tabelle](using-the-directory-table.md)
</dt> <dt>

[Veröffentlichte Versionen, Tools und verteilbare Dateien](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



