---
title: Die allgemeinen SIS-Speicher-und Common-Store Dateien
description: Alle Unterstützungs Dateien, die von einer SIS-Sicherung (Single Instance Store) verwaltet werden, werden als allgemeine Speicherdateien bezeichnet.
ms.assetid: c6231c30-9d5a-428d-a94d-9dc8db933432
keywords:
- Allgemeine Sicherung von Filialen
- SIS-Sicherung (Single Instance Store), allgemeine Speicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2f86b778b0a8db916fe580b8f833214523eb2e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858376"
---
# <a name="the-sis-common-store-and-common-store-files"></a>Die allgemeinen SIS-Speicher-und Common-Store Dateien

Alle Unterstützungs Dateien, die von einer SIS-Sicherung (Single Instance Store) verwaltet werden, werden als *Allgemeine Speicherdateien* bezeichnet. Auf jedem SIS-verwalteten Volume ist ein *gemeinsamer Speicher* vorhanden, der alle auf dem Volume vorhandenen Dateien im allgemeinen Speicher enthält. Dieses Verzeichnis befindet sich im Stammverzeichnis des Volumes und hat den Namen " \\ SIS Common Store". Der allgemeine Speicher ist als ein Verzeichnis implementiert, das vor normalem Benutzer Zugriff geschützt ist, da der Zugriff auf die Dateien des Common Stores nur direkt über die SIS-Sicherungs-API-Funktionen und nicht über Sicherungs-und Wiederherstellungs Anwendungen vorgesehen ist.

Die Eigenschaften einer Datei mit dem allgemeinen Speicher sind wie folgt:

-   Eine Common Store-Datei kann über einen oder mehrere Links verfügen, die darauf zeigen.
-   Nachdem er erstellt wurde, ändert sich der Inhalt einer Datei mit dem allgemeinen Speicher nie.
-   Die Namen der Dateien des Common Stores sind global eindeutig – das heißt, Sie sind auf allen Volumes auf der ganzen Welt eindeutig, und die Bindung zwischen einem Dateinamen und den Daten des Common Stores ist Global statisch.

Wenn SIS auf einem Volume aktiviert ist, wird eine Kopie der doppelten Dateien im allgemeinen Speicher erstellt, und alle doppelten Dateien werden durch [SIS-Links](sis-links-and-reparse-points.md) ersetzt, die auf die Datei mit dem allgemeinen Speicher verweisen. Weitere Informationen finden Sie unter [Aktivieren oder Deaktivieren von SIS auf einem Volume](/previous-versions/windows/it-pro/windows-server-storage-solutions/dd573313(v=ws.10)) in der TechNet-Dokumentation.

Wenn auf einen der SIS-Links für einen Schreibvorgang zugegriffen wird, stellt der SIS-Filter zuerst den ursprünglichen Inhalt der SIS-Verknüpfungs Datei aus der Datei mit dem allgemeinen Speicher wieder her. der Analyse Punkt, der die SIS-Verknüpfungs Datei mit dem allgemeinen Speicher verbindet, wird entfernt, und der Schreibvorgang wird dann für die ursprüngliche Zieldatei durchgeführt.

Die Datei mit dem allgemeinen Speicher wird nur entfernt, wenn der letzte auf Sie verweisende SIS-Link gelöscht wird.

 

 