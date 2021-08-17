---
title: HTTP Server API Version 1.0-Datentypen
description: Die HTTP-Server-API verwendet verschiedene Bezeichnertypen für spezielle Zwecke, die in der Http.h-Headerdatei als 64-Bit-Ganzzahlen ohne Vorzeichen deklariert sind.
ms.assetid: bec1d41e-0c80-49bc-84e1-b16c409cd0f3
keywords:
- HTTP_CONNECTION_ID HTTP-Typ
- HTTP_RAW_CONNECTION_ID HTTP-Typ
- HTTP_REQUEST_ID HTTP-Typ
- HTTP_URL_CONTEXT HTTP-Typ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151ef975470ca21c6e82e5bc7bd7bd8b99a70573385375e8552b6660ce78f631
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950799"
---
# <a name="http-server-api-version-10-data-types"></a>HTTP Server API Version 1.0-Datentypen

Die HTTP-Server-API verwendet verschiedene spezielle Bezeichnertypen, die in der Http.h-Headerdatei als 64-Bit-Ganzzahlen ohne Vorzeichen deklariert sind (**ULONGLONGs**):

-   \_ \_ HTTP-VERBINDUNGS-ID
-   \_ \_ HTTP-ROHVERBINDUNGS-ID \_
-   \_ \_ HTTP-ANFORDERUNGs-ID
-   \_HTTP-URL-KONTEXT \_

Eine Anwendung sollte nicht versuchen, bezeichner zu generieren oder zu ändern, die zu einem dieser Typen gehören.

 

 




