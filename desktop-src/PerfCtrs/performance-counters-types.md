---
description: PDH definiert die folgenden Datentypen.
ms.assetid: 8a2e8683-502a-4893-8b4f-5e2cf464a933
title: Datentypen von Leistungsindikatoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23208978cfc3c0a67c7547598f26e506a5571a54d0d5ddfc93b7ecff38f9c559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674740"
---
# <a name="performance-counters-data-types"></a>Datentypen von Leistungsindikatoren

## <a name="performance-data-helper-pdh-types"></a>Typen von Performance Data Helper (PDH)

Consumer, die die [PdH-Funktionen (Performance Data Helper)](using-the-pdh-functions-to-consume-counter-data.md) verwenden, verwenden die folgenden Typen:

| Datentyp | Beschreibung
|-----------|------------
| **PDH \_ HQUERY**   | Verarbeiten einer Abfrage. Die [**PdhOpenQuery-Funktion**](/windows/win32/api/pdh/nf-pdh-pdhopenqueryw) gibt dieses Handle zurück. Schließen Sie das Handle mit [**pdhCloseQuery.**](/windows/win32/api/pdh/nf-pdh-pdhclosequery)
| **PDH \_ HCOUNTER** | Handle für einen Zähler. Die [**PdhAddCounter-Funktion**](/windows/win32/api/pdh/nf-pdh-pdhaddcounterw) gibt dieses Handle zurück. Schließen Sie das Handle mithilfe von [**PdhRemoveCounter,**](/windows/win32/api/pdh/nf-pdh-pdhremovecounter) oder schließen Sie das Handle für die Abfrage, die den Zähler enthält. Rufen Sie **PdhRemoveCounter** nicht für einen Leistungsindikator auf, wenn die entsprechende Abfrage bereits geschlossen wurde. PDH verwaltet die Verknüpfung zwischen Leistungsindikatoren und Abfragen und schließt indikatorenhandles automatisch, wenn das entsprechende Abfragehandle geschlossen wird.
| **PDH \_ HLOG**     | Verarbeiten einer Protokolldatei. Die Funktionen [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) und [**PdhBindInputDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea) geben dieses Handle zurück. Schließen Sie das Handle mit [**pdhCloseLog.**](/windows/win32/api/pdh/nf-pdh-pdhcloselog)
| **\_PDH-STATUS**   | PDH-Statuswert. Alle PDH-Funktionen geben einen Wert vom Typ **PDH \_ STATUS** zurück. Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert ERROR \_ SUCCESS. Andernfalls gibt die Funktion einen [Systemfehlercode](/windows/desktop/Debug/system-error-codes) oder einen [PDH-Fehlercode](pdh-error-codes.md)zurück.
