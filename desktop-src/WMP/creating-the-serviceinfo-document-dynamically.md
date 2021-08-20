---
title: Dynamisches Erstellen des ServiceInfo-Dokuments
description: Dynamisches Erstellen des ServiceInfo-Dokuments
ms.assetid: 96937b04-f705-49f6-8ddf-25c98a51dc9a
keywords:
- Windows Media Player,Erstellen eines ServiceInfo-Dokuments
- Onlineshops,Erstellen eines ServiceInfo-Dokuments
- Typ 1 Onlineshops,Erstellen eines ServiceInfo-Dokuments
- 'Typ 2: Onlineshops,Erstellen eines ServiceInfo-Dokuments'
- Windows Media Player Onlineshops,dynamisches Erstellen eines ServiceInfo-Dokuments
- Onlineshops,dynamisches Erstellen eines ServiceInfo-Dokuments
- Geben Sie 1 Onlineshops ein, und erstellen Sie dynamisch ein ServiceInfo-Dokument.
- 'Typ 2: Onlineshops, dynamisches Erstellen eines ServiceInfo-Dokuments'
- Windows Media Player,ServiceInfo-Dokument
- Onlineshops,ServiceInfo-Dokument
- Typ 1 Onlineshops,ServiceInfo-Dokument
- Typ 2 Onlineshops,ServiceInfo-Dokument
- Dynamisches Erstellen eines ServiceInfo-Dokuments
- Erstellen eines ServiceInfo-Dokuments
- ServiceInfo-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3883487d072af57174a1f40f2fcef05d3290917b473a95bf723c34d793c5ba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340990"
---
# <a name="creating-the-serviceinfo-document-dynamically"></a>Dynamisches Erstellen des ServiceInfo-Dokuments

Sie können ASP verwenden, um Ihr ServiceInfo-Dokument zu erstellen. Dies kann Ihnen mithilfe der folgenden Techniken mehr Flexibilität in Ihrem Onlineshop bieten:

-   Dynamisches Generieren des Hostnamens für URLs.
-   Ändern von URLs für die Lokalisierung basierend auf Locale- und Geoidparametern.
-   Dynamisches Anfügen von Abfragezeichenfolgenparametern aus der ServiceInfo-URL an andere URLs, z. B. die URL der Navigationsseite.

Der folgende Beispielcode zeigt eine einfache ASP-Seite, die dynamisch ein ServiceInfo-Dokument erstellt:


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



Im obigen Beispielcode wird ASP verwendet, um den Hostnamen vom Webserver abzurufen und die URLs im Dokument dynamisch zu erstellen. Der Code ruft auch den *Abfragezeichenfolgenparameter des Locale-Objekts* aus der ServiceInfo-Anforderung ab und fügt ihn an die URL für die Navigationsseite an.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Allgemeine Informationen zu Onlineshops vom Typ 1 und 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Navigation für Typ 2-Onlineshops**](navigation-for-type-2-online-stores.md)
</dt> <dt>

[**ServiceInfo-Dokument für eine Online-Store**](serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**ServiceInfo-Dokument für eine Online-Store**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 




