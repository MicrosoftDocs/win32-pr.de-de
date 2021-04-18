---
description: Die TSPI-Spezifikation steht sehr eng im Zusammenhang mit den Spezifikationen für TAPI 2,2 (TAPI/C).
ms.assetid: 2c51f7e3-c741-4736-9611-2327d65b427e
title: Allgemeiner Vergleich mit TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce81d569d042cdd3eeb87088b1b7027858ca806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357789"
---
# <a name="overall-comparison-with-tapi"></a>Allgemeiner Vergleich mit TAPI

Die TSPI-Spezifikation steht sehr eng im Zusammenhang mit den Spezifikationen für TAPI 2,2 (TAPI/C). Die meisten Funktionen in einer besitzen eine entsprechende Funktion in der anderen. Die übliche Entsprechung lautet wie folgt:

-   TSPI-Funktionen haben dieselben Namen wie TAPI-Funktionen, mit dem Unterschied, dass Sie "**TSPI \_**" vorangesteht sind. Beispielsweise entspricht die TAPI-Funktion [**lineaccept**](/windows/win32/api/tapi/nf-tapi-lineaccept) der TSPI-Funktion [**TSPI \_ lineaccept**](/windows/win32/api/tspi/nf-tspi-tspi_lineaccept).
-   Prozeduren, die einen asynchronen Vorgang zulassen, fügen einen *dwrequestid-* Parameter des Typs [drv \_ RequestId](drv-requestid.md) als ersten Parameter ein. Dieser Parameter gibt den Wert an, der zurückgegeben werden soll, um den asynchronen Vorgang anzugeben und den asynchronen Abschluss zu melden.
-   *hcallparameter* des Typs "hcall" werden durch *hdcall-Parameter* des Typs " [hdrvcall"](hdrvline.md)ersetzt, der das Handle des Dienstanbieters für den-Rückruf angibt.
-   *hline* -Parameter vom Typ "hline" werden durch *hdline* -Parameter vom Typ " [hdrvline](hdrvline.md)" ersetzt, wodurch das Handle des Dienstanbieters für die Zeile angegeben wird.
-   *hphone* -Parameter vom Typ "hphone" werden durch *hdphone* -Parameter des Typs " [hdrvphone](hdrvphone.md)" ersetzt, der den Handle des Dienstanbieters für das Telefon angibt.
-   Prozeduren, die einen neuen-Anruf erstellen, wie [**z. b. TSPI \_ linemakecall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall), ersetzen einen einzelnen *lphcall-Parameter* durch zwei Parameter: einen " *htcall"* des Typs " [htapicall](htapicall.md) ", der den TAPI-Handle für den-Befehl übergibt, und einen *lphdcallof* "lphdrvcall", der den Speicherort angibt Eine ähnliche Aufteilung von Parametern tritt in [**TSPI \_ lineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) und [**TSPI \_ phoneopen**](/windows/win32/api/tspi/nf-tspi-tspi_phoneopen)auf.
-   Auf der TSPI-Ebene gibt es keine "Berechtigung" für Geräte Handles. Außerdem verfügt jede Anwendung, die über ein Gerät oder ein Telefon Handle verfügt, auf API-Ebene über ein anderes handle, aber TAPI führt diese in einem einzigen Handle auf der Dienstanbieter Seite zusammen. Folglich werden die Fehlercodes und Statusmeldungen im Zusammenhang mit den Berechtigungen und der Anzahl der Clients, die ein Gerät verwenden, nicht auf der TSPI-Ebene angezeigt.

Der Satz von TAPI-Funktionen ordnet 1 nicht auf dem Satz von TSPI-Funktionen zu. Insbesondere werden Funktionen im Zusammenhang mit Berechtigungen, Telefonnummern Übersetzung und Interanwendungskommunikation von TAPI verarbeitet und verfügen nicht über die entsprechende Funktion in TSPI. Andere Funktionen, wie z. b. solche, die für die Konfiguration und Initialisierung des Dienstanbieters verwendet werden, verfügen über keine entsprechenden Funktionen in TAPI.

 

 
