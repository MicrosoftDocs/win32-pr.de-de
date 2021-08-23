---
title: Konfigurieren der Serversitzung
description: Konfigurieren der Serversitzung
ms.assetid: 1e4e9440-8d70-44df-90a7-2d5e25b2f680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321d2710a0d9a0f7f3c70ad6de84336d382ae161b938ee2e22f20ddde5012604
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746590"
---
# <a name="configuring-the-server-session"></a>Konfigurieren der Serversitzung

Die Serversitzungs-ID wird mit der [**HttpCreateServerSession-Funktion**](/windows/desktop/api/Http/nf-http-httpcreateserversession) erstellt und im Aufruf von [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)verwendet. Der *pPropertyInformation-Parameter* verweist auf die Konfigurationsstruktur für den festgelegten Eigenschaftentyp. Der *Parameter PropertyInformationLength* gibt die Größe der Konfigurationsstruktur in Bytes an. Wenn Sie beispielsweise **httpServerTimeoutsProperty** festlegen, muss der **pPropertyInformation-Parameter** auf einen Puffer zeigen, der mindestens die Größe der [**HTTP \_ TIMEOUT \_ LIMIT \_ INFO-Struktur**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) aufweist.

In der Regel erstellt eine HTTP-Anwendung eine einzelne Serversitzung und kann anwendungsweite Eigenschaften festlegen, z. B. das globale Bandbreiteneinschränkungslimit oder die zentralisierte Protokollierung für diese Serversitzung aktivieren. [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) überschreibt die HTTP-Server-API-Konfigurationen für die aufrufende Anwendung. Sie wirkt sich nicht auf die HTTP-Server-API-weiten Eigenschaften aus. Die Serversitzungskonfigurationen werden durch Aufrufen von [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)abgefragt.

 

 




