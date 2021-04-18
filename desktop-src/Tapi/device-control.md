---
description: Für die Gerätesteuerung auf Endbenutzer-oder Server Anwendungsebene ist ein relativ kleiner Satz grundlegender Informationen erforderlich.
ms.assetid: 9c787656-93ef-4e0b-9516-8822ae49a83a
title: Gerätesteuerung (telefonieapi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b17336941a55a529c6b436270f7b225a1cada3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343685"
---
# <a name="device-control-telephony-api"></a>Gerätesteuerung (telefonieapi)

Für die Gerätesteuerung auf Endbenutzer-oder Server Anwendungsebene ist ein relativ kleiner Satz grundlegender Informationen erforderlich. Die Abstraktions Ebene des Dienstanbieters führt ein detailliertes Geräte Steuerelement aus. Die Dienstanbieter melden erforderliche Geräteinformationen über TAPI an eine Anwendung.

Zu den wichtigsten Gerätekategorien gehören:

-   [Netzwerk](network-ovr.md): die Transportschicht für die Kommunikation. Aus Sicht der Anwendung werden Informationen über das Netzwerk in der Regel in den Adresstyp eingebettet, z. b. lineadresssstype \_ PhoneNumber.
-   [Line](line-ovr.md): eine Verbindung mit einem Netzwerk. Dieses Konzept wird stark in TAPI 2,2 (TAPI/C) verwendet.
-   [Channel](channel-ovr.md): eine Unterteilung einer Zeile. Das Wissen von Kanälen ist in der Regel nicht erforderlich, da der Dienstanbieter konfiguriert, wie Sie als Adressen angezeigt werden.
-   [Adresse](address-ovr.md): ein Netzwerk Speicherort in einem Netzwerk. Jede Zeile oder jeder Kanal weist mindestens eine zugeordnete Adresse auf. Die Adresse ist ein wichtiges Konzept in TAPI 3,1 (TAPI/com) und TAPI 2,2 (TAPI/C).
-   [Terminal](terminal-ovr.md): eine Quelle oder ein Renderer für eine bestimmte Adresse und einen Medientyp.

Die Dienstanbieter melden Gerätemerkmale als Reaktion auf Anwendungs Abfragen an TAPI. Dienstanbieter initiieren auch Berichte zu Änderungen im Gerätezustand. Diese Änderungen werden dann an eine Anwendung basierend auf den während der Initialisierung angeforderten Benachrichtigungen gemeldet.

Grundlegende Gerätemerkmale:

-   [Geräteklasse](device-class-ovr.md)
-   [Geräte Bezeichner](device-identifier-ovr.md)
-   [Adresstyp](address-type-ovr.md)
-   [Adress Bezeichner](address-identifier-ovr.md)
-   [Geräte Ereignisse](device-events-ovr.md)
-   [Medientyp](media-type-ovr.md)
-   [Terminaltyp](terminal-type-ovr.md)

Außerdem stellen die Dienstanbieter Informationen über die Kapazität einer bestimmten Adresse bereit, um verschiedene Sitzungs Vorgänge auszuführen.

Zusätzliche Merkmale können bestimmten Geräten zugeordnet werden, wenn Sie von den Dienstanbietern unterstützt werden. Eine TAPI 2. x-Anwendung ermittelt Funktionen mithilfe der Funktionen [**linegetdevcaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) und [**linegetaddresscaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) . TAPI 3. x-Anwendungen verwenden zu diesem Zweck die [**itaddressfunktionalitäten**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) -Schnittstelle.

TAPI 2. x bietet einen speziellen Satz zusätzlicher Vorgänge, die der Dienstanbieter für die Verwendung mit Telefongeräten implementieren kann. Siehe [Telefongeräte](./opening-and-closing-phone-devices.md).

Erweiterte Funktionen sind Anbieter spezifisch und werden nicht direkt von der Microsoft-telefonieapi abgedeckt. Weitere Informationen finden Sie unter [Erweiterte Zeilen Funktionen](./extended-line-functions.md), [Erweiterte Telefoniefunktionen](./extended-telephony-phone-functions.md)oder [anbieterspezifische Schnittstellen](provider-specific-interfaces.md).

Im folgenden finden Sie eine Zusammenfassung der TAPI-Vorgänge, mit denen Dienstanbieter auf Geräteeigenschaften abgefragt und Daten im aktuellen Zustand bereitgestellt werden



| TAPI 2. x-Funktionen                                                  | BESCHREIBUNG                                                                                                    |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**linegetdevcaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)                   | Fragt ein angegebenes Zeilen Gerät ab, um die Telefoniefunktionen der zugeordneten Adressen zu ermitteln               |
| [**linegetaddresscaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps)           | Fragt ein angegebenes Zeilen Gerät ab, um die Telefoniefunktionen einer bestimmten Adresse zu bestimmen.                   |
| [**linegetdevconfig**](/windows/win32/api/tapi/nf-tapi-linegetdevconfig)               | Gibt eine "nicht transparente" Datenstruktur zurück, in der die aktuelle Konfiguration eines Geräts gespeichert wird.                          |
| [**linesetdevconfig**](/windows/win32/api/tapi/nf-tapi-linesetdevconfig)               | Stellt die Gerätekonfiguration wieder her.                                                                                 |
| [**lineconfigdialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog)               | Zeigt ein Dialogfeld an, in dem der Benutzer die auf dem Gerät bezogenen Parameter konfigurieren kann.                       |
| [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid)                             | Ruft einen stabilen Geräte Bezeichner ab, der in weiteren TAPI-Funktionsaufrufen oder mit einer anderen API verwendet werden kann. |
| [**linegetlinedevstatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus)       | Fragt das Gerät nach dem aktuellen Status ab, z. b. die Anzahl aktiver Aufrufe.                                             |
| [**linesetlinedevstatus**](/windows/win32/api/tapi/nf-tapi-linesetlinedevstatus)       | Legt den Gerätestatus fest, z. b. das Festlegen eines Geräts als nicht im Dienst.                                                |
| [**linegeticon**](/windows/win32/api/tapi/nf-tapi-linegeticon)                         | Ruft das anbieterspezifische Symbol für die Anzeige für den Benutzer ab.                                                      |
| [**linenegotiateextversion**](/windows/win32/api/tapi/nf-tapi-linenegotiateextversion) | Ermöglicht einer Anwendung das Aushandeln einer Erweiterungs Version, die mit dem angegebenen Zeilen Gerät verwendet werden soll.                 |
| [**linedevspecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific)                 | Ermöglicht den Zugriff auf gerätespezifische Features.                                                                      |
| [**linedevspecificfeature**](/windows/win32/api/tapi/nf-tapi-linedevspecificfeature)   | Sendet gerätespezifische Funktionen an den Dienstanbieter.                                                        |



 



| TAPI 3. x-Schnittstellen oder-Methoden                                   | BESCHREIBUNG                                                                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [**Itaddress-Funktionen**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities)           | Ruft Informationen zu den Funktionen einer Adresse ab.                                                  |
| [**Itammediaformat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat)                       | Legt das DirectShow-™ Medienformat fest und ruft es ab.                                                                 |
| [**Itbasicaudioterminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasicaudioterminal)             | Legt standardmäßige audioterminalmerkmale fest, z. b. Volume.                                  |
| [**Itmediasupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                         | Ruft Informationen zu den Medien Unterstützungsfunktionen einer Adresse ab.                                    |
| [**Itterminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                                 | Basisschnittstelle für das Terminal Objekt. Ruft Informationen wie die Terminal Klasse und die unterstützten Medien ab. |
| [**Itterminalsupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)                   | Ruft Informationen zu verfügbaren Terminals ab und erstellt zusätzliche Terminals.                               |
| [Anbieterspezifische Schnittstellen](provider-specific-interfaces.md) | Der Dienstanbieter ist abhängig.                                                                             |



 

 

 
