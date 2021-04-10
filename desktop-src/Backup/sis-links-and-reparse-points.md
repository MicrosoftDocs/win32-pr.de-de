---
title: SIS-Links und Analyse Punkte
description: SIS ist ein NTFS-Filtertreiber, der doppelte Dateien durch Copy-on-Write-Links (als SIS-Links bezeichnet) ersetzt, die auf eine einzelne Sicherungsdatei zeigen, wodurch der Datenträger-und Cache Aufwand dieser Dateien reduziert wird.
ms.assetid: 1600a9ff-413c-4059-b04c-c862f6cf8f32
keywords:
- Sicherung von Analyse Punkten
- SIS-Sicherung (Single Instance Store), SIS-Links
- SIS-Sicherung (Single Instance Store), Analyse Punkte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4987e7c64a83e7d0b02ed91899a182616be7943
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102102"
---
# <a name="sis-links-and-reparse-points"></a>SIS-Links und Analyse Punkte

SIS ist ein NTFS-Filtertreiber, der doppelte Dateien durch Copy-on-Write-Links (als SIS-Links bezeichnet) ersetzt, die auf eine einzelne Sicherungsdatei zeigen, wodurch der Datenträger-und Cache Aufwand dieser Dateien reduziert wird. Diese Sicherungsdatei ist in einem [gemeinsamen Speicher](the-sis-common-store-and-common-store-files.md)enthalten. Die Implementierung der SIS-Architektur nutzt Analyse [Punkte](/windows/desktop/FileIO/reparse-points) , die Informationen zu den SIS-Links enthalten.

SIS-Links werden als sparsesdateien implementiert, in der Regel mit den meisten Bereichen der Datei, deren Zuordnung aufgehoben wurde, und einem Analyse Punkt. Die Struktur und der Inhalt eines Analyse Punkts sind für Ihre Sicherungs-und Wiederherstellungs Anwendungen nicht transparent. Ihre Anwendungen senden und rufen jedoch die Daten innerhalb dieser Analyse Punkte an und von SIS-API-Funktionen ab, die die darin enthaltenen Informationen verarbeiten. Die Informationen in einem Analyse Punkt beziehen sich auf eine einzelne Sicherungsdatei, die die eigentlichen Datei Daten enthält. Diese Sicherungsdatei wird als " [Common-Store"-Datei](the-sis-common-store-and-common-store-files.md)bezeichnet und ist im gemeinsamen Speicher vorhanden.

Wenn Sie einen SIS-Link wiederherstellen, sollte die Wiederherstellungs Anwendung die folgenden Schritte ausführen:

1.  Bestimmen Sie die allgemeinen Speicherdateien, auf die der SIS-Link verweist.
2.  Wenn die Datei oder die Dateien nicht im allgemeinen Speicher vorhanden sind, stellen Sie die Datei oder die Dateien zusammen mit dem SIS-Link wieder her.
3.  Wenn der SIS-Link auf eine auf dem Datenträger vorhandene Datei im allgemeinen Speicher oder auf Dateien verweist, stellen Sie nur den SIS-Link wieder her. Beachten Sie, dass sich die Daten in den Dateien des Common Stores nie ändern. wenn sich also eine gegebene Common Store-Datei zum Zeitpunkt der Wiederherstellung noch auf dem Datenträger befindet, hat Sie denselben Inhalt wie bei der Sicherung, und es ist nicht erforderlich, Sie zu überschreiben.

Der einzige zusätzliche Aufwand, der für die SIS-gestützten Sicherungen erforderlich ist, besteht darin, dass die Sicherungs Anwendung den SIS-Link und die Daten sichern muss, die den Unterstützungs Dateien zugeordnet sind. Alle SIS-Sicherungs-und-Wiederherstellungs Vorgänge sind für ein bestimmtes Volume lokal.

 

 