---
description: Die Callcenter-Schnittstellen stellen Methoden bereit, die Aufrufe in einer Warteschlange Anreihen und innerhalb eines Callcenter verteilen.
ms.assetid: 0b9a455d-a614-4698-90ab-e81f020fad3e
title: Kurz Referenz für Callcenter-Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbfc34f1f30fc1f06d543cb7d5fa811517040523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350251"
---
# <a name="call-center-controls-quick-reference"></a>Kurz Referenz für Callcenter-Steuerelemente

Die Callcenter-Schnittstellen stellen Methoden bereit, die Aufrufe in einer Warteschlange Anreihen und innerhalb eines Callcenter verteilen. TAPI 3. x definiert fünf Haupt-Callcenter-Objekte: acdgroup, Agent, Agenthandler, agentsession und Queue. Alle diese Objekte können so erweitert werden, dass Sie Implementierungs spezifische Methoden bereitstellen. Darüber hinaus stellt die [**ittapicallcenter**](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter) -Schnittstelle für das TAPI-Objektmethoden zum Auflisten von Agenthandler-Objekten bereit.



| Callcenter-Schnittstelle                              | BESCHREIBUNG                                                              |
|----------------------------------------------------|--------------------------------------------------------------------------|
| [**Itacdgroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup)                   | Ruft Informationen zu Name und Warteschlange für eine ACD-Gruppe ab.                        |
| [**Itacdgrouetvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroupevent)         | Ruft die Beschreibung der ACD-Gruppen Ereignisse ab.                                    |
| [**Itagent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent)                         | Stellt Methoden bereit, mit denen Informationen zu einem Agent festgelegt und angezeigt werden.         |
| [**Itagentevent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentevent)               | Benachrichtigungs Schnittstelle für [**itagent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent).                   |
| [**Itagenthandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler)           | Stellt Methoden zum Erstellen von agentobjekten und zum Aufzählen von ACD-Gruppen bereit.       |
| [**Itagenthandlerevent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandlerevent) | Ruft die Beschreibung der Agenthandler-Ereignisse ab.                                 |
| [**Itagentsession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession)           | Stellt Methoden bereit, um Informationen zu einer Agentsitzung festzulegen und zu erhalten. |
| [**Itagentsessionevent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsessionevent) | Benachrichtigungs Schnittstelle für " [**itagentsession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession)".     |
| [**Itqueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue)                         | Ruft Informationen zu einer Warteschlange ab und legt Sie fest.                            |
| [**Itqueueevent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueueevent)               | Ruft Informationen zu einem Warteschlangen Ereignis ab.                               |
| [**Ienumacdgroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumacdgroup)             | Listet [**itacdgroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup)auf.                             |
| [**Ienumagent**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagent)                   | Listet den [**itagent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent)auf.                                   |
| [**Ienumagenthandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagenthandler)     | Listet [**itagenthandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler)auf.                     |
| [**Ienumagentsession**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagentsession)     | Listet [**itagentsession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession)auf.                     |
| [**Ienumqueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumqueue)                   | Listet [**itqueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue)auf.                                   |



 

Die folgenden Schnittstellen zählen TAPI 3. x-Elemente gemäß com-Standards auf. Diese Schnittstellen bilden eigenständige Objekte und werden auch mit den zugehörigen Objekten zusammengefasst.



| Enumeratorschnittstelle                           | BESCHREIBUNG                                          |
|------------------------------------------------|------------------------------------------------------|
| [**Ienumacdgroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumacdgroup)         | Listet [**itacdgroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup)auf.         |
| [**Ienumagent**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagent)               | Listet den [**itagent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent)auf.               |
| [**Ienumagenthandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagenthandler) | Listet [**itagenthandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler)auf. |
| [**Ienumagentsession**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagentsession) | Listet [**itagentsession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession)auf. |
| [**Ienumqueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumqueue)               | Listet [**itqueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue)auf.               |



 

Die Ereignis-(Benachrichtigungs-) Schnittstellen ermöglichen es einer TAPI 3. x-Anwendung, auf asynchrone Ereignisse zu reagieren. Sie müssen die Ereignis [**\_ Filter-Methode ittapi::p UT**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) und eine Ereignis Filtermaske festlegen, um den Empfang von Anforderungs Ereignissen zu aktivieren. Wenn Sie **ittapi::p UT \_ EventFilter** nicht anrufen, empfängt Ihre Anwendung keine Ereignisse.



| Ereignis Schnittstelle                                    | BESCHREIBUNG                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------|
| [**Itacdgrouetvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroupevent)         | Ruft die Beschreibung der Gruppen Ereignisse für die automatische Ereignis Verteilung (ACD) ab. |
| [**Itagentevent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentevent)               | Ruft die Beschreibung der Agentereignisse ab.                                   |
| [**Itagenthandlerevent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandlerevent) | Ruft die Beschreibung der agenthandlerereignisse ab.                           |
| [**Itagentsessionevent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsessionevent) | Ruft die Beschreibung der agentsitzungsereignisse ab.                           |



 

 

 
