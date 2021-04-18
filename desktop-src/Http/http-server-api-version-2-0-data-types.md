---
title: HTTP Server-API, Version 2,0, Datentypen
description: HTTP Server-API, Version 2,0, Datentypen
ms.assetid: 13a0cac9-9e75-4350-a523-5ad9a57caad7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670099f3303682f52fdc78397dc7f229577b94d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340443"
---
# <a name="http-server-api-version-20-data-types"></a>HTTP Server-API, Version 2,0, Datentypen

Die HTTP-Server-API verwendet verschiedene im http. h-Header deklarierte Typen von speziellen Zweck Bezeichnern wie folgt:

-   **UShort** Timeout für HTTP- \_ Dienst \_ Konfigurations \_ Timeout \_ , \* Phttp- \_ Dienst \_ Konfigurations \_ Timeout \_ Parameter
-   **ULONGLONG** HTTP \_ - \_ opop-ID, nicht transparente \* Phttp- \_ \_ ID
-   **Http \_ nicht transparente \_ ID** HTTP-Anforderungs- \_ \_ ID, \* Phttp- \_ Anforderungs- \_ ID
-   **Http \_ nicht transparente \_ ID** HTTP-Verbindungs- \_ \_ ID, \* Phttp- \_ Verbindungs- \_ ID
-   **Http \_ nicht transparente \_ ID** http- \_ \_ rohverbindungs- \_ ID, \* Phttp- \_ \_ rohverbindungs- \_ ID
-   **UShort** Timeout für HTTP- \_ Dienst \_ Konfigurations \_ Timeout \_ , \* Phttp- \_ Dienst \_ Konfigurations \_ Timeout \_ Parameter

Eine Anwendung sollte nicht versuchen, einen Bezeichner zu generieren oder zu ändern, der zu einem dieser Typen gehört.

 

 




