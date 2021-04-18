---
description: Wenn es sich bei der Datenquelle um eine Protokolldatei handelt, können Sie einen Zeitbereich für die Abfrage angeben.
ms.assetid: 8d9c3e96-3645-4875-9b5f-a6c9ddf23ec3
title: Festlegen eines Zeit Bereichs für eine Abfrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55baf642a4a12a86476e2d6feada6b79f1fda72c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357753"
---
# <a name="setting-a-time-range-for-a-query"></a>Festlegen eines Zeit Bereichs für eine Abfrage

Wenn es sich bei der Datenquelle um eine Protokolldatei handelt, können Sie einen Zeitbereich für die Abfrage angeben. Die Abfrage ruft Leistungsdaten aus der Protokolldatei ab, die während des angegebenen Zeitraums erfasst wurde. Um den Zeitbereich festzulegen, müssen Sie die [**pdhsetquerytimerange**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange) -Funktion aufrufen. **Pdhsetquerytimerange** wird nicht verwendet, um Leistungsdaten aus Echtzeitdaten Quellen abzufragen.

Führen Sie die folgenden Schritte aus, um einen Zeitwert zu erstellen.

1.  Weisen Sie eine [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur zu, und initialisieren Sie die Felder mit dem gewünschten Uhrzeitwert.
2.  Ruft [**systemtimeyfiletime**](/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) auf, um den Zeitwert der [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur in eine [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) -Struktur Zeit zu konvertieren.
3.  Wandeln Sie die [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) -Struktur als Longlong-Variable um, wobei Sie die Auffüll Konventionen für Strukturelemente ihrer Plattform und Ihres Compilers berücksichtigen.
4.  Kopieren Sie den Longlong-Wert in das entsprechende Feld in der [**PDH- \_ Zeit \_ Info**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info) -Struktur.

Rufen Sie die [**pdhgetdatasourcetimerange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) -Funktion auf, um den Zeitbereich aller in einer Protokolldatei enthaltenen Leistungsdaten abzurufen.

 

 
