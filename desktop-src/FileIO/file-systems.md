---
description: Verwalten Von Verzeichnissen mit Verzeichniseintragstabelle, Verzeichnishandles und Replikationspunkten.
title: Lokale Dateisysteme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77aa77c1029ce4dc19529b148dde1798084acf91afcf6e4435adf8fb2ab266f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696230"
---
# <a name="local-file-systems"></a>Lokale Dateisysteme

Mit einem *Dateisystem* können Anwendungen Dateien auf Speichergeräten speichern und abrufen. Dateien werden in einer hierarchischen Struktur platziert. Das Dateisystem gibt Benennungskonventionen für Dateien und das Format für die Angabe des Pfads zu einer Datei in der Struktur an.

Jedes Dateisystem besteht aus einem oder mehreren Treibern und Dynamic Link-Bibliotheken, die die Datenformate und Features des Dateisystems definieren. Dateisysteme können auf vielen verschiedenen Arten von Speichergeräten vorhanden sein, einschließlich Festplatten, Jukeboxes, wechselbaren optischen Datenträgern, Band-Sicherungseinheiten und Grafikkarten.

Alle von Windows unterstützten Dateisysteme verfügen über die folgenden Speicherkomponenten:

-   Volumes: Ein *Volume* ist eine Sammlung von Verzeichnissen und Dateien.
-   Verzeichnisse: Ein *Verzeichnis* ist eine hierarchische Sammlung von Verzeichnissen und Dateien.
-   Dateien. Eine *Datei* ist eine logische Gruppierung verwandter Daten.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                | Beschreibung                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Verzeichnisverwaltung](directory-management.md)<br/>          | Ein *Verzeichnis* ist eine hierarchische Sammlung von Verzeichnissen und Dateien. Die einzige Einschränkung für die Anzahl der Dateien, die in einem einzelnen Verzeichnis enthalten sein können, ist die physische Größe des Datenträgers, auf dem sich das Verzeichnis befindet.<br/> |
| [Datenträgerverwaltung](disk-management.md)<br/>                    | Eine *Festplatte* ist eine feste Festplatte auf einem Computer, die relativ schnellen Zugriff auf große Datenmengen bietet. Dies ist der Speichertyp, der am häufigsten mit Windows verwendet wird. Das System unterstützt auch Wechselmedien.<br/>    |
| [Dateiverwaltung](file-management.md)<br/>                    | Ein *Dateiobjekt* stellt eine Darstellung einer Ressource (entweder ein physisches Gerät oder eine Ressource auf einem physischen Gerät) bereit, die vom E/A-System verwaltet werden kann.<br/>                                                            |
| [Transaktionales NTFS (TxF)](transactional-ntfs-portal.md)<br/> | Transaktionales NTFS (TxF) ermöglicht das Durchführen von Dateivorgängen auf einem NTFS-Dateisystemvolume in einer Transaktion.<br/>                                                                                                                 |
| [Volumeverwaltung](volume-management.md)<br/>                | Die höchste Organisationsebene im Dateisystem ist das *Volume*. Ein Dateisystem befindet sich auf einem Volume.<br/>                                                                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[FAT Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc758586(v=ws.10))
</dt> <dt>

[Dateisystemtechnologien](/previous-versions/windows/it-pro/windows-server-2003/cc778296(v=ws.10))
</dt> <dt>

[Technische Referenz zu NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))
</dt> </dl>

 

