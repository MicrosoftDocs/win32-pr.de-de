---
title: Konfigurieren der URL-Gruppe
description: .
ms.assetid: be222076-51ff-4907-924f-cc7b0d4fe767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59d9be6969b2b197d0bdcb404ad6b8965c278235
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947906"
---
# <a name="configuring-the-url-group"></a>Konfigurieren der URL-Gruppe

Die URL-Gruppen-ID wird mit der [**httpkreateurlgroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) -Funktion erstellt und im Aufrufen von [**httpablgroupproperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)verwendet. Der *ppropertyinformation* -Parameter verweist auf die Konfigurations Struktur für den Eigenschaftentyp, der festgelegt wird. Der **propertyinformationlength** -Parameter gibt die Größe der Konfigurations Struktur in Bytes an. Wenn Sie z. b. **httpservertimeoutsproperty** festlegen, muss der *ppropertyinformation* -Parameter auf einen Puffer zeigen, der nicht kleiner als die Informationsstruktur für das [**http- \_ Timeout \_ Limit \_**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) sein darf. Die URL-Gruppen Konfigurationen werden durch Aufrufen von " [**httpqueryurlgroupproperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)" abgefragt.

Nachdem die URL-Gruppe erstellt wurde, werden der Gruppe mit [**httpaddurltourlgroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup)URLs hinzugefügt. Die URL-Gruppe muss mit einer Anforderungs Warteschlange der Version 2,0 verknüpft werden, um Anforderungen zu empfangen. Um die URL-Gruppe einer Anforderungs Warteschlange zuzuordnen, ruft die Anwendung [**httpseturlgroupproperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) auf und gibt **httpserverbindingproperty** im *Property* -Parameter an. Wenn diese Eigenschaft nicht festgelegt ist, werden übereinstimmende Anforderungen für die URL-Gruppe nicht an eine Anforderungs Warteschlange gesendet, und die HTTP-Server-API generiert eine 503-Antwort. Die Anwendung kann nur URLs hinzufügen, die zuvor mit dem Dienst für eine URL-Gruppe reserviert wurden, wenn Sie mit niedrigen Berechtigungen ausgeführt wird. Weitere Informationen finden Sie im Thema [Namespace Reservierungen, Registrierungen und Routing](namespace-reservations-registrations-and-routing.md) .

 

 




