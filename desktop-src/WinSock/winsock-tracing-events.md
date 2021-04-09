---
description: Details der Winsock-Ablauf Verfolgungs Ereignisse.
ms.assetid: 246AE0BE-E8E2-4291-8BF4-577F889F055B
title: Winsock-Ablauf Verfolgungs Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeabd2d06741f8dfa1f47b513a09c941ee1490b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129104"
---
# <a name="winsock-tracing-events"></a>Winsock-Ablauf Verfolgungs Ereignisse

In diesem Abschnitt werden ausführliche Informationen zu bestimmten Details der Winsock-Ablauf Verfolgungs Ereignisse beschrieben.

Die Winsock-Ablauf Verfolgung ist ein Feature zur Problembehandlung, das in Binärdateien im Einzelhandel aktiviert werden kann, um bestimmte Windows Socket-Ereignisse mit minimalem mehr Aufwand Diese Funktion ermöglicht bessere Diagnosefunktionen für Entwickler und den Produktsupport. Die Winsock-Netzwerk Ereignis Ablauf Verfolgung unterstützt Ablaufverfolgungs-Socketvorgänge für IPv4-und IPv6 Die Ablauf Verfolgung der Winsock-Katalog Änderung unterstützt die Ablauf Verfolgung von Änderungen, die an den Winsock-Katalog durch mehrstufige Dienstanbieter (LSPs

> [!Note]  
> Mehrstufige Dienstanbieter sind veraltet. Ab Windows 8 und Windows Server 2012 verwenden Sie die [Windows-Filter Plattform](../fwp/windows-filtering-platform-start-page.md).

 

Die Winsock-Ablauf Verfolgung verwendet die Ereignis Ablauf Verfolgung für Windows (Event Tracing for Windows, etw), eine allgemeine, hoch Geschwindigkeits Ablauf Verfolgungs Funktion des Betriebssystems. Etw bietet einen Ablauf Verfolgungs Mechanismus für Ereignisse, die von Anwendungen im Benutzermodus und im Kernel Modus-Gerätetreibern ausgelöst werden. Etw kann die Protokollierung dynamisch aktivieren und deaktivieren, sodass eine ausführliche Ablauf Verfolgung in Produktionsumgebungen ohne Neustarts oder Anwendungs Neustarts problemlos durchgeführt werden kann. Unterstützung für die Winsock-Ablauf Verfolgung mit etw wurde unter Windows Vista und höher hinzugefügt. Allgemeine Informationen zu etw finden Sie unter verbessertes [Debugging und Leistungsoptimierung mit etw](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).

In der folgenden Liste finden Sie ausführliche Informationen zu den einzelnen Winsock-Ablauf Verfolgungs Ereignissen. Klicken Sie auf den Ereignis Namen, um weitere Informationen zu einem beliebigen Ereignis zu erhalten.



| Veranstaltungsname                                                            | BESCHREIBUNG                                                                               |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**AFD- \_ Ereignis \_ Erstellung**](afd-event-create.md)                        | Winsock-Netzwerk Ablauf Verfolgungs Ereignis für einen Socket-Erstellungs Vorgang.                            |
| [**AFD- \_ Ereignis \_ Schließen**](afd-event-close.md)                          | Winsock-Netzwerkablaufverfolgungs-Ereignis für SocketClose.                                 |
| [**Winsock \_ WS2HELP \_ LSP- \_ Installation**](winsock-ws2help-lsp-install.md) | Änderungs Ereignis für den Winsock-Katalog für einen mehrstufigen Dienstanbieter (LSP). |
| [**Winsock \_ WS2HELP \_ LSP \_ Entfernen**](winsock-ws2help-lsp-remove.md)   | Änderungs Ereignis für den Winsock-Katalog für einen mehrstufigen Dienstanbieter (LSP).      |
| [**Winsock \_ WS2HELP \_ LSP \_ Deaktivieren**](winsock-ws2help-lsp-disable.md) | Änderungs Ereignis für den Winsock-Katalog für einen mehrstufigen Dienstanbieter (LSP).      |
| [**Winsock \_ WS2HELP \_ LSP \_ Reset**](winsock-ws2help-lsp-reset.md)     | Das Änderungs Ereignis für den Winsock-Katalog für einen Winsock-Katalog Zurücksetzungs Vorgang.                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbessertes Debugging und Leistungsoptimierung mit ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[Winsock-Ablauf Verfolgung](winsock-tracing.md)
</dt> <dt>

[Winsock-Ablauf Verfolgungs Ebenen](winsock-tracing-levels.md)
</dt> <dt>

[Kontrolle über die Winsock-Ablauf Verfolgung](control-of-winsock-tracing.md)
</dt> <dt>

[Details der Winsock-Netzwerk Ereignis Ablauf Verfolgung](winsock-tracing-event-details.md)
</dt> <dt>

[Details zur Änderung der Winsock-Katalog Änderung](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
