---
title: Wiederherstellen des Systems
description: Wenn der Computer im Laufe der Zeit verwendet wird, werden Wiederherstellungspunkte im Datenarchiv gesammelt, ohne dass vom Benutzer eine Verwaltung oder ein Eingriff erforderlich ist.
ms.assetid: 9581eff5-44d0-407e-b7cb-d3e13910a936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c5ff4aef88ec9eca591ee3c1afb1ad570689a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340210"
---
# <a name="restoring-the-system"></a>Wiederherstellen des Systems

Wenn der Computer im Laufe der Zeit verwendet wird, werden Wiederherstellungspunkte im Datenarchiv gesammelt, ohne dass vom Benutzer eine Verwaltung oder ein Eingriff erforderlich ist. Wenn der Benutzer das System jemals in einem früheren Zustand wiederherstellen muss, werden die verfügbaren Wiederherstellungspunkte für den Benutzer über die Benutzeroberfläche der Systemwiederherstellung angezeigt. Der Benutzer kann einen dieser Wiederherstellungspunkte auswählen. Die einzige Möglichkeit, auf dieses Archiv von Wiederherstellungs Punkten zuzugreifen, ist die Benutzeroberfläche für die Systemwiederherstellung und die System Wiederherstellungs-API. Dies dient zum Schutz der Datenintegrität und zum Verhindern von versehentlichen Änderungen, die von Benutzern, Anwendungen oder anderen Agents vorgenommen werden.

Zum Wiederherstellen eines Systems führt die Systemwiederherstellung die Dateiänderungen, die an den überwachten Dateien vorgenommen wurden, rückgängig und erfasst den Dateistatus zum Zeitpunkt des ausgewählten Wiederherstellungs Punkts. Anschließend wird die aktuelle Registrierung durch die Datei ersetzt, die für den ausgewählten Wiederherstellungspunkt gespeichert ist.

Gehen Sie folgendermaßen vor, um sicherzustellen, dass Ihre Anwendung nach einer Wiederherstellung das gewünschte Verhalten hat:

-   Speichern Sie keine Informationen in der Registrierung, die den Benutzer Zugriff auf persönliche Datendateien oder-Anwendungen beim Wiederherstellen des Systems verhindern. Andernfalls müssen Sie einen Mechanismus bereitstellen, mit dem der Benutzer die Anwendungen herunterladen und neu installieren kann, ohne Sie erneut bezahlen zu müssen.
-   Verwenden Sie die [System Wiederherstellungs-API](system-restore-api.md) , um beim Installieren und deinstallieren sinnvolle Wiederherstellungspunkte zu erstellen.
-   In Windows XP müssen die zu schützenden Schlüssel Binärdateien für die Anwendung Erweiterungen verwenden, die mit den in Filelist.xml verwendeten übereinstimmen. Weitere Informationen finden Sie unter über [wachte Dateinamen Erweiterungen](monitored-file-extensions.md). Diese Datei wird nicht von Windows 7 und Windows Vista verwendet. Verwenden Sie keine überwachten Erweiterungs Typen für vom Benutzer bearbeitbare Dateien. Wenn Sie z. b. die persönliche Datendatei eines Benutzers mithilfe der Datei "Extension. ini" benennen, kann der Benutzer die Arbeit aufgrund einer Systemwiederherstellung verlieren.

 

 




