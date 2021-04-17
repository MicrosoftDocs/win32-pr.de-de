---
title: System überwachen
description: System überwachen
ms.assetid: e0318aca-4e3e-4272-ba31-c770d6b05272
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da7d18f42ac091b9c73c4d9a9ac3929bed235310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387928"
---
# <a name="monitoring-the-system"></a>System überwachen

Die System Wiederherstellung in Windows Vista und höher speichert eine Kopie des Volumes, wenn ein Wiederherstellungspunkt erzeugt wird. Für die Systemwiederherstellung sind mindestens 300 MB freier Speicherplatz auf dem Systemlaufwerk bei der Installation erforderlich.

Die Systemwiederherstellung in Windows XP überwacht einen Kernsatz von System-und Anwendungs Dateien und archiviert die Zustände dieser Dateien, bevor Systemänderungen vorgenommen werden. Die System Wiederherstellung speichert außerdem eine vollständige Momentaufnahme der Registrierung und einige dynamische Systemdateien. Für die Systemwiederherstellung sind mindestens 200 MB freier Speicherplatz auf dem Systemlaufwerk bei der Installation erforderlich. Wenn die Menge an freiem Speicherplatz auf einem beliebigen Laufwerk unter 50 MB sinkt, schaltet die System Wiederherstellung in den Standbymodus um und beendet die Erstellung von Wiederherstellungs Punkten. Zu diesem Zeitpunkt werden alle Wiederherstellungspunkte gelöscht. Bei der Systemwiederherstellung wird die Erstellung von Wiederherstellungs Punkten erneut aktiviert und fortgesetzt, sobald auf dem Systemlaufwerk 200 MB freier Speicherplatz verfügbar sind. Die von der Überwachung überwachten oder ausgeschlossenen Dateien werden in der Datei% windir% \\ system32 \\ Restore \\Filelist.xml angegeben. Weitere Informationen finden Sie unter über [wachte Dateinamen Erweiterungen](monitored-file-extensions.md).

 

 




