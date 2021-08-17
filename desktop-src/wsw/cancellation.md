---
title: Abbruch
description: Die meisten Vorgänge in der WWSAPI können während der Ausführung abgebrochen werden.
ms.assetid: d73d76e1-bd78-40ce-9f92-e282b6b127ce
keywords:
- Abbrechen von Webdiensten für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf75bd8d07d8f78ddf0a5750e6f4f96feb073dc15b8e63ed23ab8ceb061de145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841780"
---
# <a name="cancellation"></a>Abbruch

Die meisten Vorgänge in der WWSAPI können während der Ausführung abgebrochen werden.

Welche Funktion Sie zum Abbrechen eines Vorgangs verwenden, hängt vom betroffenen Objekt ab.

| Funktion                                           | Beschreibung                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)           | Bricht alle ausstehenden Eingaben und Ausgaben für einen angegebenen Kanal ab und legt den Kanalzustand auf WS \_ CHANNEL \_ STATE \_ FAULTED fest. |
| [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)         | Bricht alle ausstehenden Eingaben und Ausgaben für einen angegebenen Listener ab.                                                          |
| [**WsAbortServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy) | Bricht alle ausstehenden Eingaben und Ausgaben für einen angegebenen Dienstproxy ab.                                                     |
| [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)   | Unterbricht und beendet aktuelle Vorgänge auf dem Diensthost.                                                    |
| [**WsAboanCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)             | Verbricht einen Aufruf, einen angegebenen Aufruf eines angegebenen Dienstproxys.                                                        |



 

Informationen zu Abbruchen, die sich auf [serverseitige Dienstvorgänge](server-side-service-operations.md) und Dienstmodellrückrufe auswirken, finden Sie unter [Aufrufabbruch.](call-cancellation.md)


 

 




