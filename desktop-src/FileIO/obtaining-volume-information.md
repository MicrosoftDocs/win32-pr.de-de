---
description: Vor dem Zugriff auf Dateien und Verzeichnisse auf einem bestimmten Volume sollten Sie die Funktionen des Dateisystems mithilfe der GetVolumeInformation-Funktion ermitteln.
ms.assetid: 008e0cc4-bc12-47e8-a8b7-d4fa9395fceb
title: Abrufen von Volumeinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc5323c3f82db1115a81902f156e9366abad31e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527044"
---
# <a name="obtaining-volume-information"></a>Abrufen von Volumeinformationen

Die [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) -Funktion Ruft Informationen über das Dateisystem auf einem bestimmten Volume ab. Zu diesen Informationen gehören der Volumename, die Seriennummer des Volumes, der Dateisystem Name, Dateisystemflags, die maximale Länge eines Datei namens usw. Vor dem Zugriff auf Dateien und Verzeichnisse auf einem bestimmten Volume sollten Sie die Funktionen des Dateisystems mithilfe der [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) -Funktion ermitteln. Diese Funktion gibt Werte zurück, die Sie verwenden können, um die Anwendung so anzupassen, dass Sie mit dem Dateisystem effektiv funktioniert.

Im Allgemeinen sollten Sie keine statischen Puffer für Dateinamen und Pfade verwenden. Verwenden Sie stattdessen die von [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) zurückgegebenen Werte, um Puffer nach Bedarf zuzuordnen. Wenn Sie statische Puffer verwenden müssen, reservieren Sie 256 Zeichen für Dateinamen und 260 Zeichen für Pfade.

Die Funktionen " [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) " und " [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) " rufen die Pfade zum System Verzeichnis bzw. zum Windows-Verzeichnis ab.

Die Funktion [**GetDiskFreeSpace**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea) ruft Organisations Informationen zu einem Volume ab, einschließlich der Anzahl der Bytes pro Sektor, der Anzahl der Sektoren pro Cluster, der Anzahl der freien Cluster und der Gesamtzahl der Cluster. Allerdings kann **GetDiskFreeSpace** keine Volumegrößen von mehr als 2 GB melden. Verwenden Sie die [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) -Funktion, um sicherzustellen, dass Ihre Anwendung mit großen Kapazitäts Laufwerken funktioniert.

Die [**GetDriveType**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea) -Funktion gibt an, ob das Volume, auf das der angegebene Laufwerk Buchstabe verweist, ein Wechsel-, festes, CD-ROM-, RAM-oder Netzwerklaufwerk ist.

Die Funktion [**GetLogicalDrives**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrives) identifiziert die vorhandenen Volumes. Die [**getlogicaldrivestrings**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrivestringsw) -Funktion Ruft für jedes vorhandene Volume eine NULL-terminierte Zeichenfolge ab. Verwenden Sie diese Zeichen folgen, wenn ein Stammverzeichnis erforderlich ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datei System Erkennung](file-system-recognition.md)
</dt> </dl>

 

 
