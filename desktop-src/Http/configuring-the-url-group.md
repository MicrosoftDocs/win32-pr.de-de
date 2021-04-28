---
title: Konfigurieren der URL-Gruppe
description: Konfigurieren der URL-Gruppe
ms.assetid: be222076-51ff-4907-924f-cc7b0d4fe767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 407ca18fc5d2797c99e86661bf462eaf0a3fdc5b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109698"
---
# <a name="configuring-the-url-group"></a>Konfigurieren der URL-Gruppe

Die URL-Gruppen-ID wird mit der [**HttpCreateUrlGroup-Funktion**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) erstellt und im Aufruf von [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)verwendet. Der *pPropertyInformation-Parameter* verweist auf die Konfigurationsstruktur für den festgelegten Eigenschaftentyp. Der **Parameter PropertyInformationLength** gibt die Größe der Konfigurationsstruktur in Bytes an. Wenn Sie beispielsweise **httpServerTimeoutsProperty** festlegen, muss der *pPropertyInformation-Parameter* auf einen Puffer verweisen, der nicht kleiner als die [**HTTP \_ TIMEOUT \_ LIMIT \_ INFO-Struktur**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) sein darf. Die URL-Gruppenkonfigurationen werden durch Aufrufen von [**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)abgefragt.

Nachdem die URL-Gruppe erstellt wurde, werden der Gruppe mit [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup)URLs hinzugefügt. Die URL-Gruppe muss einer Anforderungswarteschlange der Version 2.0 zugeordnet werden, um Anforderungen zu empfangen. Um die URL-Gruppe einer Anforderungswarteschlange zuzuordnen, ruft die Anwendung [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) auf und gibt **HttpServerBindingProperty** im *Property-Parameter* an. Wenn diese Eigenschaft nicht festgelegt ist, werden übereinstimmende Anforderungen für die URL-Gruppe nicht an eine Anforderungswarteschlange übermittelt, und die HTTP-Server-API generiert eine 503-Antwort. Die Anwendung kann einer URL-Gruppe nur URLs hinzufügen, die zuvor für den Dienst reserviert wurden, wenn sie mit geringen Rechten ausgeführt wird. Weitere Informationen finden Sie im Thema [Namespacereservierungen, Registrierungen und Routing.](namespace-reservations-registrations-and-routing.md)

 

 




