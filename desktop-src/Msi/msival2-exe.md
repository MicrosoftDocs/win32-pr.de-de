---
description: Msival2.exe ist ein Befehlszeilen-Hilfsprogramm, mit dem eine Suite interner Konsistenz Auswertung-ICES ausgeführt werden kann.
ms.assetid: c48f4584-732a-468d-a651-2c09ce3c9ddd
title: Msival2.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b70ca2ccdeaf72c5191f292a8fa3f9b4de5dd9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218531"
---
# <a name="msival2exe"></a>Msival2.exe

Msival2.exe ist ein Befehlszeilen-Hilfsprogramm, mit dem eine Suite [interner Konsistenz Auswertung-ICES](internal-consistency-evaluators-ices.md)ausgeführt werden kann.

Dieses Tool ist nur in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.

Weitere Informationen zu ICES und der CUB-Datei finden [Sie unter Using Internal Konsistenz Evaluators](using-internal-consistency-evaluators.md).

## <a name="syntax"></a>Syntax

**Msival2** *{Database} {CUB-Datei} \[ -f \] \[ -l {LogFile} \] \[ -i {Ice ID} \[ : {Ice ID}.. \] \] .*

## <a name="command-line-options"></a>Befehlszeilenoptionen

Msival2.exe verwendet die folgenden Befehlszeilenoptionen für die Groß-und Kleinschreibung. Ein Schrägstrich kann auch anstelle eines Bindestrichs verwendet werden.



| Option | BESCHREIBUNG                                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -f     | Filtert alle Informationsmeldungen aus den angezeigten Ergebnissen heraus. Alle anderen Nachrichten Typen werden angezeigt.                                                                                                                                                                                              |
| -i     | Führen Sie nur die in der Befehlszeile aufgelisteten ICES in der angegebenen Reihenfolge aus. Jede benutzerdefinierte Ice-Aktion sollte aufgeführt werden, wie Sie in der [Tabelle CustomAction](customaction-table.md) der CUB-Datei angezeigt wird. Wenn diese Option weggelassen wird, führt das Tool den Standardsatz von ICES aus, der vom Autor der CUB-Datei angegeben wird. |
| -l     | Schreiben Sie Ergebnisse in die angegebene Datei. Die Datei darf nicht bereits vorhanden sein. Wenn die Datei vorhanden ist, wird Sie nicht überschrieben.                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwicklungs Tools für Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Interne Konsistenz Auswertung-ICES](internal-consistency-evaluators-ices.md)
</dt> <dt>

[Veröffentlichte Versionen, Tools und verteilbare Dateien](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



