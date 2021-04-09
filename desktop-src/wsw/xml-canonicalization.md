---
title: XML-Kanonisierung
description: Die XML-Kanonisierung löst das Problem der Umwandlung eines Satzes von XML-Knoten in Bytes auf eine Weise aus, dass triviale Änderungen an der XML-Datei (z. b. das Ändern der Reihenfolge von Attributen in einem Element) das resultierende Byte Formular nicht ändern.
ms.assetid: a64303a1-efc4-4c91-ab8d-3e389a655b3e
keywords:
- XML-kanonisierungsweb Dienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab8b1aa00b99b604276a479f1a47aacb5bd8b1e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103858558"
---
# <a name="xml-canonicalization"></a>XML-Kanonisierung

Die XML-Kanonisierung löst das Problem der Umwandlung eines Satzes von XML-Knoten in Bytes auf eine Weise aus, dass triviale Änderungen an der XML-Datei (z. b. das Ändern der Reihenfolge von Attributen in einem Element) das resultierende Byte Formular nicht ändern. Die von der Kanonisierung erhaltenen Bytes werden häufig verwendet, um eine kryptografische Signatur über XML-Inhalt zu generieren.


Die häufig verwendeten XML-Kanonisierungsalgorithmen standardisieren die folgenden Aspekte:

-   Zeichencodierung (UTF-8 ohne Präambel)
-   Zeilenvorschub und andere Zeichen Formulare
-   Attribut Reihenfolge in einem Element
-   Leeres Element Formular
-   Rendering von Namespace Deklarationen

Die APIs [**wsstartreadercanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization) und [**wsendreadercanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) stellen die XML-kanonisierungsfunktionalität beim Lesen eines Dokuments bereit.

Die APIs [**wsstartwritercanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization) und [**wsendwritercanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) stellen die XML-kanonisierungsfunktionalität beim Schreiben eines Dokuments bereit.

Die folgenden Enumerationen werden bei der Kanonisierung verwendet:

-   [**WS- \_ XML- \_ Kanonisierungsalgorithmus \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_algorithm)
-   [**Eigenschaften-ID der WS- \_ XML- \_ Kanonisierung \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_property_id)

Die folgenden Funktionen werden bei der Kanonisierung verwendet:

-   [**Wsendreadercanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization)
-   [**Wsendschreiterkanonisierung**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization)
-   [**Wsstartreadercanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization)
-   [**Wsstartschreitercanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization)

Die folgenden Strukturen werden bei der Kanonisierung verwendet:

-   [**\_XML- \_ Kanonisierung \_ inklusive \_ Präfixe**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_inclusive_prefixes)
-   [**WS \_ XML \_ Canonicalization ( \_ Eigenschaft)**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_property)

 

 




