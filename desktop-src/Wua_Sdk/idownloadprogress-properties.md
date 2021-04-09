---
description: Die idownloadprogress-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 8f64c702-b2b5-4a5f-9365-bc962e35f499
title: Idownloadprogress-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469246acb59b4aa58efcbf4bb5aa7f04b7e44b6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958988"
---
# <a name="idownloadprogress-properties"></a>Idownloadprogress-Eigenschaften

Die [**idownloadprogress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) -Schnittstelle definiert die folgenden Eigenschaften.



| Eigenschaft                                                                               | BESCHREIBUNG                                                                                                                                      |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Currentupdatebytesherunter geladen**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytesdownloaded) | Ruft eine Zeichenfolge ab, die angibt, wie viele Daten für die Inhalts Datei oder Dateien des heruntergeladenen Updates in Bytes übertragen wurden.  |
| [**Currentupdatebytestodownload**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytestodownload) | Ruft eine Zeichenfolge ab, die schätzt, wie viele Daten für die Inhalts Datei oder Dateien des heruntergeladenen Updates in Bytes übertragen werden sollen. |
| [**Currentupdatedownloadphase**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatedownloadphase)     | Ruft einen [**Downloadphase**](/windows/win32/api/wuapi/ne-wuapi-downloadphase) -Enumerationswert ab, der die Phase des Downloads angibt, der gerade ausgeführt wird.          |
| [**Currentupdateingedex**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdateindex)                     | Ruft einen NULL basierten Indexwert ab, der das Update angibt, das gerade heruntergeladen wird, wenn mehrere Updates ausgewählt wurden.             |
| [**Currentupdateprozentucomplete**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatepercentcomplete) | Ruft eine Schätzung des Prozentsatzes des aktuellen Updates ab, das heruntergeladen wurde.                                                               |
| [**PercentComplete**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_percentcomplete)                           | Ruft eine Schätzung des Prozentsatzes aller Updates ab, die heruntergeladen wurden.                                                                 |
| [**Totalbytesherunter geladen**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytesdownloaded)                 | Ruft eine Zeichenfolge ab, die die Gesamtmenge der heruntergeladenen Daten in Bytes angibt.                                                        |
| [**Totalbytestodownload**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytestodownload)                 | Ruft eine Zeichenfolge ab, die die Schätzung der Gesamtmenge der heruntergeladenen Daten in Bytes darstellt.                                        |



 

 

 



