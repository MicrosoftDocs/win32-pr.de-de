---
description: Nachdem Sie ein HTML-Quelldokument für die Ereignis Referenzseite (ERP) erstellt haben, müssen Sie es benennen, bevor Netzwerkmonitor es in der Ereignisanzeige anzeigen kann.
ms.assetid: 0c668a8b-94a5-4996-8214-4629a24a8337
title: Benennen einer Ereignis Referenzseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9c82b153ce2c7086af3883bcf3c4b34a0e68a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355477"
---
# <a name="naming-an-event-reference-page"></a>Benennen einer Ereignis Referenzseite

Nachdem Sie ein HTML-Quelldokument für die Ereignis Referenzseite (ERP) erstellt haben, müssen Sie es benennen, bevor Netzwerkmonitor es in der Ereignisanzeige anzeigen kann.

Namens Monitor-und expertenerp-Dateien mit dem folgenden Format:

``` syntax
<ExpertName><EventIdent>.htm (or <MonitorName><EventIdent>.htm)
```

<dl> <dt>

<span id="ExpertName"></span><span id="expertname"></span><span id="EXPERTNAME"></span>**Profilname**
</dt> <dd>

Der dll-Dateiname ohne die Dateinamenerweiterung.

</dd> <dt>

<span id="EventIdent"></span><span id="eventident"></span><span id="EVENTIDENT"></span>**Eventident**
</dt> <dd>

Ereignis Bezeichner des expertenerp.

Der Ereignis Bezeichner befindet sich auch im **eventident** -Member der **nmeventdata** -Struktur.

</dd> </dl>

Weitere Informationen zum Erstellen von ERP finden Sie in den folgenden Themen:

-   [Erstellen von Referenzseiten für Experten und Überwachungs Ereignisse](creating-expert-and-monitor-event-reference-pages.md)
-   [Schreiben einer Ereignis Referenzseite](writing-an-event-reference-page.md)
-   [Testen einer Ereignis Referenzseite](testing-an-event-reference-page.md)

 

 



