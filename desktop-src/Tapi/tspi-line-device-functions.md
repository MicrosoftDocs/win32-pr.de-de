---
description: Dieser Abschnitt enthält eine alphabetische Liste der verfügbaren Liniengerätefunktionen in der Telefonie-SPI.
ms.assetid: 2a27fbb7-93b5-4106-afd3-e63456650fb9
title: TSPI-Line-Gerätefunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a52282154e99ca4e400f6b2d5f32d00a19d62cfe98f0b789d4ee24b9a240293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119403710"
---
# <a name="tspi-line-device-functions"></a>TSPI-Line-Gerätefunktionen

Dieser Abschnitt enthält eine alphabetische Liste der verfügbaren Liniengerätefunktionen in der Telefonie-SPI. Die Informationen für jede Funktion umfassen Folgendes:

-   Eine -Anweisung des Zwecks der Funktion.
-   Die richtige Syntax für die Funktion.
-   Eine Beschreibung der Parameter der Funktion, einschließlich gültiger Aufrufzustände.
-   Eine Beschreibung des Rückgabewerts der Funktion.
-   Ein Abschnitt "Hinweise", der eine oder alle der folgenden Punkte enthalten kann: eine Liste der gültigen Aufrufzustände beim Eintrag der Funktion und typische Aufrufzustandsübergänge, wenn die Anforderung abgeschlossen ist; eine Beschreibung, welche Member großer Datenstrukturen vom Dienstanbieter ausgefüllt werden müssen und welche Member ihre Werte intakt beibehalten müssen; und vergleichen sie mit einer entsprechenden Funktion in TAPI.
-   Verweise auf andere Funktionen, Nachrichten oder Datenstrukturen.
    > [!Note]  
    > Die tatsächlichen Zustände, in denen eine Funktion ausgeführt werden kann, können durch die Funktionen des Dienstanbieters eingeschränkt werden. Dienstanbieter müssen das **dwCallFeatures-Member** in der [**LINECALLSTATUS-Struktur,**](/windows/win32/api/tapi/ns-tapi-linecallstatus) das **dwAddressFeatures-Member** in der [**LINEADDRESSSTATUS-Struktur**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) und das **dwLineFeatures-Member** in der [**LINEDEVSTATUS-Struktur**](/windows/win32/api/tapi/ns-tapi-linedevstatus) festlegen, um Anwendungen anzugeben, ob eine Funktion zu diesem Zeitpunkt zulässig ist.

     

Dieser Abschnitt enthält die folgenden TSPI-Zeilengerätefunktionen:

-   [**TSPI \_ lineAccept**](/windows/win32/api/tspi/nf-tspi-tspi_lineaccept)
-   [**TSPI \_ lineAddToConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineaddtoconference)
-   [**TSPI \_ lineAnswer**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer)
-   [**TSPI \_ lineBlindTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_lineblindtransfer)
-   [**\_TSPI-ZeileSchließen**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose)
-   [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)
-   [**\_TSPI-ZeileCloseMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [**TSPI \_ lineCompleteCall**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletecall)
-   [**TSPI \_ lineCompleteTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [**TSPI \_ lineConditionalMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_lineconditionalmediadetection)
-   [**TSPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog)
-   [**TSPI \_ lineConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialogedit)
-   [**TSPI \_ lineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [**TSPI \_ lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
-   [**TSPI \_ lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
-   [**TSPI \_ lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial)
-   [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop)
-   [TSPI \_ lineDropNoOwner](tspi-linedropnoowner.md)
-   [TSPI \_ lineDropOnClose](tspi-linedroponclose.md)
-   [**TSPI \_ lineForward**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [**TSPI \_ lineGatherDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegatherdigits)
-   [**TSPI \_ lineGenerateDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits)
-   [**TSPI \_ lineGenerateTone**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratetone)
-   [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)
-   [**TSPI \_ lineGetAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)
-   [**TSPI \_ lineGetAddressStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus)
-   [**TSPI \_ lineGetCallAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid)
-   [**TSPI \_ lineGetCallHubTracking**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallhubtracking)
-   [**TSPI \_ lineGetCallIDs**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallids)
-   [**TSPI \_ lineGetCallInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)
-   [**\_TSPI-ZeileGetCallStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)
-   [**TSPI \_ lineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)
-   [**TSPI \_ lineGetDevConfig**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)
-   [**TSPI \_ lineGetExtensionID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetextensionid)
-   [**\_TSPI-ZeileGetIcon**](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)
-   [**TSPI \_ lineGetID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)
-   [**TSPI \_ lineGetLineDevStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)
-   [**TSPI \_ lineGetNumAddressIDs**](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids)
-   [**TSPI \_ lineHold**](/windows/win32/api/tspi/nf-tspi-tspi_linehold)
-   [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [**TSPI \_ lineMonitorDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitordigits)
-   [**TSPI \_ lineMonitorMedia**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitormedia)
-   [**TSPI \_ lineMonitorTones**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitortones)
-   [**TSPI \_ lineMSPIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [**TSPI \_ lineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion)
-   [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion)
-   [**\_TSPI-ZeileOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)
-   [**TSPI \_ linePark**](/windows/win32/api/tspi/nf-tspi-tspi_linepark)
-   [**TSPI \_ linePickup**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [**TSPI \_ linePrepareAddToConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [**TSPI \_ lineReceiveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [**TSPI \_ lineRedirect**](/windows/win32/api/tspi/nf-tspi-tspi_lineredirect)
-   [**TSPI \_ lineReleaseUserUserInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linereleaseuseruserinfo)
-   [**TSPI \_ lineRemoveFromConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineremovefromconference)
-   [**TSPI \_ lineSecureCall**](/windows/win32/api/tspi/nf-tspi-tspi_linesecurecall)
-   [**TSPI \_ lineSelectExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_lineselectextversion)
-   [**TSPI \_ lineSendUserUserInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linesenduseruserinfo)
-   [**TSPI \_ lineSetAppSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific)
-   [**TSPI \_ lineSetCallData**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalldata)
-   [**TSPI \_ lineSetCallHubTracking**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallhubtracking)
-   [**TSPI \_ lineSetCallParams**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallparams)
-   [**TSPI \_ lineSetCallQualityOfService**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallqualityofservice)
-   [**TSPI \_ lineSetCallTreatment**](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalltreatment)
-   [TSPI \_ lineSetCurrentLocation](tspi-linesetcurrentlocation.md)
-   [**TSPI \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection)
-   [**TSPI \_ lineSetDevConfig**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)
-   [**TSPI \_ lineSetLineDevStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linesetlinedevstatus)
-   [**TSPI \_ lineSetMediaControl**](/windows/win32/api/tspi/nf-tspi-tspi_linesetmediacontrol)
-   [**TSPI \_ lineSetMediaMode**](/windows/win32/api/tspi/nf-tspi-tspi_linesetmediamode)
-   [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)
-   [**TSPI \_ lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal)
-   [**TSPI \_ lineSetupConference**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [**TSPI \_ lineSetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [**TSPI \_ lineSwapHold**](/windows/win32/api/tspi/nf-tspi-tspi_lineswaphold)
-   [**TSPI \_ lineUncompleteCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineuncompletecall)
-   [**TSPI \_ lineUnhold**](/windows/win32/api/tspi/nf-tspi-tspi_lineunhold)
-   [**TSPI \_ lineUnpark**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
