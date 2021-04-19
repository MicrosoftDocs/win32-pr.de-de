---
description: PDH definiert die folgenden Datentypen.
ms.assetid: 8a2e8683-502a-4893-8b4f-5e2cf464a933
title: Leistungsindikator Datentypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38f9800288494eb82f675265b6e0b801c783668d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349858"
---
# <a name="performance-counters-data-types"></a>Leistungsindikator Datentypen

## <a name="performance-data-helper-pdh-types"></a>PDH-Typen (Performance Data Helper)

Consumer, die die [PDH-Funktionen (Performance Data Helper)](using-the-pdh-functions-to-consume-counter-data.md) verwenden, verwenden die folgenden Typen:

| Datentyp | BESCHREIBUNG
|-----------|------------
| **PDH \_ hquery**   | Handle für eine Abfrage. Die [**pdhopenquery**](/windows/win32/api/pdh/nf-pdh-pdhopenqueryw) -Funktion gibt dieses Handle zurück. Schließen Sie das Handle mithilfe von " [**pdhclosequery**](/windows/win32/api/pdh/nf-pdh-pdhclosequery)".
| **PDH- \_ hcounter** | Handle für einen-Counter. Die [**pdhaddcounter**](/windows/win32/api/pdh/nf-pdh-pdhaddcounterw) -Funktion gibt dieses Handle zurück. Schließen Sie das Handle mithilfe von [**PdhRemoveCounter**](/windows/win32/api/pdh/nf-pdh-pdhremovecounter) , oder schließen Sie das Handle für die Abfrage, die den-Wert enthält. **PdhRemoveCounter** sollte nicht für einen-Wert aufgerufen werden, wenn die entsprechende Abfrage bereits geschlossen wurde. PDH behält die Verknüpfung zwischen Indikatoren und Abfragen bei und schließt Zähler Handles automatisch, wenn das entsprechende Abfrage Handle geschlossen wird.
| **PDH- \_ hlog**     | Handle für eine Protokolldatei. Die Funktionen [**pdhopslog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) und [**pdhbindinputdatasource**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea) geben dieses Handle zurück. Schließen Sie das Handle mithilfe von [**pdhcloselog**](/windows/win32/api/pdh/nf-pdh-pdhcloselog).
| **PDH- \_ Status**   | PDH-Statuswert. Alle PDH-Funktionen geben einen Wert vom Typ **PDH- \_ Status** zurück. Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich. Andernfalls gibt die Funktion einen [Systemfehler Code](/windows/desktop/Debug/system-error-codes) oder einen [PDH-Fehlercode](pdh-error-codes.md)zurück.
