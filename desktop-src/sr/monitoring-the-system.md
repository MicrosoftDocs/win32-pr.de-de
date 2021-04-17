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
# <a name="monitoring-the-system"></a><span data-ttu-id="a32b9-103">System überwachen</span><span class="sxs-lookup"><span data-stu-id="a32b9-103">Monitoring the System</span></span>

<span data-ttu-id="a32b9-104">Die System Wiederherstellung in Windows Vista und höher speichert eine Kopie des Volumes, wenn ein Wiederherstellungspunkt erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="a32b9-104">System Restore in Windows Vista and later saves a copy of the volume when generating a restore point.</span></span> <span data-ttu-id="a32b9-105">Für die Systemwiederherstellung sind mindestens 300 MB freier Speicherplatz auf dem Systemlaufwerk bei der Installation erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a32b9-105">System Restore requires a minimum of 300 MB of free disk space on the system drive at installation.</span></span>

<span data-ttu-id="a32b9-106">Die Systemwiederherstellung in Windows XP überwacht einen Kernsatz von System-und Anwendungs Dateien und archiviert die Zustände dieser Dateien, bevor Systemänderungen vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="a32b9-106">System Restore in Windows XP monitors a core set of system and application files, archiving the states of these files before system changes are made.</span></span> <span data-ttu-id="a32b9-107">Die System Wiederherstellung speichert außerdem eine vollständige Momentaufnahme der Registrierung und einige dynamische Systemdateien.</span><span class="sxs-lookup"><span data-stu-id="a32b9-107">System Restore also saves a full snapshot of the registry and some dynamic system files.</span></span> <span data-ttu-id="a32b9-108">Für die Systemwiederherstellung sind mindestens 200 MB freier Speicherplatz auf dem Systemlaufwerk bei der Installation erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a32b9-108">System Restore requires a minimum of 200 MB of free disk space on the system drive at installation.</span></span> <span data-ttu-id="a32b9-109">Wenn die Menge an freiem Speicherplatz auf einem beliebigen Laufwerk unter 50 MB sinkt, schaltet die System Wiederherstellung in den Standbymodus um und beendet die Erstellung von Wiederherstellungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="a32b9-109">When the amount of free disk space falls below 50 MB on any drive, System Restore switches to standby mode and stops creating restore points.</span></span> <span data-ttu-id="a32b9-110">Zu diesem Zeitpunkt werden alle Wiederherstellungspunkte gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a32b9-110">All restore points are deleted at that time.</span></span> <span data-ttu-id="a32b9-111">Bei der Systemwiederherstellung wird die Erstellung von Wiederherstellungs Punkten erneut aktiviert und fortgesetzt, sobald auf dem Systemlaufwerk 200 MB freier Speicherplatz verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a32b9-111">System Restore reactivates and resumes creating restore points as soon as 200 MB of disk space is free on the system drive.</span></span> <span data-ttu-id="a32b9-112">Die von der Überwachung überwachten oder ausgeschlossenen Dateien werden in der Datei% windir% \\ system32 \\ Restore \\Filelist.xml angegeben.</span><span class="sxs-lookup"><span data-stu-id="a32b9-112">The files that are monitored or excluded from monitoring are specified in the file %windir%\\system32\\restore\\Filelist.xml.</span></span> <span data-ttu-id="a32b9-113">Weitere Informationen finden Sie unter über [wachte Dateinamen Erweiterungen](monitored-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="a32b9-113">For more information, see [Monitored File Name Extensions](monitored-file-extensions.md).</span></span>

 

 




