---
title: HTTP Server API Version 2.0-Datentypen
description: HTTP Server API Version 2.0-Datentypen
ms.assetid: 13a0cac9-9e75-4350-a523-5ad9a57caad7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a347b58a97ad89e499136c07f85e18ee2ce1bddc31b5c6d67b8f14a2348a44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950769"
---
# <a name="http-server-api-version-20-data-types"></a>HTTP Server API Version 2.0-Datentypen

Die HTTP-Server-API verwendet verschiedene spezielle Bezeichnertypen, die im Http.h-Header wie folgt deklariert sind:

-   **USHORT** HTTP \_ SERVICE \_ CONFIG \_ TIMEOUT \_ PARAM, \* PHTTP \_ SERVICE \_ CONFIG \_ TIMEOUT \_ PARAM
-   **ULONGLONG** HTTP \_ OPAQUE \_ ID, \* PHTTP \_ OPAQUE \_ ID
-   **HTTP \_ NICHT TRANSPARENTE \_ ID** \_ HTTP-ANFORDERUNGS-ID, \_ \* \_ PHTTP-ANFORDERUNGS-ID \_
-   **HTTP \_ NICHT TRANSPARENTE \_ ID** HTTP-VERBINDUNGS-ID, \_ \_ \* \_ PHTTP-VERBINDUNGS-ID \_
-   **HTTP \_ UNDURCHSICHTIGE \_ ID** HTTP \_ RAW CONNECTION \_ \_ ID, \* PHTTP RAW CONNECTION \_ \_ \_ ID
-   **USHORT** HTTP \_ SERVICE \_ CONFIG \_ TIMEOUT \_ PARAM, \* PHTTP \_ SERVICE \_ CONFIG \_ TIMEOUT \_ PARAM

Eine Anwendung sollte nicht versuchen, einen Bezeichner zu generieren oder zu ändern, der zu einem dieser Typen gehört.

 

 




