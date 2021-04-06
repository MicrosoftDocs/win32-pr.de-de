---
title: Dynamisches Erstellen des serviceingefo-Dokuments
description: Dynamisches Erstellen des serviceingefo-Dokuments
ms.assetid: 96937b04-f705-49f6-8ddf-25c98a51dc9a
keywords:
- Windows Media Player Online Stores, Erstellen eines serviceingefo-Dokuments
- Online Stores, Erstellen eines serviceingefo-Dokuments
- Typ 1 Online Stores, serviceInfo-Dokument wird erstellt
- Typ 2 Online Stores, Erstellen von serviceInfo-Dokumenten
- Windows Media Player Online Stores, Dynamisches Erstellen von servicabfo-Dokumenten
- Online Stores, Dynamisches Erstellen von serviceingefo-Dokumenten
- Typ 1 Online Stores, Dynamisches Erstellen von serviceInfo-Dokumenten
- Typ 2 Online Stores, Dynamisches Erstellen von serviceInfo-Dokumenten
- Windows Media Player Online Stores, serviceingefo-Dokument
- Online Stores, serviceingefo-Dokument
- Typ 1 Online Stores, serviceInfo-Dokument
- Typ 2 Online Stores, serviceInfo-Dokument
- Dynamisches Erstellen von servicinfo-Dokumenten
- servicinfo-Dokument wird erstellt
- Servicinfo-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90159e72046536cf6b69521586a0640935478eb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947427"
---
# <a name="creating-the-serviceinfo-document-dynamically"></a>Dynamisches Erstellen des serviceingefo-Dokuments

Sie können ASP zum Erstellen des serviceingefo-Dokuments verwenden. Dadurch erhalten Sie mehr Flexibilität in Ihrem Online Store, indem Sie die folgenden Verfahren verwenden:

-   Dynamisches Erstellen des Host Namens für URLs.
-   Ändern von URLs für die Lokalisierung basierend auf Gebiets Schema-und Geoid-Parametern.
-   Dynamisches Anfügen von Abfrage Zeichen folgen Parametern aus der serviceingefo-URL an andere URLs, z. b. die URL der Navigationsseite.

Der folgende Beispielcode zeigt eine einfache ASP-Seite, die ein servicanfo-Dokument dynamisch erstellt:


```C++
<%
    Dim sHost
    Dim sLocale

    sHost = Request.ServerVariables("HTTP_HOST")
    sLocale = Request.QueryString("locale")
%>

<?xml version="1.0" encoding="utf-8"?>
<ServiceInfo Version="1.00" Key="MyCommerceService">
    <FriendlyName>My Online Store</FriendlyName>
    <ServiceTask1
        URL = "https://<%= sHost %>/service/html/Music.asp">
    </ServiceTask1>
    <ServiceTask2
        URL = "https://<%= sHost %>/service/html/Video.asp">
    </ServiceTask2>
    <ServiceTask3
        URL = "https://<%= sHost %>/service/html/Radio.asp">
    </ServiceTask3>
    <Navigate
        BaseURL = "https://<%= sHost %>/service/html/navigate.asp?myloc<%= sLocale %>">
    </Navigate>
</ServiceInfo>
```



Der vorherige Beispielcode verwendet ASP zum Abrufen des Host namens vom Webserver und zum dynamischen Erstellen der URLs im Dokument. Der Code ruft auch den Parameter für die *locale* -Abfrage Zeichenfolge aus der servicinfo-Anforderung ab und fügt ihn an die URL für die Navigationsseite an.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Navigation für den Typ 2-Online Speicher**](navigation-for-type-2-online-stores.md)
</dt> <dt>

[**ServiceInfo-Dokument für einen Typ-1-Online Store**](serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**ServiceInfo-Dokument für einen Typ 2-Online Store**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Servicinfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 




