---
description: Nachdem Sie ein ERP-Quell-HTML-Dokument (Event Reference Page) erstellt haben, müssen Sie es benennen, bevor Netzwerkmonitor in der Datei anzeigen Ereignisanzeige.
ms.assetid: 0c668a8b-94a5-4996-8214-4629a24a8337
title: Benennen einer Ereignisreferenzseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 569991c5e5ac24e18476fe27727f4fad1c310c8fd4e9439062fdf91bfb344005
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799690"
---
# <a name="naming-an-event-reference-page"></a>Benennen einer Ereignisreferenzseite

Nachdem Sie ein ERP-Quell-HTML-Dokument (Event Reference Page) erstellt haben, müssen Sie es benennen, bevor Netzwerkmonitor in der Datei anzeigen Ereignisanzeige.

Benennen Sie Monitor- und ERP-Expertendateien in diesem Format:

``` syntax
<ExpertName><EventIdent>.htm (or <MonitorName><EventIdent>.htm)
```

<dl> <dt>

<span id="ExpertName"></span><span id="expertname"></span><span id="EXPERTNAME"></span>**ExpertName**
</dt> <dd>

DLL-Dateiname, mit Ausnahme der Dateinamenerweiterung.

</dd> <dt>

<span id="EventIdent"></span><span id="eventident"></span><span id="EVENTIDENT"></span>**EventIdent**
</dt> <dd>

Ereignisbezeichner des ERP-Experten.

Der Ereignisbezeichner befindet sich auch im **EventIdent-Element** der **NMEVENTDATA-Struktur.**

</dd> </dl>

Weitere Informationen zum Erstellen eines ERP-Systems finden Sie in den folgenden Themen:

-   [Erstellen von Referenzseiten für Experten und Monitor-Ereignisse](creating-expert-and-monitor-event-reference-pages.md)
-   [Schreiben einer Ereignisreferenzseite](writing-an-event-reference-page.md)
-   [Testen einer Ereignisreferenzseite](testing-an-event-reference-page.md)

 

 



