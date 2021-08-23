---
description: Medienfeatures unterscheiden sich bei TAPI 2.2 (TAPI/C) im Gegensatz zu TAPI 3 (COM), hauptsächlich weil die COM-API Zugriff auf Mediendienstanbieter (Media Service Providers, MSPs) hat.
ms.assetid: 73042eb1-b2d6-4dcb-b40e-f8f3933dcdb0
title: Medienzugriff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f2fc67e18a85718a10a0489656d4b423dd2f9f849a876ea5eec0543017611f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575610"
---
# <a name="media-access"></a>Medienzugriff

Medienfeatures unterscheiden sich bei TAPI 2.2 (TAPI/C) im Gegensatz zu TAPI 3 (COM), hauptsächlich weil die COM-API Zugriff auf Mediendienstanbieter (Media Service Providers, MSPs) hat. Weitere Informationen zu MSPs finden Sie unter [Informationen zum Media Service Provider (MSP).](./about-the-media-service-provider-msp-.md) Weitere Informationen zu Medienstreamvorgängen finden Sie unter [Media Control](./device-control.md).

Die beiden wichtigsten Konzepte für eine Anwendung sind der Medientyp (oder Modus) und der Stream. Der Typ ist das Formular, in dem Daten übertragen werden. Weitere Informationen und eine Liste der TAPI-definierten Typen finden Sie unter [LINEMEDIAMODE-Konstanten. \_ ](linemediamode--constants.md) Der Medienstream ist der tatsächliche Datenstrom. Ein MSP kann direkten Zugriff auf den Stream ermöglichen. TAPI 2.2-Anwendungen haben Zugriff, verweisen aber in erster Linie auf andere APIs, um solche Steuerelemente zu implementieren.

Zu diesen APIs gehören die Waveform-API, die Comm-API und die Media Control Interface (MCI). Die Waveform-API wird für die Multimediaprogrammierung verwendet, die Comm-API ist ein Satz von Kommunikationsfunktionen, die vom Platform Software Development Kit (SDK) bereitgestellt werden, und die MCI bietet eine allgemeine generalisierte Schnittstelle zum Steuern von Mediengeräten.

Beispielsweise kann eine Anwendung für Liniengeräte TAPI 2.2 verwenden, um eine Verbindung mit einer anderen Station herzustellen. Nachdem die Verbindung hergestellt wurde, kann die Anwendung die Waveform-API (oder die MCI Waveaudio-API) auf dem zugeordneten Gerät verwenden, um Audiodaten über die Verbindung wiederzuspielen (senden) und aufzuzeichnen (zu empfangen). Analog dazu verwendet eine Anwendung die Modemkonfigurationserweiterungen der Kommunikations-API, um den Medienstream zu steuern, wenn der Verbindungsmedienstream von einem Modem stammt.

Um TAPI 2.2 mit Medienstreamzugriff auf ein Telefon oder einen Anruf auf einem Leitungsgerät zu ermöglichen, muss der Dienstanbieter sowohl die Telefonie-SPI als auch die entsprechende Medienstream-SPI oder DDI (Device-Driver Interface) implementieren. Der Dienstanbieter kann Leitungen und Smartphones gleichzeitig unterstützen.

Da diese Geräteklassen und Medienstreamvorgänge unabhängig voneinander funktionieren, muss die Koordination ihrer Verwendung auf Anwendungsebene erfolgen. Mehrere Anwendungen, die Aufrufe und Medienstreams gemeinsam nutzen, erfordern wahrscheinlich eine Koordination ihrer Aktivitäten auf Anwendungsebene, um eine in Konflikt stehende Verwendung von TAPI und der Medienstream-API zu verhindern.

TAPI meldet Änderungen am Typ des Mediendatenstroms (Sprache, Fax, Datenmodem usw.) an teilnehmende Anwendungen. Dieser Prozess wird manchmal als [*Aufrufklassifizierung*](c-tapgloss.md)bezeichnet. Der Mechanismus zum Bestimmen des Mediendatenstromtyps ist spezifisch für den Dienstanbieter. Beispielsweise kann ein Dienstanbieter den Mediendatenstrom nach Energie oder Tönen filtern, die den Medientyp charakterisieren, oder er kann unterschiedliches Ringen, in Nachrichten ausgetauschte Daten über das Netzwerk oder Wissen über den Aufrufer oder die aufgerufene ID verwenden, um diese Bestimmung zu treffen.

-   [Aufrufüberwachung](call-monitoring.md)
-   [Mediensteuerelement](/previous-versions/windows/desktop/legacy/ms736578(v=vs.85))
-   [Ziffernsammlung](digit-gathering.md)
-   [Generieren von Inband-Ziffern und -Tönen](generating-inband-digits-and-tones.md)

 

 
