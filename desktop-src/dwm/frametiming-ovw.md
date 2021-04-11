---
title: Zugreifen auf und Steuern von DWM-Frame Daten
description: In diesem Thema werden die Desktopfenster-Manager-APIs (DWM) erläutert, die für die Planung und die Medienpräsentation verwendet werden.
ms.assetid: e5d010ea-8411-4537-b9f8-6dc84841087a
keywords:
- Desktopfenster-Manager (DWM), Planung und Media Presentation-APIs
- Dwm (Desktopfenster-Manager), Planung und Media Presentation-APIs
- Planen und Media Presentation-APIs
- Desktopfenster-Manager (DWM), zugreifen auf Frame Daten
- Dwm (Desktopfenster-Manager), zugreifen auf Frame Daten
- Zugreifen auf Frame Daten
- Desktopfenster-Manager (DWM), Steuern von Frame-Daten
- Dwm (Desktopfenster-Manager), Steuern von Frame-Daten
- Steuern von Frame-Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a577847dc20883c84af680d1c39e285a6085e70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310180"
---
# <a name="accessing-and-controlling-dwm-frame-data"></a>Zugreifen auf und Steuern von DWM-Frame Daten

In diesem Thema werden die Desktopfenster-Manager-APIs (DWM) erläutert, die für die Planung und die Medienpräsentation verwendet werden.

## <a name="dwm-frame-timing-api"></a>DWM-Frame-API

Die APIs für die Planung und die Medienpräsentation ermöglichen eine genauere Steuerung, wann das Desktop Image zusammengesetzt und dargestellt wird. Dies wird in der Regel von Medien-und Videowiedergabe Anwendungen benötigt, für die der DWM-Dienst asynchron mit einem eigenen Präsentations Zeitplan ausgeführt wird. Dies kann zu Stichproben Artefakten führen, wenn diese nicht streng gesteuert werden.

Die Funktionen für Planung und Medienpräsentation umfassen Folgendes: Details zu deren Verwendung finden Sie auf diesen Seiten.

-   [**Dwmenablemmcss**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss). Benachrichtigt den DWM-Dienst, die MMCSS-Zeitplanung (Multimedia Class Schedule Service) zu aktivieren, während der Aufrufprozess aktiv ist.
-   [**Dwmgetcompositiontiminginfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo). Ruft die aktuellen Informationen zur Kompositions Zeit ab.
-   [**Dwmmodifypreviousdxframeduration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration). Ändert die Anzahl der Aktualisierungen, während der der vorherige Frame angezeigt wird.
-   [**Dwmsetdxframeduration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration). Legt die Anzahl der Aktualisierungen fest, in denen der dargestellte Frame angezeigt werden soll.
-   [**Dwmsetpresentparameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters). Legt die aktuellen Parameter für die Frame Komposition fest.

 

 




