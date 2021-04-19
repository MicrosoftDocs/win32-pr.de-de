---
title: url
description: Die wwsapi-URL-API-Elemente stellen Mechanismen bereit, mit denen Sie URLs in Komponenten Teile aufteilen und aus Escapezeichen versehen und Komponenten Teile wieder in eine URL umwandeln können.
ms.assetid: 2904fee0-d92b-4054-8ad9-51c409756f33
keywords:
- URL-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8511bf755f80f124071f658a65249243dc2f2af
ms.sourcegitcommit: 6f8c895f4d43c4463f6f33fa8014c5de413ece1f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/20/2020
ms.locfileid: "106339050"
---
# <a name="url"></a>url

Die wwsapi-URL-API-Elemente stellen Mechanismen bereit, mit denen Sie URLs in Komponenten Teile aufteilen und aus Escapezeichen versehen und Komponenten Teile wieder in eine URL umwandeln können.

-   Verwenden Sie die [**wsdecodeurl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl) -Funktion, um URLs zu teilen und in Komponenten Teile zu entweichen.
-   Verwenden Sie zum Escapezeichen und zum Kombinieren von Komponenten teilen in einer URL die [**wsencodeurl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl) -Funktion.
-   Um relative URLs mit einer absoluten Basis-URL zu kombinieren, die eine absolute URL bildet, verwenden Sie die [**wscombineurl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl) -Funktion.

Die folgenden Enumerationen sind Teil der URL:

-   [**WS- \_ URL- \_ Flags**](/windows/win32/api/webservices/ne-webservices-ws_xml_writer_encoding_type)
-   [**WS- \_ URL- \_ \_ schematentyp**](/windows/desktop/api/WebServices/ne-webservices-ws_url_scheme_type)

Die folgenden Funktionen sind Teil der URL:

-   [**Wscombineurl**](/windows/desktop/api/WebServices/nf-webservices-wscombineurl)
-   [**Wsdecodeurl**](/windows/desktop/api/WebServices/nf-webservices-wsdecodeurl)
-   [**Wsencodeurl**](/windows/desktop/api/WebServices/nf-webservices-wsencodeurl)

Die folgenden Strukturen sind Teil der URL:

-   [**WS- \_ https- \_ URL**](/windows/desktop/api/WebServices/ns-webservices-ws_https_url)
-   [**WS- \_ http- \_ URL**](/windows/desktop/api/WebServices/ns-webservices-ws_http_url)
-   [**WS \_ netpipe- \_ URL**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [**WS \_ NetTcp- \_ URL**](/windows/desktop/api/WebServices/ns-webservices-ws_nettcp_url)
-   [**WS \_ soapudp- \_ URL**](/windows/desktop/api/WebServices/ns-webservices-ws_soapudp_url)
-   [**WS- \_ URL**](/windows/desktop/api/WebServices/ns-webservices-ws_url)

 

 




