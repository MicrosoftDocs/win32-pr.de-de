---
title: Abbruch
description: Die meisten Vorgänge in der wwsapi können während der Ausführung abgebrochen werden.
ms.assetid: d73d76e1-bd78-40ce-9f92-e282b6b127ce
keywords:
- Abbrechen von Webdiensten für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e979455e898922dfb7c81381c1f1aafd455274
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316850"
---
# <a name="cancellation"></a>Abbruch

Die meisten Vorgänge in der wwsapi können während der Ausführung abgebrochen werden.

Die Funktion, mit der ein Vorgang abgebrochen wird, hängt vom betroffenen Objekt ab.

| Funktion                                           | BESCHREIBUNG                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**Wsabortchannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)           | Bricht alle ausstehenden Eingaben und Ausgaben für einen angegebenen Kanal ab und legt den Kanal Zustand auf den WS- \_ Kanalstatus Fehler fest \_ \_ . |
| [**Wsabortlistener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)         | Bricht alle ausstehenden Eingaben und Ausgaben für einen angegebenen Listener ab.                                                          |
| [**Wsabortserviceproxy**](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy) | Bricht alle ausstehenden Eingaben und Ausgaben für einen angegebenen Dienst Proxy ab.                                                     |
| [**Wsabortservicehost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)   | Unterbricht und beendet die aktuellen Vorgänge auf dem Dienst Host.                                                    |
| [**Wsabandoncall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)             | Bricht einen-Befehl ab, einen angegebenen-Rückruf für einen angegebenen Dienst Proxy.                                                        |



 

Informationen zu Stornierungen, die [serverseitige Dienst Vorgänge](server-side-service-operations.md) und Dienstmodell Rückrufe betreffen, finden Sie unter [Aufruf Abbruch](call-cancellation.md).


 

 




