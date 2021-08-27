---
description: Dateiobjekte funktionieren als logische Schnittstelle zwischen Kernel- und Benutzermodusprozessen und den Dateidaten, die sich auf dem physischen Datenträger befinden.
ms.assetid: 53aabb35-4601-42d1-ac73-385473ff91e2
title: Dateiobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263eae282f76195cc125848f13f43f5ee3d8f676cc6328b2d03db443e6f1deec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107470"
---
# <a name="file-objects"></a>Dateiobjekte

*Dateiobjekte* funktionieren als logische Schnittstelle zwischen Kernel- und Benutzermodusprozessen und den Dateidaten, die sich auf dem physischen Datenträger befinden. Ein Dateiobjekt enthält sowohl die in die Datei geschriebenen Daten als auch den folgenden Satz von vom Kernel verwalteten Attributen.



| Informationstyp                                              | Zweck                                                                                                                                                                                         |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dateiname                                                     | Benennt die entsprechende physische Datei.                                                                                                                                                          |
| Aktueller Byteoffset                                           | Wird in synchronen Datei-E/A-Vorgängen (weiter unten in diesem Abschnitt beschrieben) verwendet, um den aktuellen Startspeicherort von Lese- und Schreibvorgängen zu identifizieren.                                                          |
| Freigabemodus                                                    | Gibt an, ob ein zweiter Prozess eine Datei für den Lese-, Schreib- oder Löschzugriff öffnen kann, während der erste Prozess noch darauf zutritt.                                                           |
| E/A-Modus                                                      | Gibt an, ob der erste Prozess die Datei für synchrone oder asynchrone [E/A,](synchronous-and-asynchronous-i-o.md)zwischengespeicherte oder nicht zwischengespeicherte E/A, sequenzielle oder zufällige E/A-Vorgänge und so weiter geöffnet hat. |
| Zeiger auf Geräteobjekt                                      | Identifiziert das physische Gerät, auf dem sich die Dateidaten befinden.                                                                                                                                        |
| Zeiger auf den Volumeparameterblock oder [ **VPB**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_vpb) | Identifiziert das Volume oder die Partition, auf dem bzw. der sich die Dateidaten befinden.                                                                                                                                    |
| Zeiger auf Abschnittsobjektzeiger                            | Identifiziert eine Stammstruktur, die eine [zugeordnete Datei beschreibt.](/windows/desktop/Memory/file-mapping)                                                                                                                  |
| Zeiger auf private Cachezuordnung                                  | Identifiziert die Dateidaten, die derzeit zwischengespeichert werden.                                                                                                                                              |



 

Diese Attribute werden als Teil der [**FILE \_ OBJECT-Struktur**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) in Ntddk.h definiert. Die Datenlängen und -typen der Werte finden Sie in der WDK-Dokumentation (Windows Driver Kit).

 

 
