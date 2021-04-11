---
description: Eine Datei ist eine Einheit von Daten im Dateisystem, auf die ein Benutzer zugreifen und Sie verwalten kann.
ms.assetid: 271bad79-c23b-45ee-938c-d17dae89db1a
title: Dateien und Cluster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75384900d5d487ab02bd19c13cc2c25e9a310b3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215378"
---
# <a name="files-and-clusters"></a>Dateien und Cluster

Eine *Datei* ist eine Einheit von Daten im Dateisystem, auf die ein Benutzer zugreifen und Sie verwalten kann. Eine Datei muss in Ihrem Verzeichnis einen eindeutigen Namen aufweisen. Sie besteht aus einem oder mehreren Streams von Bytes, die eine Gruppe verwandter Daten enthalten, sowie aus einer Reihe von Attributen (auch als Eigenschaften bezeichnet), die die Datei oder die Daten in der Datei beschreiben. Der Erstellungs Zeitpunkt einer Datei ist ein Beispiel für ein Datei Attribut.

Wenn eine Datei erstellt wird, wird ein unbenannter Standarddaten Strom erstellt, um alle Daten zu speichern, die in die Datei geschrieben werden, während Sie geöffnet ist Sie können auch zusätzliche Datenströme innerhalb der Datei erstellen. Diese zusätzlichen Streams werden als Alternative Streams bezeichnet. In der folgenden Abbildung ist eine Datei mit dem Standardstream und zwei Alternativen Streams dargestellt.

![Datei mit einem Standardstream und zwei Alternativen Streams](images/fig1.png)

Dateiattribute werden nicht in den Datenströmen mit den Datei Daten gespeichert, sondern an einem anderen Speicherort gespeichert und vom Betriebssystem verwaltet.

Alle Dateisystem Daten, einschließlich des systembootstrap-Codes und der Verzeichnisse, werden vom NTFS-Dateisystem in Dateien gespeichert. Andere Dateisysteme speichern diese Informationen in Datenträger Regionen außerhalb des Dateisystems. Ein Vorteil der Speicherung dieser Informationen in Dateien besteht darin, dass Windows die Informationen problemlos suchen, darauf zugreifen und Sie verwalten kann. Andere Vorteile sind, dass jede dieser Dateien durch eine Sicherheits Beschreibung geschützt werden kann, und im Fall einer Beschädigung des Datenträgers können Sie schnell auf einen sichereren Teil des Datenträgers verlagert werden.

Die grundlegende Speichereinheit aller unterstützten Dateisysteme ist ein *Cluster*, bei dem es sich um eine Gruppe von Sektoren handelt. Dadurch kann das Dateisystem die Verwaltung von Datenträger Daten unabhängig von der vom Hardware Datenträger Controller festgelegten Datenträger Sektorgröße optimieren. Wenn der zu verwaltenden Datenträger groß ist und große Datenmengen in einem einzigen Vorgang verschoben und organisiert werden, kann der Administrator die Clustergröße anpassen, um dies zu ermöglichen.

Windows verwaltet Dateien mithilfe von [Datei Objekten](file-objects.md), [Datei Handles](file-handles.md)und [Datei Zeigern](file-pointers.md).

Weitere Informationen zu Dateistreams finden Sie unter [Dateistreams](file-streams.md). Weitere Informationen zu Clustern finden Sie unter [Cluster und Blöcke](clusters-and-extents.md). Weitere Informationen zum Zugreifen auf und Verwalten von Dateien finden Sie unter [Dateiverwaltung](file-management.md) und [Datei Verwaltungs Referenz](file-management-reference.md).

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Dateistreams](file-streams.md)<br/>                 | Im NTFS-Dateisystem enthalten Streams die Daten, die in eine Datei geschrieben werden, und die mehr Informationen über eine Datei als Attribute und Eigenschaften enthält.<br/>                                                                                         |
| [Datei Objekte](file-objects.md)<br/>                 | *Datei Objekte* fungieren als logische Schnittstelle zwischen Kernel-und Benutzermodusprozesse und den Datei Daten, die sich auf dem physischen Datenträger befinden.<br/>                                                                                                      |
| [Datei Handles](file-handles.md)<br/>                 | Wenn eine Datei von einem Prozess mithilfe der Funktion " [**deatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " geöffnet wird, wird ihr ein *Datei Handle* zugeordnet, bis der Prozess beendet oder das Handle mit der Funktion " [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) " geschlossen wird.<br/> |
| [Dateizeiger](file-pointers.md)<br/>               | Ein Dateizeiger ist ein 64-Bit-Offset Wert, der das nächste Byte angibt, das gelesen werden soll, oder der Speicherort, an dem das nächste geschriebene Byte empfangen werden soll.<br/>                                                                                                                 |
| [Cluster und Blöcke](clusters-and-extents.md)<br/> | Auf Cluster kann aus zwei unterschiedlichen Perspektiven verwiesen werden: innerhalb der Datei und auf dem Volume.<br/>                                                                                                                                                   |



 

 

