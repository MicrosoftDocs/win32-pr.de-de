---
description: Ab version Windows 2000 müssen Telefoniedienstanbieter, die eine Version von 3.0 oder höher aushandeln, über einen übereinstimmenden Mediendienstanbieter verfügen.
ms.assetid: 9235c631-77bc-42c6-8139-9208c9c254b4
title: Media Service Provider Communication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3797d02c67fc86ebfb44ff9e0e7b2c85cd1604206a58f1d8f5c3ca293599e92d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404820"
---
# <a name="media-service-provider-communication"></a>Media Service Provider Communication

Ab version Windows 2000 müssen Telefoniedienstanbieter, die eine Version von 3.0 oder höher aushandeln, über einen übereinstimmenden Mediendienstanbieter verfügen. Die genaue Aufteilung der operativen Zuständigkeiten hängt von der Implementierung ab. Beispielsweise kann ein TSP den entsprechenden MSP verwenden, um die Ermittlung des Medientyps für eine eingehende Sitzung durchzuführen. Der TSP muss jedoch dem TSPI entsprechen. Dies bedeutet, dass diese Bestimmung vom MSP erhalten und an TAPI berichtet wird.

TSPI stellt die folgenden Funktionen und Meldungen zur Verfügung, um eine virtuelle Verbindung zwischen einem TSP und einem MSP zu ermöglichen:

-   [**\_TSPI-ZeileCloseMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [**TSPI \_ lineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [**TSPI \_ lineMSPIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [**TSPI \_ lineReceiveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [**LINE \_ QOSINFO**](line-qosinfo.md)
-   [**LINE \_ SENDMSPDATA**](line-sendmspdata.md)

 

 
