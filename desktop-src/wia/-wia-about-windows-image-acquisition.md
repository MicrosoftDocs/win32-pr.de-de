---
description: Die Windows-Abbild Erfassungs Schnittstelle (WIA) ist sowohl eine API als auch eine Gerätetreiber Schnittstelle (DDI).
ms.assetid: 725543f8-6e33-4e22-904c-95cbec0388c8
title: Informationen zur Windows-Abbild Erfassung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80eed6289f7a30476ea6889c947577ad003b656e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360554"
---
# <a name="about-windows-image-acquisition"></a>Informationen zur Windows-Abbild Erfassung

Die Windows-Abbild Erfassungs Schnittstelle (WIA) ist sowohl eine API als auch eine Gerätetreiber Schnittstelle (DDI). Die WIA-API ist so konzipiert, dass Anwendungen:

-   Führen Sie in einer robusten und stabilen Umgebung aus.
-   Minimieren von Interoperabilitätsproblemen
-   Listet die verfügbaren Abbild Erwerbs Geräte auf.
-   Gleichzeitiges Erstellen von Verbindungen mit mehreren Geräten.
-   Abfragen von Eigenschaften von Geräten in einer standardmäßigen und erweiterbaren Weise.
-   Beschaffen von Gerätedaten mithilfe von Standard-und Hochleistungs Übertragungsmechanismen
-   Behalten Sie Bildeigenschaften über Datenübertragungen hinweg bei.
-   Sie werden über eine Vielzahl von Geräte Ereignissen benachrichtigt.

Der wiaddi ist so konzipiert, dass die Menge an Code minimiert wird, die ein Hardwarehersteller schreiben muss, und gleichzeitig die Flexibilität, individuelle Lösungen zu erstellen. Dies wird durch Folgendes erreicht:

-   Bereitstellen einer Standard-Geräte Dienst Bibliothek, mit der die meisten Treiber Vorgänge durchführt werden
-   Herauf Stufen von Kommunikationsstandards für Industriegeräte, sodass ein WIA-Treiber die meisten WIA-Geräte unterstützt. Beispielsweise PTP (Picture Transfer Protocol).
-   Zulassen, dass der Gerätetreiber benutzerdefinierte Schnittstellen unterstützt, ohne dass die standardmäßige Geräte Dienst Bibliothek verwendet werden muss. Allerdings müssen die Treiber weiterhin die standardmäßigen WIA-Schnittstellen implementieren.

Dieser Abschnitt enthält eine kurze Übersicht über die WIA-Schnittstelle in den folgenden Bereichen:

-   [WIA-Architektur](-wia-wia-architecture.md)
-   [STI-Kompatibilität](-wia-sti-compatibility.md)
-   [TWAIN-Kompatibilität](-wia-twain-compatibility.md)
-   [WIA-Device Manager](-wia-wia-device-manager.md)
-   [WIA-Mini Treiber-Dienst Bibliothek](-wia-wia-minidriver-service-library.md)
-   [WIA-Mini Treiber](-wia-wia-minidriver.md)

 

 



