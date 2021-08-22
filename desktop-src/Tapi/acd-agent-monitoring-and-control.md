---
description: Die Überwachung und Steuerung des ACD-Agent-Status auf Stationen wird über diese Funktionen lineGetAgentCaps lineGetAgentStatus lineGetAgentGroupList lineGetAgentActivityList lineSetAgentGroup lineSetAgentState und lineSetAgentActivity unterstützt.
ms.assetid: 2851fe54-f807-4cef-b6ca-2dcc7e1ae6fb
title: Überwachung und Steuerung des ACD-Agents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8986fc31e8b30e8b32c4b347a26abfa46adbd426c20c506553ae2f41ea879a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118872657"
---
# <a name="acd-agent-monitoring-and-control"></a>Überwachung und Steuerung des ACD-Agents

Die Überwachung und Steuerung des ACD-Agent-Status auf Stationen wird durch die folgenden Funktionen unterstützt: [**lineGetAgentCaps,**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa) [**lineGetAgentStatus,**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) [**lineGetAgentGroupList,**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista) [**lineGetAgentActivityList,**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista) [**lineSetAgentGroup,**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup) [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)und [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity).

Die [**LINE \_ AGENTSTATUS-Meldung**](line-agentstatus.md) wird verwendet, um anzugeben, wann agent-Informationen geändert wurden.

Diese Steuerelemente sind einer Adresse anstelle einer Zeile zugeordnet, da viele ACD-Systeme mit unterschiedlichen ACD-Warteschlangen implementiert werden, die Schaltflächen im Telefonterminal zugeordnet sind (und separate Aufrufe aussehen). Außerdem können ACD-Agent-Telefone häufig separate Anrufanrufe für persönliche Anrufe haben.

Architekturlich sollte die ACD-Funktionalität in einer serverbasierten Anwendung implementiert werden. Die oben erwähnten Clientfunktionen werden anstelle der Zuordnung zum Telefoniedienstanbieter an eine Serveranwendung übermittelt, die (mithilfe einer Option von [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)) als Handler für solche Funktionen registriert wurde. Die [**LINE \_ PROXYREQUEST-Nachricht**](line-proxyrequest.md) wird verwendet, um der Handleranwendung zu signalisieren, wenn eine Anforderung erfolgt ist. Sie ruft die [**lineProxyResponse-Funktion**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) auf, um Ergebnisse und Daten zurück zu geben. Handleranwendungen können bei Bedarf [**auch lineProxyMessage aufrufen,**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) um LINE \_ AGENTSTATUS-Nachrichten zu generieren. Im Fall einer Legacy-PBX- oder eigenständigen ACD, die die ACD-Funktionalität selbst implementiert, muss der Telefoniedienstanbieter für den Switch eine Proxyserveranwendung enthalten, die die Anforderungen akzeptiert und diese (möglicherweise mithilfe von [**lineDevSpecific-Funktionen**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) oder einer privaten Schnittstelle) an den Dienstanbieter weiter leitet, der sie an den Switch weiter leitet.

 

 



