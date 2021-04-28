---
title: Konfigurieren der Serversitzung
description: Konfigurieren der Serversitzung
ms.assetid: 1e4e9440-8d70-44df-90a7-2d5e25b2f680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d41c1606cce397c49a15c62dae10531edfde93f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090938"
---
# <a name="configuring-the-server-session"></a>Konfigurieren der Serversitzung

Die Serversitzungs-ID wird mit der [**HttpCreateServerSession-Funktion**](/windows/desktop/api/Http/nf-http-httpcreateserversession) erstellt und im Aufruf von [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)verwendet. Der *pPropertyInformation-Parameter* verweist auf die Konfigurationsstruktur für den festgelegten Eigenschaftentyp. Der *Parameter PropertyInformationLength* gibt die Größe der Konfigurationsstruktur in Bytes an. Wenn Sie beispielsweise **httpServerTimeoutsProperty** festlegen, muss der **pPropertyInformation-Parameter** auf einen Puffer verweisen, der mindestens die Größe der [**HTTP \_ TIMEOUT \_ LIMIT \_ INFO-Struktur**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) aufweist.

In der Regel erstellt eine HTTP-Anwendung eine einzelne Serversitzung und kann anwendungsweite Eigenschaften festlegen, z. B. eine globale Bandbreiteneinschränkungsgrenze, oder die zentralisierte Protokollierung für diese Serversitzung aktivieren. [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) überschreibt die HTTP-Server-API-Konfigurationen für die aufrufende Anwendung. Sie wirkt sich nicht auf die HTTP-Server-API-weiten Eigenschaften aus. Die Serversitzungskonfigurationen werden durch Aufrufen von [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)abgefragt.

 

 




