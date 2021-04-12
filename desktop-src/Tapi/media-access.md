---
description: Die Medien Features unterscheiden sich gegenüber TAPI 2,2 (TAPI/C) im Gegensatz zu TAPI 3 (com), größtenteils weil die com-API Zugriff auf Media Service Providers (MSPs) hat.
ms.assetid: 73042eb1-b2d6-4dcb-b40e-f8f3933dcdb0
title: Medienzugriff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bb3fe361aab9d5b5c9897deb5ea36d6e85adcfd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104219008"
---
# <a name="media-access"></a>Medienzugriff

Die Medien Features unterscheiden sich gegenüber TAPI 2,2 (TAPI/C) im Gegensatz zu TAPI 3 (com), größtenteils weil die com-API Zugriff auf Media Service Providers (MSPs) hat. Weitere Informationen zu MSPs finden Sie unter [Informationen zum Media Service Provider (MSP)](./about-the-media-service-provider-msp-.md). Weitere Informationen zu Medienstrom Vorgängen finden Sie unter [Mediensteuerung](./device-control.md).

Die zwei wichtigsten Konzepte für eine Anwendung sind der Medientyp (oder der Modus) und der Stream. Der Typ ist die Form, in der Daten übertragen werden. Weitere Informationen und eine Liste von TAPI-definierten Typen finden Sie unter [linemediamode- \_ Konstanten](linemediamode--constants.md). Der Mediendaten Strom ist der tatsächliche Datenstrom. Ein MSP kann direkten Zugriff auf den Stream bereitstellen. TAPI 2,2-Anwendungen haben Zugriff, werden jedoch in erster Linie auf andere APIs verwiesen, um solche Steuerelemente zu implementieren.

Diese APIs enthalten die Waveform-API, die comm-API und die Media Control Interface (MCI). Die Waveform-API wird für die Multimedia-Programmierung verwendet. die comm-API ist der Satz von Kommunikationsfunktionen, die vom Platform Software Development Kit (SDK) bereitgestellt werden, und MCI bietet eine allgemeine generalisierte Schnittstelle zum Steuern von Mediengeräten.

Beispielsweise kann eine Anwendung für Linien Geräte TAPI 2,2 verwenden, um eine Verbindung mit einer anderen Station herzustellen. Nachdem die Verbindung hergestellt wurde, kann die Anwendung die Waveform-API (oder die MCI-waveaudioapi) auf dem zugeordneten Gerät verwenden, um Audiodaten über die Verbindung wiederzugeben (zu senden) und aufzuzeichnen (zu empfangen). Analog dazu verwendet eine Anwendung die Modem Konfigurations Erweiterungen der Communications-API, um den Mediendaten Strom zu steuern, wenn der Verbindungs Mediendaten Strom von einem Modem aus verwendet wird.

Um TAPI 2,2 den Medienstrom Zugriff auf ein Telefon oder einen Anruf an einem Geräte Gerät zu gewährleisten, muss der Dienstanbieter sowohl den telefoniespi als auch den entsprechenden Media Stream SPI oder die Gerätetreiber Schnittstelle (DDI) implementieren. Der Dienstanbieter kann Zeilen und Telefone gleichzeitig unterstützen.

Da diese Geräteklassen und Medienstrom Vorgänge unabhängig voneinander funktionieren, muss die Koordination ihrer Verwendung auf Anwendungsebene erfolgen. Mehrere Anwendungen, die Aufrufe und Mediendaten Ströme gemeinsam nutzen, erfordern wahrscheinlich eine Koordination ihrer Aktivitäten auf Anwendungsebene, um eine widersprüchliche Verwendung von TAPI und der Media Stream-API zu verhindern.

TAPI meldet Änderungen in der Art des Medien Stroms (sprach-, Fax-, Datenmodem usw.) an beteiligte Anwendungen. Dieser Prozess wird manchmal auch als " [*aufrufsklassifizierung*](c-tapgloss.md)" bezeichnet. Der Mechanismus, der zum Bestimmen des Medienstrom Typs verwendet wird, ist spezifisch für den Dienstanbieter. Ein Dienstanbieter kann z. b. den Mediendaten Strom nach Energie oder Tönen filtern, die den Medientyp charakterisieren, oder er kann ein ausgeprägtes Klingeln, in Nachrichten über das Netzwerk ausgetauschte Daten oder Informationen zum Aufrufer oder zum Aufrufen der ID verwenden, um diese Bestimmung zu treffen.

-   [Rückruf Überwachung](call-monitoring.md)
-   [Mediensteuer Element](/previous-versions/windows/desktop/legacy/ms736578(v=vs.85))
-   [Ziffern Erfassung](digit-gathering.md)
-   [Erstellen von Inband-Ziffern und-Tönen](generating-inband-digits-and-tones.md)

 

 
