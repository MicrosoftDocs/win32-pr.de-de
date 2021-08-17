---
description: 'Msival2.exe ist ein Befehlszeilenprogramm, das eine Reihe von internen Konsistenzauswertungen ausführen kann: ICEs.'
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

Msival2.exe ist ein Befehlszeilenprogramm, das eine Reihe von internen Konsistenzauswertungen [ausführen kann: ICEs](internal-consistency-evaluators-ices.md).

Dieses Tool ist nur in Windows [SDK-Komponenten für Windows Installer-Entwickler verfügbar.](platform-sdk-components-for-windows-installer-developers.md)

Weitere Informationen zu ICEs und der CUB-Datei finden Sie unter [Verwenden von internen Konsistenzauswertungen.](using-internal-consistency-evaluators.md)

## <a name="syntax"></a>Syntax

**Msiva2** *{database}{CUB file} \[ -f \] \[ -l {logfile} \] \[ -i {ICE Id} \[ :{ICE \] \] Id}...*

## <a name="command-line-options"></a>Befehlszeilenoptionen

Msival2.exe verwendet die folgenden Befehlszeilenoptionen, bei der die Groß-/Kleinschreibung nicht beachtet wird. Ein Schrägstrichtrennzeichen kann auch statt eines Bindestrichs verwendet werden.



| Option | Beschreibung                                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -f     | Filtern Sie alle Informationsmeldungen aus den angezeigten Ergebnissen heraus. Alle anderen Nachrichtentypen werden angezeigt.                                                                                                                                                                                              |
| -i     | Führen Sie nur die ICEs aus, die in der angegebenen Reihenfolge in der Befehlszeile aufgeführt sind. Jede benutzerdefinierte ICE-Aktion sollte so aufgeführt werden, wie sie in der [CustomAction-Tabelle](customaction-table.md) der CUB-Datei angezeigt wird. Wenn diese Option weggelassen wird, führt das Tool den Vom Autor der CUB-Datei angegebenen Standardsatz von ICEs aus. |
| -l     | Schreiben Sie Ergebnisse in die angegebene Datei. Die Datei darf nicht bereits vorhanden sein. Wenn die Datei vorhanden ist, wird sie nicht überschrieben.                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Installer-Entwicklungstools](windows-installer-development-tools.md)
</dt> <dt>

[Interne Konsistenzauswertungen – ICEs](internal-consistency-evaluators-ices.md)
</dt> <dt>

[Veröffentlichte Versionen, Tools und Redistributables](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



