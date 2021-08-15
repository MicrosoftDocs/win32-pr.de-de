---
description: 'Msival2.exe ist ein Befehlszeilenprogramm, das eine Sammlung interner Konsistenzauswertungen ausführen kann: ICEs.'
ms.assetid: c48f4584-732a-468d-a651-2c09ce3c9ddd
title: Msival2.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8ed1228413d5b2fab0dfab79ea4546a9d15e74c8c62e9b1ca9751699f469854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943877"
---
# <a name="msival2exe"></a>Msival2.exe

Msival2.exe ist ein Befehlszeilenprogramm, das eine Sammlung interner [Konsistenzauswertungen](internal-consistency-evaluators-ices.md)ausführen kann: ICEs.

Dieses Tool ist nur in den [Windows SDK-Komponenten für Windows Installer-Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.

Weitere Informationen zu ICEs und der CUB-Datei finden Sie unter [Verwenden von internen Konsistenzauswertungen.](using-internal-consistency-evaluators.md)

## <a name="syntax"></a>Syntax

**Msival2** *{database}{CUB file} \[ -f \] \[ -l {logfile} \] \[ -i {ICE Id} \[ :{ICE \] \] Id}...*

## <a name="command-line-options"></a>Befehlszeilenoptionen

Msival2.exe verwendet die folgenden Befehlszeilenoptionen, bei der die Groß-/Kleinschreibung nicht beachtet wird. Anstelle eines Bindestrichs kann auch ein Schrägstrichtrennzeichen verwendet werden.



| Option | BESCHREIBUNG                                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -f     | Filtern Sie alle Informationsmeldungen aus den angezeigten Ergebnissen heraus. Alle anderen Nachrichtentypen werden angezeigt.                                                                                                                                                                                              |
| -i     | Führen Sie nur die in der Befehlszeile aufgeführten ICEs in der angegebenen Reihenfolge aus. Jede benutzerdefinierte ICE-Aktion sollte so aufgelistet werden, wie sie in der [CustomAction-Tabelle](customaction-table.md) der CUB-Datei angezeigt wird. Wenn diese Option weggelassen wird, führt das Tool den vom Autor der CUB-Datei angegebenen Standardsatz von ICEs aus. |
| -l     | Schreibt Ergebnisse in die angegebene Datei. Die Datei darf nicht bereits vorhanden sein. Wenn die Datei vorhanden ist, wird sie nicht überschrieben.                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Installationsentwicklungstools](windows-installer-development-tools.md)
</dt> <dt>

[Interne Konsistenzauswertungen – ICEs](internal-consistency-evaluators-ices.md)
</dt> <dt>

[Veröffentlichte Versionen, Tools und Redistributables](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



