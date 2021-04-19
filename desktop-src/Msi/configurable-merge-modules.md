---
description: Mergemodule (MSM-Dateien) können erstellt werden, um Attribute zu enthalten, die vom Consumer des Mergemoduls konfiguriert werden können.
ms.assetid: 461436f0-3a91-4a49-934a-f975bf13df40
title: Konfigurierbare Mergemodule
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716688d947ae84279dc3409bf97abe4eb58a69d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362738"
---
# <a name="configurable-merge-modules"></a>Konfigurierbare Mergemodule

Mergemodule (MSM-Dateien) können erstellt werden, um Attribute zu enthalten, die vom Consumer des Mergemoduls konfiguriert werden können. Dadurch kann das Mergemodul zu dem Zeitpunkt konfiguriert werden, zu dem das Installationspaket und das Modul vom Endbenutzer zusammengeführt und installiert werden. Konfigurierbare Mergemodule erfordern Mergemod.dll Version 2,0, können jedoch in jeder beliebigen Version der Windows Installer ausgeführt werden.

Die Implementierung konfigurierbarer Mergemodule besteht aus zwei Teilen. Beim Erstellen des Mergemoduls (MSM-Datei) fügt der Autor des Mergemoduls zunächst Informationen zur Modul Datenbank hinzu, die angibt, welche Elemente geändert werden können und wie diese Elemente vom Modul Benutzer konfiguriert werden können. Der Autor fügt Einträge zu den [Datenbanktabellen des Mergemoduls](merge-module-database-tables.md) hinzu, die für konfigurierbare Informationen reserviert sind ([ModuleConfiguration Table](moduleconfiguration-table.md) und [ModuleSubstitution Table](modulesubstitution-table.md)), aktualisiert die [ \_ Validierungs Tabelle](-validation-table.md)und fügt der [Tabelle moduleignoretable](moduleignoretable-table.md)Einträge für die konfigurierbaren mergemodultabellen hinzu. Die Ergänzungen der Tabelle moduleignore sind erforderlich, damit das Modul mit Mergemod.dll Versionen vor 2,0 kompatibel ist.

Zweitens: Wenn das Modul in ein Installationspaket (MSI-Datei) zusammengeführt wird, verwendet der Endbenutzer des Moduls ein Zusammenführungs Tool. Das Merge-Tool ruft Mergemod.dll auf, um die Konfigurationsinformationen im Modul einem Client Konfigurationstool zur Verfügung zu stellen. Das-Konfigurationstool kann mit dem Endbenutzer interagieren, muss jedoch nicht alle möglichen Konfigurationsoptionen verfügbar machen. Wenn der Benutzer die Auswahl für ein konfigurierbares Element ablehnt, kann das Modul einen Standardwert bereitstellen. Nachdem der Benutzer dem Konfigurationstool seine Auswahl erteilt hat, ruft das Merge-Tool Mergemod.dll auf, um den Merge auszuführen.

Konfigurierbare Mergemodule sind vollständig mit den Tools vor Mergemod.dll Version 2,0 kompatibel. In diesen Fällen verwendet das Tool die Standardwerte im Modul.

Weitere Informationen finden Sie unter [Verwenden von konfigurierbaren Mergemodulen](using-configurable-merge-modules.md).

 

 



