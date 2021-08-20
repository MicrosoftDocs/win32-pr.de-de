---
description: Mergemodule (MSM-Dateien) können so konfiguriert werden, dass sie Attribute enthalten, die vom Consumer des Mergemoduls konfiguriert werden können.
ms.assetid: 461436f0-3a91-4a49-934a-f975bf13df40
title: Konfigurierbare Mergemodule
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0ca110b45e1ec9bd28662c24440124bb75d0dde73d6e425146e8be640ae2de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144269"
---
# <a name="configurable-merge-modules"></a>Konfigurierbare Mergemodule

Mergemodule (MSM-Dateien) können so konfiguriert werden, dass sie Attribute enthalten, die vom Consumer des Mergemoduls konfiguriert werden können. Dadurch kann das Mergemodul konfiguriert werden, wenn das Installationspaket und das Modul zusammengeführt und vom Endbenutzer installiert werden. Konfigurierbare Mergemodule erfordern Mergemod.dll 2.0, können aber in jeder Version des Windows ausgeführt werden.

Die Implementierung konfigurierbarer Mergemodule besteht aus zwei Teilen. Zunächst fügt der Autor des Mergemoduls beim Erstellen des Mergemoduls (MSM-Datei) Informationen zur Moduldatenbank hinzu, die angibt, welche Elemente geändert werden können und wie diese Elemente vom Modulbenutzer konfiguriert werden können. Der Autor fügt den Datenbanktabellen des [Mergemoduls](merge-module-database-tables.md) Einträge hinzu, die für konfigurierbare Informationen reserviert sind[(ModuleConfiguration-Tabelle](moduleconfiguration-table.md) und [ModuleSubsators-Tabelle),](modulesubstitution-table.md)aktualisiert die [ \_ Validierungstabelle](-validation-table.md)und fügt Der [ModuleIgnoreTable-Tabelle](moduleignoretable-table.md)Einträge für die konfigurierbaren Mergemodultabellen hinzu. Die Ergänzungen zur ModuleIgnore-Tabelle sind erforderlich, um das Modul mit Mergemod.dll versionen vor 2.0 kompatibel zu machen.

Zweitens verwendet der Endbenutzer des Moduls beim Zusammenführen des Moduls in einem Installationspaket (.msi Datei) ein Mergetool. Das Mergetool ruft Mergemod.dll, um die Konfigurationsinformationen im Modul für ein Clientkonfigurationstool verfügbar zu machen. Das Konfigurationstool kann mit dem Endbenutzer interagieren, muss jedoch nicht alle möglichen Konfigurationsoptionen verfügbar machen. Wenn der Benutzer eine Auswahl für ein konfigurierbares Element nicht bereitstellen kann, stellt das Modul möglicherweise einen Standardwert zur Verfügung. Nachdem der Benutzer dem Konfigurationstool seine Auswahl erteilt hat, ruft das Mergetool Mergemod.dll, um die Zusammenführung durchzuführen.

Konfigurierbare Mergemodule sind vollständig kompatibel mit Tools vor Mergemod.dll Version 2.0. In diesen Fällen verwendet das Tool die Standardwerte im Modul.

Weitere Informationen finden Sie unter [Verwenden konfigurierbarer Mergemodule.](using-configurable-merge-modules.md)

 

 



