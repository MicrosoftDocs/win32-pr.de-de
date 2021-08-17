---
description: Die Windows WIA-Schnittstelle (Image Acquisition) ist sowohl eine API als auch eine Gerätetreiberschnittstelle (Device Driver Interface, DDI).
ms.assetid: 725543f8-6e33-4e22-904c-95cbec0388c8
title: Informationen Windows Bilderfassung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d73662083e568a109760a052994bfcbebdfcbe53f858e50a89728a01bba344d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451300"
---
# <a name="about-windows-image-acquisition"></a>Informationen Windows Bilderfassung

Die Windows WIA-Schnittstelle (Image Acquisition) ist sowohl eine API als auch eine Gerätetreiberschnittstelle (Device Driver Interface, DDI). Die WIA-API ist so konzipiert, dass Anwendungen:

-   Ausführung in einer robusten und stabilen Umgebung.
-   Minimieren Sie Interoperabilitätsprobleme.
-   Aufzählen der verfügbaren Geräte für die Bilderfassung
-   Erstellen Sie verbindungen mit mehreren Geräten gleichzeitig.
-   Abfragen von Eigenschaften von Geräten auf standardmäßige und erweiterbare Weise.
-   Erfassen sie Gerätedaten mithilfe von Standardübertragungsmechanismen und Hochleistungsübertragungsmechanismen.
-   Verwalten von Bildeigenschaften bei Datenübertragungen.
-   Sie werden über eine Vielzahl von Geräteereignissen benachrichtigt.

Wiaddi ist so konzipiert, dass die Menge an Code minimiert wird, den ein Hardwareanbieter schreiben muss, während gleichzeitig die Flexibilität beim Erstellen einzelner Lösungen erhalten ist. Dies wird erreicht durch:

-   Bereitstellen einer Standardgerätedienstbibliothek, die die meisten Treibervorgänge ausführt.
-   Förderung von Branchenstandards für die Gerätekommunikation, sodass ein WIA-Treiber die meisten WIA-Geräte unterstützt. Beispiel: Picture Transfer Protocol (PTP).
-   Ermöglicht dem Gerätetreiber die Unterstützung benutzerdefinierter Schnittstellen, ohne dass die Standardgerätedienstbibliothek verwendet werden muss. Treiber müssen jedoch weiterhin die WIA-Standardschnittstellen implementieren.

Dieser Abschnitt bietet eine kurze Übersicht über die WIA-Schnittstelle in den folgenden Bereichen:

-   [WIA-Architektur](-wia-wia-architecture.md)
-   [STI-Kompatibilität](-wia-sti-compatibility.md)
-   [TWAIN-Kompatibilität](-wia-twain-compatibility.md)
-   [WIA-Geräte-Manager](-wia-wia-device-manager.md)
-   [WIA Minidriver-Dienstbibliothek](-wia-wia-minidriver-service-library.md)
-   [WIA-Minitreiber](-wia-wia-minidriver.md)

 

 



