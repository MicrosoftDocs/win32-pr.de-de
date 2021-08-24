---
title: Allgemeine SIS-Store und Common-Store Dateien
description: Alle Sicherungsdateien, die von einer SIS-Sicherung (Single Instance Store) verwaltet werden, werden als Common Store-Dateien bezeichnet.
ms.assetid: c6231c30-9d5a-428d-a94d-9dc8db933432
keywords:
- Common Stores Backup
- Sis-Sicherung (Single Instance Store), allgemeine Speicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f19337a967fd858c149bc9d4261abc44214d4c76023abe022b5e1c5efd5f8ed3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529470"
---
# <a name="the-sis-common-store-and-common-store-files"></a>Allgemeine SIS-Store und Common-Store Dateien

Alle Sicherungsdateien, die von einer SIS-Sicherung (Single Instance Store) verwaltet werden, werden *als Common Store-Dateien bezeichnet.* Ein *gemeinsamer Speicher* ist auf jedem von SIS verwalteten Volume vorhanden und enthält alle Dateien mit gemeinsamem Speicher, die auf diesem Volume vorhanden sind. Dieses Verzeichnis befindet sich im Stammverzeichnis des Volumes und heißt \\ "SIS Common Store". Der allgemeine Speicher wird als Verzeichnis implementiert, das vor normalem Benutzerzugriff geschützt ist, da common-store-Dateien nur für den direkten Zugriff auf SIS-Sicherungs-API-Funktionen und nicht für das Sichern und Wiederherstellen von Anwendungen vorgesehen sind.

Die Eigenschaften einer Common Store-Datei sind die folgenden:

-   Eine Common Store-Datei kann einen oder mehrere Links enthalten, die darauf verweisen.
-   Nachdem sie erstellt wurde, ändert sich der Inhalt einer Common Store-Datei nie.
-   Die Namen von Common Store-Dateien sind global eindeutig, d.&a; sie sind auf allen Volumes auf allen Systemen der Welt eindeutig, und die Bindung zwischen einem Dateinamen im allgemeinen Speicher und seinen Daten ist global statisch.

Wenn SIS auf einem Volume aktiviert ist, wird eine Kopie der doppelten Dateien in den allgemeinen Speicher erstellt, und alle doppelten Dateien werden durch [SIS-Links](sis-links-and-reparse-points.md) ersetzt, die auf die Common Store-Datei verweisen. Weitere Informationen finden Sie unter [Aktivieren oder Deaktivieren von SIS auf einem Volume](/previous-versions/windows/it-pro/windows-server-storage-solutions/dd573313(v=ws.10)) in der TechNet-Dokumentation.

Wenn für einen Schreibvorgang auf einen der SIS-Links zugegriffen wird, stellt der SIS-Filter zunächst den ursprünglichen Inhalt der SIS-Linkdatei aus der Common Store-Datei wieder wieder auf, der Reparsepunkt, der die SIS-Linkdatei mit dem allgemeinen Speicher verknüpft, wird entfernt, und der Schreibvorgang wird dann für die ursprüngliche Zieldatei ausgeführt.

Die Common Store-Datei wird nur entfernt, wenn der letzte SIS-Link gelöscht wird, der daraufzeige.

 

 