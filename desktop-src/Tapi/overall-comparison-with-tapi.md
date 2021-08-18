---
description: Die TSPI-Spezifikation ist eng mit den Spezifikationen für TAPI 2.2 (TAPI/C) verknüpft.
ms.assetid: 2c51f7e3-c741-4736-9611-2327d65b427e
title: Gesamtvergleich mit TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecedd5a53fd30e2a49b6d44e90d30f86ff8469f002166ca3328f3146a2748b78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002808"
---
# <a name="overall-comparison-with-tapi"></a>Gesamtvergleich mit TAPI

Die TSPI-Spezifikation ist eng mit den Spezifikationen für TAPI 2.2 (TAPI/C) verknüpft. Die meisten Funktionen in einer verfügen über eine entsprechende Funktion in der anderen. Die übliche Entsprechung lautet wie folgt:

-   TSPI-Funktionen haben die gleichen Namen wie TAPI-Funktionen, mit der Ausnahme, dass ihnen **"TSPI" voraus \_** ist. Beispielsweise entspricht die TAPI-Funktion [**lineAccept**](/windows/win32/api/tapi/nf-tapi-lineaccept) der TSPI-Funktion [**TSPI \_ lineAccept.**](/windows/win32/api/tspi/nf-tspi-tspi_lineaccept)
-   Prozeduren, die einen asynchronen Vorgang zulassen, fügen einen *dwRequestID-Parameter* vom Typ [DRV \_ REQUESTID](drv-requestid.md) als ersten Parameter ein. Dieser Parameter gibt den Wert an, der zurückgegeben werden soll, um einen asynchronen Vorgang anzugeben und asynchrone Vervollständigung zu melden.
-   *hCall-Parameter* des Typs HCALL werden durch *hdCall-Parameter* vom Typ [HDRVCALL](hdrvline.md)ersetzt, die das Handle des Dienstanbieters für den Aufruf angeben.
-   *hLine-Parameter* vom Typ HLINE werden durch *hdLine-Parameter* vom Typ [HDRVLINE](hdrvline.md)ersetzt, die das Handle des Dienstanbieters für die Zeile angeben.
-   *hPhone-Parameter* vom Typ HPHONE werden durch *hdPhone-Parameter* vom Typ [HDRVPHONE](hdrvphone.md)ersetzt, die das Handle des Dienstanbieters für das Telefon angeben.
-   Prozeduren, die einen neuen Aufruf erstellen, z. B. [**TSPI \_ lineMakeCall,**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)ersetzen einen einzelnen *lphCall-Parameter* durch zwei Parameter: *einen htCall* vom Typ [HTAPICALL-Parameter,](htapicall.md) der das TAPI-Handle für den Aufruf übergibt, und *einen lphdCall* vom Typ LPHDRVCALL, der den Speicherort angibt, an den der Dienstanbieter sein neues Handle für den Aufruf schreiben muss. Eine ähnliche Aufteilung der Parameter erfolgt in [**TSPI \_ lineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) und [**TSPI \_ phoneOpen**](/windows/win32/api/tspi/nf-tspi-tspi_phoneopen).
-   Auf TSPI-Ebene gibt es keine "Berechtigung", die Gerätehandles zugeordnet ist. Darüber hinaus hat auf API-Ebene jede Anwendung, die über ein Gerät oder ein Aufrufhand handle verfügt, ein anderes Handle, aber TAPI führt diese zu einem einzelnen Handle aufseiten des Dienstanbieters zusammen. Daher werden die Fehlercodes und Statusmeldungen im Zusammenhang mit Berechtigungen und der Anzahl von Clients, die ein Gerät verwenden, nicht auf TSPI-Ebene angezeigt.

Die TAPI-Funktionen ordnen dem Satz von TSPI-Funktionen nicht eins zu eins zu. Insbesondere Funktionen im Zusammenhang mit Berechtigungen, telefonnummernübersetzung und Interapplication Communication werden von TAPI verarbeitet und haben keine entsprechende Funktion in TSPI. Andere Funktionen, z. B. diejenigen, die für die Konfiguration und Initialisierung des Dienstanbieters verwendet werden, verfügen über keine entsprechenden Funktionen in TAPI.

 

 
