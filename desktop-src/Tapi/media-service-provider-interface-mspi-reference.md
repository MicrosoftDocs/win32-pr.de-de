---
description: In diesem Dokument werden die Schnittstellen beschrieben, die Methoden bereitstellen, die es einem MSP ermöglichen, mit der Microsoft-Telefonieumgebung zu interagieren und einer TAPI 3-Anwendung die Verwendung von MSPs-Mediensteuerelementen zu ermöglichen.
ms.assetid: e67d4941-ce0f-48b9-8099-b62659ad33e0
title: Referenz zur Media Service Provider Interface (MSPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94ce02312a7c94a7bc2b805a6c73c263546d9cb3f21bbe795d92a91b1010a0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404750"
---
# <a name="media-service-provider-interface-mspi-reference"></a>Referenz zur Media Service Provider Interface (MSPI)

In diesem Dokument werden die Schnittstellen beschrieben, die Methoden bereitstellen, die es einem MSP ermöglichen, mit der Microsoft-Telefonieumgebung zu interagieren und einer TAPI 3-Anwendung die Mediensteuerelemente eines MSP zu verwenden.



| Schnittstellen der Media Service Provider-Schnittstelle      | BESCHREIBUNG                                                                                                                                                                            | Erforderlich? |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)             | Nur für TAPI verfügbar gemacht. Haupt-MSP-Schnittstelle für die TAPI-DLL. TAPI 3 ruft **CoCreateInstance** auf dieser Schnittstelle auf, um das MSP-Objekt zu erstellen.                                               | Ja       |
| [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)                     | Für Anwendungen verfügbar gemacht. Stellt Methoden bereit, mit denen eine Anwendung Informationen zu einem Stream abrufen, starten, anhalten oder beenden sowie Terminals in einem Stream auswählen oder deaktivieren kann. | Ja       |
| [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)       | Für Anwendungen verfügbar gemacht. Stellt Methoden bereit, mit denen eine Anwendung Streams erstellen oder entfernen kann.                                                                                       | Ja       |
| [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)               | Für Anwendungen verfügbar gemacht. Enumeratorschnittstelle für [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).                                                                                                        | Ja       |
| [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)               | Für Anwendungen verfügbar gemacht. Stellt Methoden bereit, die einer Anwendung das Abrufen von Informationen in einem Unterstream, das Starten, Anhalten oder Beenden von Informationen sowie das Auswählen oder Aufheben der Auswahl von Terminals ermöglichen.          | Optional  |
| [**ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) | Für Anwendungen verfügbar gemacht. Stellt Methoden bereit, mit denen eine Anwendung Unterstreams erstellen oder entfernen kann.                                                                                    | Optional  |
| [**IEnumSubStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumsubstream)         | Für Anwendungen verfügbar gemacht. Enumeratorschnittstelle für [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream).                                                                                                  | Optional  |
| [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                 | Für Anwendungen verfügbar gemacht. Ruft Informationen zum [Terminalobjekt](terminal-object.md)ab, z. B. Terminalaufruf und unterstützte Medien.                                                    | Ja       |
| [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)   | Für Anwendungen verfügbar gemacht. Stellt Methoden zum Abfragen verfügbarer Terminals und zum Erstellen zusätzlicher Terminals bereit.                                                                             | Ja       |
| [**ITTerminalSupport2**](/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport2) | Für Anwendungen verfügbar gemacht. Ruft Informationen zu austauschbaren Terminalklassen und Übergeordneten Klassen ab. wird von der [**ITTerminalSupport-Schnittstelle**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) abgeleitet.           | Ja       |



 

## <a name="media-service-provider-interface-types"></a>Schnittstellentypen von Media Service Provider

-   [**\_MSP-ADRESSEREIGNIS \_**](/windows/win32/api/msp/ne-msp-msp_address_event)
-   [**\_MSP-AUFRUFEREIGNIS \_**](/windows/win32/api/msp/ne-msp-msp_call_event)
-   [**\_MSP-EREIGNIS**](/windows/win32/api/msp/ne-msp-msp_event)
-   [**\_MSP-EREIGNISINFORMATIONEN \_**](/windows/win32/api/msp/ns-msp-msp_event_info)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Service Provider Interface (MSPI)](media-service-provider-interface-mspi-.md)
</dt> </dl>

 

 
