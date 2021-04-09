---
description: comm/DataModem/Dialin
ms.assetid: 7330db08-5064-47c9-9d28-c5b2b15c3ac6
title: comm/DataModem/Dialin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cb66d72b5d9f2c75af361153d46f5cac9abdfd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960236"
---
# <a name="commdatamodemdialin"></a>comm/DataModem/Dialin

Die " **comm/DataModem/Dialin"-** Geräteklasse besteht aus datamoder-Geräten, die nur für eingehende Aufrufe verwendet werden. Diese Klasse ersetzt die Klasse " [**comm/datamoder**](comm-datamodem.md) " unter Windows 2000 und neueren Betriebssystemen.

Vor Windows 2000 hat der Unimodem-TSP nur die Geräteklasse " [**comm/datamoder**](comm-datamodem.md) " unterstützt. Unerwartetes Verhalten kann auftreten, wenn eine Anwendung, die einen ausgehenden-aufrufsvorgang einwählt, den Konfigurationssatz von einem Dienst ändert, der auf einen eingehenden Anwendungen, die Windows 2000 und spätere Betriebssysteme verwenden, sollten entweder " **comm/DataModem/Dialin** " oder " [**comm/DataModem/dialout**](comm-datamodem-dialout.md) " in Aufrufen von [**lineconfigdialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) oder [**linesetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig)angeben. Dadurch kann Unimodem eine DFÜ-Konfiguration unabhängig von der DFÜ-Konfiguration beibehalten.

Obwohl " **comm/DataModem/Dialin** " von Unimodem unter Windows 2000 und höher verwendet wird, kann es auch von anderen TSPS auf jeder beliebigen Plattform verwendet werden. Anwendungen, die auf allen Plattformen ausgeführt werden müssen, sollten in Aufrufen von APIs, die eine Geräteklasse erfordern, zuerst " **comm/DataModem/Dialin** " verwenden und " [**comm/datamoder**](comm-datamodem.md) " nur verwenden, wenn die API " **lineerr \_ invalcallstate**" zurückgibt

Der Unimodem-Dienstanbieter übersetzt die Geräteklasse " [**comm/datamoder**](comm-datamodem.md) " in Aufrufen von " [**lineconfigdialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog) " und " [**linesetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) " entweder in " **comm/DataModem/Dialin** " oder " [**comm/DataModem/dialout**](comm-datamodem-dialout.md) " wie folgt:

-   Windows 2000 und höher:
    -   Wenn im *lpszdebug* -Parameter im [**lineconfigdialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)-Befehl **null** angegeben ist, geht Unimodem von **comm/DataModem/Dialin** aus. Wenn " [**comm/datamoder**](comm-datamodem.md) " oder " [**TAPI/Line**](tapi-line.md) " im aufzurufenden **lineconfigdialog-Dialog** Feld angegeben wird, übersetzt Unimodem dieses in " [**comm/DataModem/dialout**](comm-datamodem-dialout.md)".
    -   Beim Aufrufen von [**linesetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) oder [**linegetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)wird " [**comm/datamoder**](comm-datamodem.md) " als " [**comm/DataModem/dialout**](comm-datamodem-dialout.md)" behandelt. **Null** gibt eine ungültige Geräteklasse an.
-   Vor Windows 2000:
    -   Wenn in [**lineconfigdialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)entweder **null** oder [**TAPI/Line**](tapi-line.md) angegeben ist, geht Unimodem von [**comm/datamoder**](comm-datamodem.md)aus.

Die Klasse " **comm/DataModem/Dialin** " verwendet die Strukturen und Konfigurationen, die in der Geräteklasse " [**comm/datamoder**](comm-datamodem.md) " beschrieben werden.

 

 



