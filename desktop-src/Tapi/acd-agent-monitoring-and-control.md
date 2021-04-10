---
description: 'Die Überwachung und Steuerung des ACD Agent-Status auf Stationen wird durch die folgenden Funktionen unterstützt: linegetagentcaps linegetagentstatus linegetagentgrouplist linegetagentactivitylist linesetagentgroup linesetagentstate und linesetagentactivity.'
ms.assetid: 2851fe54-f807-4cef-b6ca-2dcc7e1ae6fb
title: Überwachung und Steuerung des ACD-Agents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52d3cf9387819bada069920099b19da65e6a1e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042687"
---
# <a name="acd-agent-monitoring-and-control"></a>Überwachung und Steuerung des ACD-Agents

Die Überwachung und Steuerung des ACD Agent-Status auf Stationen wird durch die folgenden Funktionen unterstützt: [**linegetagentcaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa), [**linegetagentstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa), [**linegetagentgrouplist**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista), [**linegetagentactivitylist**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista), [**linesetagentgroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup), [**linesetagentstate**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)und [**linesetagentactivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity).

Die Meldung " [**\_ Agentstatus**](line-agentstatus.md) " wird verwendet, um anzugeben, wann die Agentinformationen geändert wurden.

Diese Steuerelemente sind einer Adresse anstelle einer Zeile zugeordnet, da viele ACD-Systeme mit unterschiedlichen ACD-Warteschlangen implementiert werden, die mit Schaltflächen im Telefon Terminal (und separaten Anruf Darstellungen) verknüpft sind. Außerdem kann es vorkommen, dass ACD-Agent-Telefone für persönliche Anrufe häufig über separate Aufruf Auftritte verfügen.

In architektonischer Sprache sollten die ACD-Funktionen in einer serverbasierten Anwendung implementiert werden. Die oben erwähnten Client Funktionen, anstatt dem Telefoniedienstanbieter zu entsprechen, werden an eine Serveranwendung übermittelt, die (mit der Option [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)) als Handler für solche Funktionen registriert hat. Die [**Zeile \_ proxyrequest**](line-proxyrequest.md) -Nachricht wird verwendet, um an die Handleranwendung zu signalisieren, wenn eine Anforderung gestellt wurde. Sie ruft die [**lineproxyresponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) -Funktion auf, um Ergebnisse und Daten zurückzugeben. Handleranwendungen können auch [**lineproxymess**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) zum Generieren von \_ zeilenagentstatusmeldungen bei Bedarf aufruft. Bei einer Legacy-PBX oder einer eigenständigen Zugriffs Steuerungs Liste, die die ACD-Funktionalität selbst implementiert, muss der Telefoniedienstanbieter für den Switch eine Proxy Serveranwendung enthalten, die die Anforderungen akzeptiert und diese (möglicherweise mithilfe von [**linedevspecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) -Funktionen oder einer privaten Schnittstelle) an den Dienstanbieter weiterleitet, der Sie an den Switch weiterleitet.

 

 



