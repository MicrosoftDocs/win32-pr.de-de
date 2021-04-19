---
description: Datei Objekte fungieren als logische Schnittstelle zwischen Kernel-und Benutzermodusprozesse und den Datei Daten, die sich auf dem physischen Datenträger befinden.
ms.assetid: 53aabb35-4601-42d1-ac73-385473ff91e2
title: Datei Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e37793ad6c31ac86809047a3ec0d34afc3efc34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350576"
---
# <a name="file-objects"></a>Datei Objekte

*Datei Objekte* fungieren als logische Schnittstelle zwischen Kernel-und Benutzermodusprozesse und den Datei Daten, die sich auf dem physischen Datenträger befinden. Ein Datei Objekt enthält sowohl die Daten, die in die Datei geschrieben wurden, als auch die folgenden Kernel verwalteten Attribute.



| Informationstyp                                              | Zweck                                                                                                                                                                                         |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dateiname                                                     | Benennt die entsprechende physische Datei.                                                                                                                                                          |
| Aktueller Byte Offset                                           | Wird in synchronen Datei-e/a verwendet (weiter unten in diesem Abschnitt beschrieben), um den aktuellen Start Speicherort von Lese-und Schreibvorgängen zu identifizieren.                                                          |
| Freigabe Modus                                                    | Gibt an, ob ein zweiter Prozess eine Datei für Lese-, Schreib-oder Lösch Zugriffe öffnen kann, während der anfängliche Prozess noch auf die Datei zugreift.                                                           |
| E/a-Modus                                                      | Gibt an, ob der anfängliche Prozess die Datei für [synchrone oder asynchrone](synchronous-and-asynchronous-i-o.md)e/a-Vorgänge, zwischengespeicherte oder nicht zwischengespeicherte e/a, sequenzielle oder zufällige e/a-Vorgänge und so weiter geöffnet hat. |
| Zeiger auf Geräte Objekt                                      | Identifiziert das physische Gerät, auf dem sich die Datei Daten befindet.                                                                                                                                        |
| Zeiger auf den Volumeparameterblock oder [ **vpb**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_vpb) | Identifiziert das Volume oder die Partition, auf dem sich die Datei Daten befindet.                                                                                                                                    |
| Zeiger auf Abschnitts Objekt Zeiger                            | Identifiziert eine Stamm Struktur, die eine zugeordnete [Datei](/windows/desktop/Memory/file-mapping)beschreibt.                                                                                                                  |
| Zeiger auf private Cache Zuordnung                                  | Identifiziert die derzeit zwischengespeicherten Datei Daten.                                                                                                                                              |



 

Diese Attribute werden als Teil der [**Datei \_ Objekt**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) Struktur in ntddk. h definiert. Informationen zu den Daten Längen und-Typen der Werte finden Sie in der Dokumentation zum Windows-Treiberkit (WDK).

 

 
