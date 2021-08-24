---
description: Ein Telefoniedienstanbieter (TSPI) übernimmt gerätespezifische Steuerungen für die Kommunikationsprogrammierung.
ms.assetid: da54e219-9adb-4a12-baab-52f2b2fb7c66
title: Telefonie-Dienstanbieterschnittstelle (TSPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fac57f3b86acdf105c4c78f46f4f1d1d0e270c2a0b1be2d8bd1f55009926329
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681800"
---
# <a name="telephony-service-provider-interface-tspi"></a>Telefonie-Dienstanbieterschnittstelle (TSPI)

Ein Telefoniedienstanbieter (TSPI) übernimmt gerätespezifische Steuerungen für die Kommunikationsprogrammierung. Ein TSP muss dem Telefoniedienstanbieter (TSPI) entsprechen, um als Dienstanbieter in der Microsoft-Telefonieumgebung zu arbeiten. TSPI definiert die externen Funktionen, die von einem Telefoniedienstanbieter verfügbar gemacht werden, der mit Kommunikationsgeräten bereitgestellt wird.

Ein TSP-Autor muss mit dem Material in [Der Microsoft-Telefonieübersicht](./microsoft-telephony-overview.md)vertraut sein, das die allgemeine Telefoniearchitektur behandelt und eine Übersicht über das Material bietet, das für mehrere Telefonie-APIs verwendet wird. Dieser Abschnitt enthält beispielsweise eine Liste von Sitzungssteuerungsvorgängen, z. B. Park, mit Beschreibungen der einzelnen Vorgänge und springt zu verwandten TAPI 2.2-, TAPI 3- und TSPI-Programmierelementen.

Die folgenden Übersichten behandeln Spezifisches Material für die Anforderungen eines TSP-Autors. Beachten Sie, dass die schwierigsten Teile beim Schreiben eines TSP geräte- und betriebssystemspezifische Details sind, die außerhalb des Rahmens dieses Dokuments liegen.

Die TSPI-Übersicht ist in die folgenden Abschnitte unterteilt:

-   [](/previous-versions/windows/desktop/legacy/ms725196(v=vs.85)) Allgemeine Überlegungen zur Programmierung umfassen DLL-Anforderungen, die ordnungsgemäße Behandlung von Versionen, von TAPI durchgeführte Fehlerüberprüfungen, eine Zusammenfassung, wie TSPI-Funktionen TAPI 2.2-Funktionen (TAPI/C) entsprechen, und eine Erörterung der Dienstebenen, die in TSPI ausgedrückt werden.
-   Der [Lebenszyklus eines Telefoniedienstanbieters](life-cycle-of-a-telephony-service-provider.md) enthält eine zusammenfassende Zusammenfassung der Betriebsphasen eines TSP.
-   [Unter Gerätezugriff](/previous-versions/windows/desktop/legacy/ms725183(v=vs.85)) werden die Grundlagen dazu behandelt, wie ein TSP Geräteinformationen und Steuerelemente für TAPI verfügbar macht.
-   [Der Sitzungszugriff](/previous-versions/windows/desktop/legacy/ms725266(v=vs.85)) deckt ab, was TAPI von einem TSP während einer Kommunikationssitzung erwartet.
-   [Media Access bietet](/previous-versions/windows/desktop/legacy/ms725240(v=vs.85)) eine begrenzte Anzahl von Steuerelementen für Medienstreams. Durch die Verwendung eines Mediendienstanbieters ist eine viel feinerer Kontrolle möglich, und Dienstanbieterautoren sollten diese API nach Möglichkeit verwenden. Der TSPI ermöglicht die Kommunikation zwischen einem TSP-/MSP-Paar.
-   [Telefon Geräte deckt](/previous-versions/windows/desktop/legacy/ms725257(v=vs.85)) die zusätzlichen Informationen und Vorgänge ab, die verfügbar gemacht werden, wenn ein TSP die Telefonsatzsteuerung verarbeitet. Diese Vorgänge sind optional.
-   [Die UI-Schnittstelle des](the-telephony-service-provider-ui-dll-interface.md) Telefoniedienstanbieters deckt spezielle Funktionen ab, die implementiert werden können, damit ein Benutzer viele Aspekte der Funktionalität eines TSP direkt festlegen kann.

Details zu [den TSPI-Programmierelementen](tspi-reference.md) finden Sie in der TSPI-Referenz.

 

 
