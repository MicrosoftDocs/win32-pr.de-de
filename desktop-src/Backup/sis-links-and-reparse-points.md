---
title: SIS-Links und -Wiederholungspunkte
description: SIS ist ein NTFS-Filtertreiber, der doppelte Dateien durch Copy-on-Write-Links (als SIS-Links bezeichnet) ersetzt, die auf eine einzelne Sicherungsdatei verweisen, wodurch der Datenträger- und Cacheaufwand dieser Dateien reduziert wird.
ms.assetid: 1600a9ff-413c-4059-b04c-c862f6cf8f32
keywords:
- Sicherung von Sicherungspunkten
- Sis-Sicherung (Single Instance Store), SIS-Links
- Single Instance Store (SIS)-Sicherung, Wiederholungspunkte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f89901df6ce1fea1635d4250f2884ec9baf68fb1552766564909486c8ed00a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588860"
---
# <a name="sis-links-and-reparse-points"></a>SIS-Links und -Wiederholungspunkte

SIS ist ein NTFS-Filtertreiber, der doppelte Dateien durch Copy-on-Write-Links (als SIS-Links bezeichnet) ersetzt, die auf eine einzelne Sicherungsdatei verweisen, wodurch der Datenträger- und Cacheaufwand dieser Dateien reduziert wird. Diese Sicherungsdatei ist in einem [allgemeinen Speicher](the-sis-common-store-and-common-store-files.md)enthalten. Bei der Implementierung der SIS-Architektur werden Dies sind [die Rearse-Punkte,](/windows/desktop/FileIO/reparse-points) die Informationen zu den SIS-Links enthalten.

SIS-Links werden als Sparsedateien implementiert, in der Regel mit den meisten Bereichen der Datei, die nicht zugeordnet sind, und einem Wiederholungspunkt. Die Struktur und der Inhalt eines Wiederholungspunkts sind für Ihre Sicherungs- und Wiederherstellungsanwendungen nicht transparent. Ihre Anwendungen senden und rufen die Daten in diesen Auswertungspunkten jedoch an und von SIS-API-Funktionen ab, die die darin enthaltenen Informationen verarbeiten. Die Informationen in einem Auswertungspunkt beziehen sich auf eine einzelne Sicherungsdatei, die die tatsächlichen Dateidaten enthält. Diese Sicherungsdatei wird als [Common Store-Datei](the-sis-common-store-and-common-store-files.md)bezeichnet und ist im gemeinsamen Speicher vorhanden.

Beim Wiederherstellen eines SIS-Links sollte Ihre Wiederherstellungsanwendung die folgenden Schritte ausführen:

1.  Bestimmen Sie die Common Store-Dateien, auf die bzw. die die SIS-Verbindung verweist.
2.  Wenn die Datei oder die Dateien nicht im allgemeinen Speicher vorhanden sind, stellen Sie die Datei bzw. die Dateien zusammen mit dem SIS-Link wieder her.
3.  Wenn der SIS-Link auf eine datei oder dateien verweist, die im allgemeinen Speicher auf dem Datenträger vorhanden sind, stellen Sie nur die SIS-Verknüpfung wieder her. Denken Sie daran, dass sich die Daten in Common Store-Dateien nie ändern. Wenn sich also eine bestimmte Common Store-Datei zum Zeitpunkt der Wiederherstellung noch auf dem Datenträger befindet, hat sie den gleichen Inhalt wie bei der Sicherung, und es ist nicht erforderlich, sie zu überschreiben.

Der einzige zusätzliche Mehraufwand für SIS-gestützte Sicherungen besteht darin, dass Ihre Sicherungsanwendung den SIS-Link und die den Sicherungsdateien zugeordneten Daten sichern muss. Alle SIS-Sicherungs- und -Wiederherstellungsvorgänge sind lokal auf einem bestimmten Volume.

 

 