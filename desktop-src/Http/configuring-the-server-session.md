---
title: Konfigurieren der Server Sitzung
description: .
ms.assetid: 1e4e9440-8d70-44df-90a7-2d5e25b2f680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcf069b22992fa178798c7f28545e30217d0dada
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340411"
---
# <a name="configuring-the-server-session"></a>Konfigurieren der Server Sitzung

Die Server Sitzungs-ID wird mit der [**httpkreateserversession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) -Funktion erstellt und im [**httpsetserversessionproperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)-Befehl verwendet. Der *ppropertyinformation* -Parameter verweist auf die Konfigurations Struktur für den Eigenschaftentyp, der festgelegt wird. Der *propertyinformationlength* -Parameter gibt die Größe der Konfigurations Struktur in Bytes an. Wenn Sie z. b. **httpservertimeoutsproperty** festlegen, muss der **ppropertyinformation** -Parameter auf einen Puffer verweisen, der mindestens die Größe der Informationsstruktur für das [**http- \_ Timeout \_ Limit \_**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) hat.

In der Regel erstellt eine HTTP-Anwendung eine einzelne Server Sitzung und kann Anwendungs weite Eigenschaften festlegen, wie z. b. das Limit für die globale Bandbreitendrosselung oder die zentralisierte Protokollierung für diese Server Sitzung. [**Httpsetserversessionproperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) überschreibt die HTTP-Server-API-Konfigurationen für die aufrufende Anwendung. Dies hat keine Auswirkung auf die API-weiten http-Server-Eigenschaften. Die Server Sitzungs Konfigurationen werden durch Aufrufen von " [**httpqueryserversessionproperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)" abgefragt.

 

 




