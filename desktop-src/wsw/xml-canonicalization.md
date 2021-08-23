---
title: XML-Kanonisierung
description: Die XML-Kanonisierung löst das Problem der Konvertierung einer Reihe von XML-Knoten in Bytes so, dass triviale Änderungen am XML-Code (z. B. das Ändern der Reihenfolge von Attributen in einem Element) die resultierende Byteform nicht ändern.
ms.assetid: a64303a1-efc4-4c91-ab8d-3e389a655b3e
keywords:
- XML-Kanonisierungswebdienste für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db77e449c4e3d6ee5f6e2cb474c84a6b1161a4fee87c35d01d278882b178cc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082984"
---
# <a name="xml-canonicalization"></a>XML-Kanonisierung

Die XML-Kanonisierung löst das Problem der Konvertierung einer Reihe von XML-Knoten in Bytes so, dass triviale Änderungen am XML-Code (z. B. das Ändern der Reihenfolge von Attributen in einem Element) die resultierende Byteform nicht ändern. Die aus der Kanonisierung erhaltenen Bytes werden häufig verwendet, um eine kryptografische Signatur über XML-Inhalt zu generieren.


Die häufig verwendeten XML-Kanonisierungsalgorithmen standardisieren die folgenden Aspekte:

-   Zeichencodierung (UTF-8 ohne Präambel)
-   Zeilenfeed und andere Zeichenformen
-   Attribut reihenfolge in einem Element
-   Leeres Elementformular
-   Rendern von Namespacedeklarationen

Die APIs [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization) und [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) stellen die XML-Kanonisierungsfunktionalität beim Lesen eines Dokuments zur Verfügung.

Die APIs [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization) und [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) stellen die XML-Kanonisierungsfunktionalität beim Schreiben eines Dokuments zur Verfügung.

Die folgenden Enumerationen werden bei der Kanonisierung verwendet:

-   [**WS \_ \_ XML-KANONISIERUNGSALGORITHMUS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_algorithm)
-   [**WS \_ \_ XML-KANONISIERUNGSEIGENSCHAFTS-ID \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_property_id)

Die folgenden Funktionen werden bei der Kanonisierung verwendet:

-   [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization)
-   [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization)
-   [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization)
-   [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization)

Die folgenden Strukturen werden bei der Kanonisierung verwendet:

-   [**INKLUSIVE WS \_ \_ XML-KANONISIERUNGSPRÄFIXE \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_inclusive_prefixes)
-   [**WS \_ \_ XML-KANONISIERUNGSEIGENSCHAFT \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_property)

 

 




