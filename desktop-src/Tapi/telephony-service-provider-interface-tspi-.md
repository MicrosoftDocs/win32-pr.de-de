---
description: Von einem Telefoniedienstanbieter (TSPI) werden gerätespezifische Steuerelemente für die Kommunikations Programmierung verarbeitet.
ms.assetid: da54e219-9adb-4a12-baab-52f2b2fb7c66
title: Telefoniedienstanbieter-Schnittstelle (TSPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a9d8ac4fd15fbc2685073e5954e14951f33acd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352302"
---
# <a name="telephony-service-provider-interface-tspi"></a>Telefoniedienstanbieter-Schnittstelle (TSPI)

Von einem Telefoniedienstanbieter (TSPI) werden gerätespezifische Steuerelemente für die Kommunikations Programmierung verarbeitet. Ein TSP muss dem Telefoniedienstanbieter (TSPI) entsprechen, um in der Microsoft-Telefonieumgebung als Dienstanbieter fungieren zu können. TSPI definiert die externen Funktionen, die von einem Telefoniedienstanbieter zur Verfügung gestellt werden

Ein TSP-Autor muss mit dem Material in der [Übersicht über die Microsoft-Telefonie](./microsoft-telephony-overview.md)vertraut sein, das die allgemeine Telefoniearchitektur behandelt und einen Überblick über die allgemeinen Informationen zu verschiedenen telefonieapis bietet. Dieser Abschnitt enthält z. b. eine Liste der Sitzungs Steuerungs Vorgänge, wie z. b. Park, mit Beschreibungen der einzelnen Vorgänge und springt zu verwandten TAPI 2,2-, TAPI 3-und TSPI-Programmier Elementen.

Die folgenden Übersichten decken Material ab, das spezifisch für die Anforderungen eines TSP-Autors ist. Beachten Sie, dass die schwierigsten Teile beim Schreiben eines TSP Geräte-und betriebssystemspezifische Details sind, die außerhalb des Umfangs dieses Dokuments liegen.

Die Übersicht über TSPI ist in die folgenden Abschnitte unterteilt:

-   [Allgemeine Überlegungen zur Programmierung](/previous-versions/windows/desktop/legacy/ms725196(v=vs.85)) umfassen dll-Anforderungen, ordnungsgemäße Verarbeitung von Versionen, von TAPI ausgeführte Fehlerprüfungen, eine Zusammenfassung der Entsprechung von TSPI-Funktionen zu TAPI 2,2-Funktionen (TAPI/C) und eine Erörterung der Dienst Ebenen, wie in TSPI ausgedrückt.
-   Der [Lebenszyklus eines Telefoniedienstanbieters](life-cycle-of-a-telephony-service-provider.md) enthält eine allgemeine Zusammenfassung der Betriebsphasen eines TSP.
-   Der [Gerätezugriff](/previous-versions/windows/desktop/legacy/ms725183(v=vs.85)) behandelt die Grundlagen, wie ein TSP Geräteinformationen und Steuerelemente für TAPI verfügbar macht.
-   Der [Sitzungs Zugriff](/previous-versions/windows/desktop/legacy/ms725266(v=vs.85)) deckt, was TAPI von einem TSP bei einer Kommunikationssitzung erwartet.
-   Der [Medien Zugriff](/previous-versions/windows/desktop/legacy/ms725240(v=vs.85)) bietet einen begrenzten Satz von Steuerelementen für Mediendaten Ströme. Eine weitaus präzisere Steuerung ist durch die Verwendung eines Media Service-Anbieters möglich, und die Autoren von Dienstanbietern sollten diese API verwenden, wenn dies möglich ist. Die TSPI ermöglicht die Kommunikation zwischen einem TSP-/MSP-Paar.
-   [Telefongeräte](/previous-versions/windows/desktop/legacy/ms725257(v=vs.85)) decken die ergänzenden Informationen und Vorgänge ab, die verfügbar gemacht werden, wenn ein TSP die Telefon Satz Steuerung behandelt. Diese Vorgänge sind optional.
-   [Die UI-DLL-Schnittstelle für den Telefoniedienstanbieter](the-telephony-service-provider-ui-dll-interface.md) deckt spezielle Funktionen ab, die implementiert werden können, um es Benutzern zu ermöglichen, viele Aspekte der Funktionalität eines TSP direkt festzulegen

Ausführliche Informationen zu den TSPI-Programmier Elementen finden Sie in der [TSPI-Referenz](tspi-reference.md) .

 

 
