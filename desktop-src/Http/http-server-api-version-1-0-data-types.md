---
title: HTTP Server-API, Version 1,0, Datentypen
description: Die HTTP-Server-API verwendet verschiedene in der http. h-Header Datei deklarierte Typen von speziellen Zweck Bezeichnern als 64-Bit-Ganzzahlen ohne Vorzeichen.
ms.assetid: bec1d41e-0c80-49bc-84e1-b16c409cd0f3
keywords:
- HTTP_CONNECTION_ID http-Typ
- HTTP_RAW_CONNECTION_ID http-Typ
- HTTP_REQUEST_ID http-Typ
- HTTP_URL_CONTEXT http-Typ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 681e24c06334a9010287e2084d9d6a04428ca6a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338019"
---
# <a name="http-server-api-version-10-data-types"></a>HTTP Server-API, Version 1,0, Datentypen

Die HTTP-Server-API verwendet verschiedene Typen von speziellen Zweck Bezeichnern, die in der http. h-Header Datei als 64-Bit-Ganzzahlen ohne Vorzeichen (**ulonglongs**) deklariert sind:

-   HTTP- \_ Verbindungs- \_ ID
-   HTTP \_ - \_ rohverbindungs- \_ ID
-   HTTP- \_ Anforderungs- \_ ID
-   HTTP- \_ URL- \_ Kontext

Eine Anwendung sollte nicht versuchen, einen Bezeichner zu generieren oder zu ändern, der zu einem dieser Typen gehört.

 

 




