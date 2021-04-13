---
description: Beginnend mit Windows 2000-Telefoniedienstanbietern, die eine Version von 3,0 oder höher aushandeln, muss ein entsprechender Medien Dienstanbieter vorhanden sein.
ms.assetid: 9235c631-77bc-42c6-8139-9208c9c254b4
title: Kommunikation mit dem Mediendienst Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a50ec6a4fb96a86ceab3a302b138ee72d6c61b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351478"
---
# <a name="media-service-provider-communication"></a>Kommunikation mit dem Mediendienst Anbieter

Beginnend mit Windows 2000-Telefoniedienstanbietern, die eine Version von 3,0 oder höher aushandeln, muss ein entsprechender Medien Dienstanbieter vorhanden sein. Die genaue Division von betrieblichen Zuständigkeiten ist implementierungsabhängig. Beispielsweise kann ein TSP den passenden MSP verwenden, um die Medientyp Bestimmung für eine eingehende Sitzung auszuführen. Der TSP muss jedoch dem TSPI entsprechen. Dies bedeutet, dass diese Bestimmung vom MSP erhalten und an TAPI gemeldet wird.

TSPI bietet die folgenden Funktionen und Meldungen, um eine virtuelle Verbindung zwischen einem TSP und einem MSP zuzulassen:

-   [**TSPI \_ lineclosemspinstance**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [**TSPI \_ linecreatemspinstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [**TSPI \_ linemspidentify**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [**TSPI \_ linereceivemspdata**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [**Zeilen- \_ qosinfo**](line-qosinfo.md)
-   [**Zeile \_ sendmspdata**](line-sendmspdata.md)

 

 
