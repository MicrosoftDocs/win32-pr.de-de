---
description: Die Gerätesteuerung auf Endbenutzer- oder Serveranwendungsebene erfordert einen relativ kleinen Satz grundlegender Informationen.
ms.assetid: 9c787656-93ef-4e0b-9516-8822ae49a83a
title: Gerätesteuerung (Telefonie-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f67b33cb03b5a4ac84309bd9c463a9d73e1ebfb8bf51deb4189585f9e1ec3752
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118867402"
---
# <a name="device-control-telephony-api"></a>Gerätesteuerung (Telefonie-API)

Die Gerätesteuerung auf Endbenutzer- oder Serveranwendungsebene erfordert einen relativ kleinen Satz grundlegender Informationen. Die Abstraktionsschicht des Dienstanbieters führt eine detaillierte Gerätesteuerung durch. Die Dienstanbieter melden erforderliche Geräteinformationen über TAPI an eine Anwendung.

Zu den wichtigsten Gerätekategorien gehören:

-   [Netzwerk:](network-ovr.md)Die Transportschicht für die Kommunikation. Aus Sicht einer Anwendung werden Informationen über das Netzwerk in der Regel in den Adresstyp eingebettet, z. B. LINEADDRESSTYPE \_ PHONENUMBER.
-   [Zeile:](line-ovr.md)Eine Verbindung mit einem Netzwerk. Dieses Konzept wird in TAPI 2.2 (TAPI/C) stark verwendet.
-   [Channel:](channel-ovr.md)Eine Untereinheit einer Zeile. Die Kenntnis von Kanälen ist für eine Anwendung normalerweise nicht erforderlich, da der Dienstanbieter konfiguriert, wie sie als Adressen angezeigt werden.
-   [Adresse:](address-ovr.md)Eine Netzwerkadresse in einem Netzwerk. Jeder Zeile oder jedem Kanal ist mindestens eine Adresse zugeordnet. Die Adresse ist ein wichtiges Konzept sowohl in TAPI 3.1 (TAPI/COM) als auch in TAPI 2.2 (TAPI/C).
-   [Terminal:](terminal-ovr.md)Eine Quelle oder ein Renderer für eine bestimmte Adresse und einen bestimmten Medientyp.

Die Dienstanbieter melden TAPI gerätemerkmale als Reaktion auf Anwendungsabfragen. Dienstanbieter initiieren auch Berichte zu Änderungen im Gerätezustand. Diese Änderungen werden dann basierend auf den während der Initialisierung angeforderten Benachrichtigungen an eine Anwendung gemeldet.

Grundlegende Gerätemerkmale sind:

-   [Device-Klasse](device-class-ovr.md)
-   [Gerätebezeichner](device-identifier-ovr.md)
-   [Adresstyp](address-type-ovr.md)
-   [Adressbezeichner](address-identifier-ovr.md)
-   [Geräteereignisse](device-events-ovr.md)
-   [Medientyp](media-type-ovr.md)
-   [Terminaltyp](terminal-type-ovr.md)

Darüber hinaus stellen die Dienstanbieter Informationen zur Kapazität einer bestimmten Adresse bereit, um verschiedene Sitzungsvorgänge auszuführen.

Zusätzliche Merkmale können bestimmten Geräten zugeordnet werden, wenn sie von den Dienstanbietern unterstützt werden. Eine TAPI 2.x-Anwendung ermittelt Funktionen mithilfe der Funktionen [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) und [**lineGetAddressCaps.**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) TAPI 3.x-Anwendungen verwenden zu diesem Zweck die [**ITAddressCapabilities-Schnittstelle.**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities)

TAPI 2.x bietet eine spezielle Reihe von zusätzlichen Vorgängen, die der Dienstanbieter für die Verwendung mit Telefongeräten implementieren kann. Weitere Informationen finden Sie [unter Telefon Devices](./opening-and-closing-phone-devices.md).

Erweiterte Funktionen sind anbieterspezifisch und werden nicht direkt von der Microsoft-Telefonie-API abgedeckt. Weitere Informationen finden Sie unter [Funktionen für erweiterte Linien,](./extended-line-functions.md) [erweiterte Telefonie Telefon Funktionen](./extended-telephony-phone-functions.md)oder [anbieterspezifische Schnittstellen.](provider-specific-interfaces.md)

Im Folgenden finden Sie eine Zusammenfassung der TAPI-Vorgänge, die Dienstanbieter nach Gerätemerkmalen abfragen und Daten zum aktuellen Zustand bereitstellen.



| TAPI 2.x-Funktionen                                                  | Beschreibung                                                                                                    |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)                   | Fragt ein angegebenes Liniengerät ab, um die Telefoniefunktionen der zugeordneten Adressen zu bestimmen.               |
| [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps)           | Fragt ein angegebenes Liniengerät ab, um die Telefoniefunktionen einer bestimmten Adresse zu bestimmen.                   |
| [**lineGetDevConfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig)               | Gibt eine "nicht transparente" Datenstruktur zurück, in der die aktuelle Konfiguration eines Geräts gespeichert wird.                          |
| [**lineSetDevConfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig)               | Stellt die Gerätekonfiguration wieder her.                                                                                 |
| [**lineConfigDialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog)               | Zeigt ein Dialogfeld an, in dem der Benutzer Parameter konfigurieren kann, die sich auf das Gerät beziehen.                       |
| [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid)                             | Ruft einen stabilen Gerätebezeichner ab, der in weiteren TAPI-Funktionsaufrufen oder mit einer anderen API verwendet werden kann. |
| [**lineGetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus)       | Fragt das Gerät nach dem aktuellen Status ab, z. B. nach der Anzahl aktiver Aufrufe.                                             |
| [**lineSetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linesetlinedevstatus)       | Legt den Gerätestatus fest, z. B. das Festlegen eines Geräts als nicht im Dienst.                                                |
| [**lineGetIcon**](/windows/win32/api/tapi/nf-tapi-linegeticon)                         | Ruft ein anbieterspezifisches Symbol für die Anzeige für den Benutzer ab.                                                      |
| [**lineNegotiateExtVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateextversion) | Ermöglicht es einer Anwendung, eine Erweiterungsversion auszuhandeln, die mit dem angegebenen Zeilengerät verwendet werden soll.                 |
| [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific)                 | Gewährt Zugriff auf gerätespezifische Features.                                                                      |
| [**lineDevSpecificFeature**](/windows/win32/api/tapi/nf-tapi-linedevspecificfeature)   | Sendet gerätespezifische Features an den Dienstanbieter.                                                        |



 



| TAPI 3.x-Schnittstellen oder -Methoden                                   | Beschreibung                                                                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities)           | Ruft Informationen zu den Funktionen einer Adresse ab.                                                  |
| [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat)                       | Legt directShow™ Medienformat fest und ruft es ab.                                                                 |
| [**ITBasicAudioTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasicaudioterminal)             | Legt Standardmerkmale des Audioterminals fest, z. B. Lautstärke, und ruft diese ab.                                  |
| [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                         | Ruft Informationen zu den Medienunterstützungsfunktionen einer Adresse ab.                                    |
| [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                                 | Basisschnittstelle für das Terminalobjekt. Ruft Informationen wie Terminalklasse und unterstützte Medien ab. |
| [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)                   | Ruft Informationen zu verfügbaren Terminals ab und erstellt zusätzliche Terminals.                               |
| [Anbieterspezifische Schnittstellen](provider-specific-interfaces.md) | Dienstanbieterabhängig.                                                                             |



 

 

 
