---
description: Die IDownloadProgress-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 8f64c702-b2b5-4a5f-9365-bc962e35f499
title: IDownloadProgress-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeed70acfb6b350c463b731d44cfe0d48cc1fd8a5190c247fcda316c4707126f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130572"
---
# <a name="idownloadprogress-properties"></a>IDownloadProgress-Eigenschaften

Die [**IDownloadProgress-Schnittstelle**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) definiert die folgenden Eigenschaften.



| Eigenschaft                                                                               | Beschreibung                                                                                                                                      |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CurrentUpdateBytesDownloaded**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytesdownloaded) | Ruft eine Zeichenfolge ab, die angibt, wie viele Daten für die Inhaltsdatei oder die Dateien des updates, das heruntergeladen wird, in Bytes übertragen wurden.  |
| [**CurrentUpdateBytesToDownload**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytestodownload) | Ruft eine Zeichenfolge ab, die schätzt, wie viele Daten für die Inhaltsdatei oder die Dateien des updates, das heruntergeladen wird, in Bytes übertragen werden sollen. |
| [**CurrentUpdateDownloadPhase**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatedownloadphase)     | Ruft einen [**DownloadPhase-Enumerationswert**](/windows/win32/api/wuapi/ne-wuapi-downloadphase) ab, der die Phase des Downloads angibt, die gerade läuft.          |
| [**CurrentUpdateIndex**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdateindex)                     | Ruft einen nullbasierten Indexwert ab, der das Update angibt, das gerade heruntergeladen wird, wenn mehrere Updates ausgewählt wurden.             |
| [**CurrentUpdatePercentComplete**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatepercentcomplete) | Ruft eine Schätzung des Prozentsatzes des aktuellen Updates ab, das heruntergeladen wurde.                                                               |
| [**Percentcomplete**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_percentcomplete)                           | Ruft eine Schätzung des Prozentsatzes aller heruntergeladenen Updates ab.                                                                 |
| [**TotalBytesDownloaded**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytesdownloaded)                 | Ruft eine Zeichenfolge ab, die die Gesamtmenge der heruntergeladenen Daten in Bytes angibt.                                                        |
| [**TotalBytesToDownload**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytestodownload)                 | Ruft eine Zeichenfolge ab, die die Schätzung der Gesamtmenge der heruntergeladenen Daten in Bytes darstellt.                                        |



 

 

 



