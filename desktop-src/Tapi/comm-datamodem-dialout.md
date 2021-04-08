---
description: comm/DataModem/dialout
ms.assetid: b1cc19d2-4a9f-4d3f-a868-d5928654ad75
title: comm/DataModem/dialout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 553e998acdfe77509d62050b825dae6ea88d3b3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960235"
---
# <a name="commdatamodemdialout"></a>comm/DataModem/dialout

Die Geräteklasse " **comm/DataModem/dialout** " besteht aus datamoder-Geräten, die nur für ausgehende Aufrufe verwendet werden. Diese Klasse ersetzt die Klasse " [**comm/datamoder**](comm-datamodem.md) " unter Windows 2000 und neueren Betriebssystemen.

Vor Windows 2000 hat der Unimodem-TSP nur die Geräteklasse " [**comm/datamoder**](comm-datamodem.md) " unterstützt. Unerwartetes Verhalten kann auftreten, wenn eine Anwendung, die einen ausgehenden-aufrufsvorgang einwählt, den Konfigurationssatz von einem Dienst ändert, der auf einen eingehenden Anwendungen, die Windows 2000 und spätere Betriebssysteme verwenden, sollten entweder " [**comm/DataModem/Dialin**](comm-datamodem-dialin.md) " oder " **comm/DataModem/dialout** " in Aufrufen von [**lineconfigdialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) oder [**linesetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig)angeben. Dadurch kann Unimodem eine DFÜ-Konfiguration unabhängig von der DFÜ-Konfiguration beibehalten.

Obwohl " **comm/DataModem/dialout** " von Unimodem unter Windows 2000 und höher verwendet wird, kann es auch von anderen TSPS auf jeder beliebigen Plattform verwendet werden. Anwendungen, die auf allen Plattformen ausgeführt werden müssen, sollten zuerst " **comm/DataModem/dialout** " in Aufrufen der API verwenden, die eine Geräteklasse erfordern, und nur " [**comm/datamoder**](comm-datamodem.md) " verwenden, wenn die API " **lineerr \_ invalcallstate**" zurückgibt

Der Unimodem-Dienstanbieter übersetzt die Geräteklasse " [**comm/datamoder**](comm-datamodem.md) " in Aufrufen von " [**lineconfigdialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) " und " [**linesetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) " entweder in " [**comm/DataModem/Dialin**](comm-datamodem-dialin.md) " oder " **comm/DataModem/dialout** " wie folgt:

-   Windows 2000 und höher:
    -   Wenn im *lpszdebug* -Parameter im [**lineconfigdialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)-Befehl **null** angegeben ist, geht Unimodem von [**comm/DataModem/Dialin**](comm-datamodem-dialin.md)aus. Wenn " [**comm/datamoder**](comm-datamodem.md) " oder " [**TAPI/Line**](tapi-line.md) " im aufzurufenden **lineconfigdialog-Dialog** Feld angegeben wird, übersetzt Unimodem dieses in " **comm/DataModem/dialout**".
    -   Beim Aufrufen von [**linesetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) oder [**linegetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)wird " [**comm/datamoder**](comm-datamodem.md) " als " **comm/DataModem/dialout**" behandelt. **Null** gibt eine ungültige Geräteklasse an.
-   Vor Windows 2000:
    -   Wenn in [**lineconfigdialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)entweder **null** oder [**TAPI/Line**](tapi-line.md) angegeben ist, geht Unimodem von [**comm/datamoder**](comm-datamodem.md)aus.

Die Klasse " **comm/DataModem/dialout** " verwendet die Strukturen und Konfigurationen, die in der Geräteklasse " [**comm/datamoder**](comm-datamodem.md) " beschrieben werden.

 

 



