---
description: Verzeichnisse mit Verzeichniseintrags Tabelle, Verzeichnis Handles, Analyse Punkten verwalten.
title: Lokale Dateisysteme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f624ef1999b81adb63ba1d5b7e349259cabd53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755160"
---
# <a name="local-file-systems"></a>Lokale Dateisysteme

Ein *Dateisystem* ermöglicht Anwendungen das Speichern und Abrufen von Dateien auf Speichergeräten. Dateien werden in einer hierarchischen Struktur abgelegt. Das Dateisystem gibt Benennungs Konventionen für Dateien und das Format zum Angeben des Pfads zu einer Datei in der Baumstruktur an.

Jedes Dateisystem besteht aus einem oder mehreren Treibern und Dynamic-Link-Bibliotheken, die die Datenformate und Features des Dateisystems definieren. Dateisysteme können auf vielen unterschiedlichen Arten von Speichergeräten vorhanden sein, z. b. Festplatten, Jukeboxes, wechselbare optische Datenträger, Band Sicherungs Einheiten und Speicherkarten.

Alle von Windows unterstützten Dateisysteme verfügen über die folgenden Speicherkomponenten:

-   Volumes: Ein *Volume* ist eine Sammlung von Verzeichnissen und Dateien.
-   Verzeichnisse: Ein *Verzeichnis* ist eine hierarchische Sammlung von Verzeichnissen und Dateien.
-   Dateien. Eine *Datei* ist eine logische Gruppierung verwandter Daten.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                | BESCHREIBUNG                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Verzeichnisverwaltung](directory-management.md)<br/>          | Ein *Verzeichnis* ist eine hierarchische Sammlung von Verzeichnissen und Dateien. Die einzige Einschränkung der Anzahl von Dateien, die in einem einzelnen Verzeichnis enthalten sein kann, ist die physische Größe des Datenträgers, auf dem sich das Verzeichnis befindet.<br/> |
| [Datenträgerverwaltung](disk-management.md)<br/>                    | Eine *Festplatte* ist ein Festplatten Datenträger innerhalb eines Computers, der einen relativ schnellen Zugriff auf große Datenmengen speichert und ermöglicht. Dabei handelt es sich um den Typ des Speichers, der am häufigsten mit Windows verwendet wird. Das System unterstützt auch Wechsel Datenträger.<br/>    |
| [Dateiverwaltung](file-management.md)<br/>                    | Ein *Datei Objekt* bietet eine Darstellung einer Ressource (entweder ein physisches Gerät oder eine Ressource auf einem physischen Gerät), die vom e/a-System verwaltet werden kann.<br/>                                                            |
| [Transaktionale NTFS (TxF)](transactional-ntfs-portal.md)<br/> | Transaktionale NTFS (TxF) ermöglicht die Ausführung von Datei Vorgängen auf einem NTFS-Dateisystem Volume in einer Transaktion.<br/>                                                                                                                 |
| [Volumeverwaltung](volume-management.md)<br/>                | Die höchste Organisationsebene im Dateisystem ist das *Volume*. Ein Dateisystem befindet sich auf einem Volume.<br/>                                                                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Technische Referenz zu FAT](/previous-versions/windows/it-pro/windows-server-2003/cc758586(v=ws.10))
</dt> <dt>

[Technologien für Dateisysteme](/previous-versions/windows/it-pro/windows-server-2003/cc778296(v=ws.10))
</dt> <dt>

[Technische Referenz zu NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))
</dt> </dl>

 

