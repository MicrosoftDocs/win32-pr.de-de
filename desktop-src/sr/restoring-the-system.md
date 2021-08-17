---
title: Wiederherstellen des Systems
description: Da der Computer im Laufe der Zeit verwendet wird, werden Wiederherstellungspunkte im Datenarchiv gesammelt, ohne dass der Benutzer eine Verwaltung oder einen Eingriff erfordert.
ms.assetid: 9581eff5-44d0-407e-b7cb-d3e13910a936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d7e54fd12bbb05dacd0c388c1867319189924d761a43d90c6f2a9f718f26e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857520"
---
# <a name="restoring-the-system"></a>Wiederherstellen des Systems

Da der Computer im Laufe der Zeit verwendet wird, werden Wiederherstellungspunkte im Datenarchiv gesammelt, ohne dass der Benutzer eine Verwaltung oder einen Eingriff erfordert. Wenn der Benutzer das System in einem früheren Zustand wiederherstellen muss, werden die verfügbaren Wiederherstellungspunkte für den Benutzer über die Benutzeroberfläche für die Systemwiederherstellung sichtbar gemacht. Der Benutzer kann einen dieser Wiederherstellungspunkte auswählen. Die einzige Möglichkeit, auf dieses Archiv von Wiederherstellungspunkten zuzugreifen, ist die Benutzeroberfläche für die Systemwiederherstellung und die Systemwiederherstellungs-API. Dies soll die Datenintegrität schützen und versehentliche Änderungen durch den Benutzer, Anwendungen oder andere Agents verhindern.

Zum Wiederherstellen eines Systems werden an überwachten Dateien vorgenommene Dateiänderungen durch die Systemwiederherstellung rückgängig gemacht, und der Dateizustand wird zum Zeitpunkt des ausgewählten Wiederherstellungspunkts wiederhergestellt. Anschließend wird die aktuelle Registrierung durch die registrierung ersetzt, die für den ausgewählten Wiederherstellungspunkt gespeichert wurde.

Gehen Sie wie folgt vor, um sicherzustellen, dass Ihre Anwendung nach einer Wiederherstellung das gewünschte Verhalten aufwies:

-   Speichern Sie keine Informationen in der Registrierung, die den Benutzerzugriff auf personenbezogene Datendateien oder Anwendungen bei der Systemwiederherstellung verhindern. Andernfalls müssen Sie einen Mechanismus bereitstellen, mit dem der Benutzer die Anwendungen herunterladen und neu installieren kann, ohne sie erneut bezahlen zu müssen.
-   Verwenden Sie die [Systemwiederherstellungs-API,](system-restore-api.md) um bei der Installation und Deinstallation aussagekräftige Wiederherstellungspunkte zu erstellen.
-   In Windows XP müssen die zu schützenden Binärdateien der Schlüsselanwendung Erweiterungen verwenden, die mit den in der Anwendung verwendeten Filelist.xml. Weitere Informationen finden Sie unter [Überwachte Dateinamenerweiterungen.](monitored-file-extensions.md) Diese Datei wird nicht von Windows 7 und Windows Vista verwendet. Verwenden Sie keine überwachten Erweiterungstypen für Dateien, die vom Benutzer bearbeitet werden können. Wenn Sie z. B. die personenbezogene Datendatei eines Benutzers mithilfe der Erweiterung .ini benennen, kann der Benutzer die Arbeit als Folge einer Systemwiederherstellung verlieren.

 

 




