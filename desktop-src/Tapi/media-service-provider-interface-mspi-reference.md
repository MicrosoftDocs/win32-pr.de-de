---
description: Dieses Dokument beschreibt die Schnittstellen, die Methoden bereitstellen, die einem MSP ermöglichen, mit der Microsoft-Telefonieumgebung zu interagieren und eine TAPI 3-Anwendung für die Verwendung von MSPs-mediensteuer Elementen zuzulassen.
ms.assetid: e67d4941-ce0f-48b9-8099-b62659ad33e0
title: Referenz zur Media Service Provider Interface (MSPi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a30b961fff4d8a9e50fb35573633cc2dc06e370c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106349770"
---
# <a name="media-service-provider-interface-mspi-reference"></a>Referenz zur Media Service Provider Interface (MSPi)

Dieses Dokument beschreibt die Schnittstellen, die Methoden bereitstellen, die einem MSP ermöglichen, mit der Microsoft-Telefonieumgebung zu interagieren und eine TAPI 3-Anwendung die Verwendung der Media-Steuerelemente eines MSP zuzulassen.



| Schnittstellen für Media Services-Anbieter Schnittstellen      | BESCHREIBUNG                                                                                                                                                                            | Erforderlich? |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [**Itmspaddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)             | Nur für TAPI verfügbar gemacht. Haupt-MSP-Schnittstelle für die TAPI-dll. TAPI 3 ruft **cokreateinstance** für diese Schnittstelle auf, um das MSP-Objekt zu erstellen.                                               | Ja       |
| [**Itstream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)                     | Verfügbar für Anwendungen. Stellt Methoden bereit, die es einer Anwendung ermöglichen, Informationen zu einem Stream abzurufen, zu starten, anzuhalten oder zu beenden und um Terminals in einem Stream auszuwählen oder deren Auswahl aufzuheben. | Ja       |
| [**Itstreamcontrol**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)       | Verfügbar für Anwendungen. Stellt Methoden bereit, die es einer Anwendung ermöglichen, Streams zu erstellen oder zu entfernen.                                                                                       | Ja       |
| [**Ienumstream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)               | Verfügbar für Anwendungen. Enumeratorschnittstelle für [**itstream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).                                                                                                        | Ja       |
| [**Itsubstream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)               | Verfügbar für Anwendungen. Stellt Methoden bereit, die es einer Anwendung ermöglichen, Informationen in einem substream abzurufen, zu starten, anzuhalten oder zu beenden und um Terminals auszuwählen oder deren Auswahl aufzuheben.          | Optional  |
| [**Itsubstreamcontrol**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) | Verfügbar für Anwendungen. Stellt Methoden bereit, die es einer Anwendung ermöglichen, unter Ströme zu erstellen oder zu entfernen.                                                                                    | Optional  |
| [**Ienumsubstream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumsubstream)         | Verfügbar für Anwendungen. Enumeratorschnittstelle für [**itsubstream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream).                                                                                                  | Optional  |
| [**Itterminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                 | Verfügbar für Anwendungen. Ruft Informationen zum [Terminal Objekt](terminal-object.md)ab, z. b. zum Terminal-und unterstützten Medien.                                                    | Ja       |
| [**Itterminalsupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)   | Verfügbar für Anwendungen. Bietet Methoden zum Abfragen von verfügbaren Terminals und zum Erstellen zusätzlicher Terminals.                                                                             | Ja       |
| [**ITTerminalSupport2**](/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport2) | Verfügbar für Anwendungen. Ruft Informationen über austauschbare Terminal Klassen und übergeordnete Klassen ab. wird von der [**itterminalsupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) -Schnittstelle abgeleitet.           | Ja       |



 

## <a name="media-service-provider-interface-types"></a>Media Service Provider-Schnittstellentypen

-   [**MSP- \_ Adress \_ Ereignis**](/windows/win32/api/msp/ne-msp-msp_address_event)
-   [**MSP- \_ Rückruf \_ Ereignis**](/windows/win32/api/msp/ne-msp-msp_call_event)
-   [**MSP- \_ Ereignis**](/windows/win32/api/msp/ne-msp-msp_event)
-   [**MSP- \_ Ereignis \_ Informationen**](/windows/win32/api/msp/ns-msp-msp_event_info)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Service Provider Interface (MSPi)](media-service-provider-interface-mspi-.md)
</dt> </dl>

 

 
