---
description: Dieser Abschnitt enthält eine alphabetische Liste der verfügbaren Gerätefunktionen in der telefoniespi.
ms.assetid: 2a27fbb7-93b5-4106-afd3-e63456650fb9
title: TSPI-Line-Gerätefunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea2ca54096ac89b76a4658129362e87d4281fcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865687"
---
# <a name="tspi-line-device-functions"></a>TSPI-Line-Gerätefunktionen

Dieser Abschnitt enthält eine alphabetische Liste der verfügbaren Gerätefunktionen in der telefoniespi. Die Informationen zu den einzelnen Funktionen umfassen Folgendes:

-   Eine-Anweisung des Zwecks der Funktion.
-   Die korrekte Syntax für die Funktion.
-   Eine Beschreibung der Funktionsparameter, einschließlich gültiger anrufzustände.
-   Eine Beschreibung des Rückgabewerts der Funktion.
-   Ein Abschnitt "Hinweise", der eine beliebige oder alle der folgenden Optionen enthalten kann: eine Liste der gültigen aufrufzustände für den Eintrag der Funktion und typische Aufrufe von Zustands Übergängen, wenn die Anforderung abgeschlossen ist. eine Beschreibung der Elemente von großen Datenstrukturen, die vom Dienstanbieter ausgefüllt werden müssen und deren Werte intakt bleiben müssen. und im Vergleich mit einer entsprechenden Funktion in TAPI.
-   Verweise auf andere Funktionen, Nachrichten oder Datenstrukturen.
    > [!Note]  
    > Die tatsächlichen Zustände, in denen eine Funktion ausgeführt werden kann, können durch die Funktionen des Dienstanbieters eingeschränkt werden. Dienstanbieter müssen den **dwcallfeatures** -Member in der [**linecallstatus**](/windows/win32/api/tapi/ns-tapi-linecallstatus) -Struktur, den **dwaddressfeatures** -Member in der [**lineaddressstatus**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) -Struktur und den **dwlinefeatures** -Member in der [**linedevstatus**](/windows/win32/api/tapi/ns-tapi-linedevstatus) -Struktur festlegen, um Anwendungen anzugeben, ob eine Funktion zu diesem Zeitpunkt zulässig ist oder nicht.

     

Dieser Abschnitt enthält die folgenden TSPI-Gerätefunktionen:

-   [**TSPI- \_ lineaccept**](/windows/win32/api/tspi/nf-tspi-tspi_lineaccept)
-   [**TSPI \_ lineaddtconference**](/windows/win32/api/tspi/nf-tspi-tspi_lineaddtoconference)
-   [**TSPI- \_ lineanswer**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer)
-   [**TSPI \_ lineblintransfer**](/windows/win32/api/tspi/nf-tspi-tspi_lineblindtransfer)
-   [**TSPI- \_ lineclose**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose)
-   [**TSPI \_ lineclosecall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)
-   [**TSPI \_ lineclosemspinstance**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [**TSPI \_ linecompletecall**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletecall)
-   [**TSPI \_ linecompletetransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [**TSPI \_ lineconditionalmediadetection**](/windows/win32/api/tspi/nf-tspi-tspi_lineconditionalmediadetection)
-   [**TSPI \_ lineconfigdialog**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog)
-   [**TSPI \_ lineconfigdialogedit**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialogedit)
-   [**TSPI \_ linecreatemspinstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [**TSPI \_ linedevspecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
-   [**TSPI \_ linedevspecificfeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
-   [**TSPI- \_ linedial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial)
-   [**TSPI- \_ linedrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop)
-   [TSPI \_ linedropnoowner](tspi-linedropnoowner.md)
-   [TSPI \_ linedroponclose](tspi-linedroponclose.md)
-   [**TSPI ( \_ lineforward)**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [**TSPI- \_ linegather-Ziffern**](/windows/win32/api/tspi/nf-tspi-tspi_linegatherdigits)
-   [**TSPI \_ linegeneratedigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits)
-   [**TSPI \_ linegeneratetone**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratetone)
-   [**TSPI \_ linegetaddresscaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)
-   [**TSPI \_ linegetadressssid**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)
-   [**TSPI \_ linegetaddressstatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus)
-   [**TSPI \_ linegetcalladressssid**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid)
-   [**TSPI \_ linegetcallhubtracking**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallhubtracking)
-   [**TSPI \_ linegetkallids**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallids)
-   [**TSPI \_ linegetcallinfo**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)
-   [**TSPI \_ linegetcallstatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)
-   [**TSPI \_ linegetdevcaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)
-   [**TSPI \_ linegetdevconfig**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)
-   [**TSPI \_ linegetextensionid**](/windows/win32/api/tspi/nf-tspi-tspi_linegetextensionid)
-   [**TSPI- \_ linegeticon**](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)
-   [**TSPI- \_ lineGetID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)
-   [**TSPI \_ linegetlinedevstatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)
-   [**TSPI \_ linegetnumaddressids**](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids)
-   [**TSPI- \_ linehold**](/windows/win32/api/tspi/nf-tspi-tspi_linehold)
-   [**TSPI \_ linemakecall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [**TSPI \_ linemonitordigits**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitordigits)
-   [**TSPI \_ linemonitormedia**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitormedia)
-   [**TSPI- \_ linemonitortones**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitortones)
-   [**TSPI \_ linemspidentify**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [**TSPI \_ linenegotiateextversion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion)
-   [**TSPI \_ linenegotiatetspiversion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion)
-   [**TSPI ( \_ lineOpen)**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)
-   [**TSPI- \_ linepark**](/windows/win32/api/tspi/nf-tspi-tspi_linepark)
-   [**TSPI- \_ linepickup**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [**TSPI \_ lineprepareaddumconference**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [**TSPI \_ linereceivemspdata**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [**TSPI \_ lineredirect**](/windows/win32/api/tspi/nf-tspi-tspi_lineredirect)
-   [**TSPI \_ linereleaseuseruserinfo**](/windows/win32/api/tspi/nf-tspi-tspi_linereleaseuseruserinfo)
-   [**TSPI \_ lineremovefromconference**](/windows/win32/api/tspi/nf-tspi-tspi_lineremovefromconference)
-   [**TSPI \_ linesecurecall**](/windows/win32/api/tspi/nf-tspi-tspi_linesecurecall)
-   [**TSPI \_ lineselectextversion**](/windows/win32/api/tspi/nf-tspi-tspi_lineselectextversion)
-   [**TSPI \_ linesenduseruserinfo**](/windows/win32/api/tspi/nf-tspi-tspi_linesenduseruserinfo)
-   [**TSPI \_ linesetappspecific**](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific)
-   [**TSPI \_ linesetcalldata**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalldata)
-   [**TSPI \_ linesetcallhubtracking**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallhubtracking)
-   [**TSPI \_ linesetcallparametriams**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallparams)
-   [**TSPI \_ linesetcallqualityofservice**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallqualityofservice)
-   [**TSPI \_ linesetcalltreatment**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalltreatment)
-   [TSPI \_ linesetcurrentlocation](tspi-linesetcurrentlocation.md)
-   [**TSPI \_ linesetdefaultmediadetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection)
-   [**TSPI \_ linesetdevconfig**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)
-   [**TSPI \_ linesetlinedevstatus**](/windows/win32/api/tspi/nf-tspi-tspi_linesetlinedevstatus)
-   [**TSPI \_ linesetmediacontrol**](/windows/win32/api/tspi/nf-tspi-tspi_linesetmediacontrol)
-   [**TSPI \_ linesetmediamode**](/windows/win32/api/tspi/nf-tspi-tspi_linesetmediamode)
-   [**TSPI- \_ linesetstatus-Meldungen**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)
-   [**TSPI \_ linesetterminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal)
-   [**TSPI \_ linesetupconference**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [**TSPI \_ lineSetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [**TSPI \_ lineswaphold**](/windows/win32/api/tspi/nf-tspi-tspi_lineswaphold)
-   [**TSPI \_ lineuncompletecall**](/windows/win32/api/tspi/nf-tspi-tspi_lineuncompletecall)
-   [**TSPI \_ lineunhold**](/windows/win32/api/tspi/nf-tspi-tspi_lineunhold)
-   [**TSPI \_ lineunpark**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
