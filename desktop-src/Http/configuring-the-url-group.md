---
title: Konfigurieren der URL-Gruppe
description: Konfigurieren der URL-Gruppe
ms.assetid: be222076-51ff-4907-924f-cc7b0d4fe767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d2d335af063eb8cadc557db3f01da850b468099866e292bcd5ea2a3af314de8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014908"
---
# <a name="configuring-the-url-group"></a>Konfigurieren der URL-Gruppe

Die URL-Gruppen-ID wird mit der [**HttpCreateUrlGroup-Funktion**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) erstellt und im Aufruf von [**HttpSetUrlGroupProperty verwendet.**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) Der *pPropertyInformation-Parameter* verweist auf die Konfigurationsstruktur für den festgelegten Eigenschaftentyp. Der **PropertyInformationLength-Parameter** gibt die Größe der Konfigurationsstruktur in Bytes an. Wenn Sie beispielsweise **httpServerTimeoutsProperty** festlegen, muss der *pPropertyInformation-Parameter* auf einen Puffer zeigen, der nicht kleiner als die [**HTTP \_ TIMEOUT \_ LIMIT \_ INFO-Struktur**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) sein darf. Die URL-Gruppenkonfigurationen werden durch Aufrufen von [**HttpQueryUrlGroupProperty abgefragt.**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)

Nachdem die URL-Gruppe erstellt wurde, werden der Gruppe mit [**HttpAddUrlToUrlGroup URLs hinzugefügt.**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) Die URL-Gruppe muss einer Anforderungswarteschlange der Version 2.0 zugeordnet sein, um Anforderungen zu empfangen. Um die URL-Gruppe einer Anforderungswarteschlange zu zuordnen, ruft die Anwendung [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) auf und gibt **HttpServerBindingProperty** im *Property-Parameter* an. Wenn diese Eigenschaft nicht festgelegt ist, werden übereinstimmende Anforderungen für die URL-Gruppe nicht an eine Anforderungswarteschlange übermittelt, und die HTTP-Server-API generiert eine 503-Antwort. Die Anwendung kann nur URLs, die zuvor für den Dienst reserviert wurden, einer URL-Gruppe hinzufügen, wenn sie mit geringen Berechtigungen ausgeführt wird. Weitere Informationen finden Sie im Thema [Namespacereservierungen, Registrierungen und Routing.](namespace-reservations-registrations-and-routing.md)

 

 




