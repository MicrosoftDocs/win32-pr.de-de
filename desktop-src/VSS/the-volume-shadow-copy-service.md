---
description: Der Volumeschattenkopie-Dienst (VSS) stellt die Systeminfrastruktur zum Ausführen von VSS-Anwendungen auf Windows-basierten Systemen zur Verfügung.
ms.assetid: 237b2729-1e9b-4d0e-9c59-990e047a0360
title: Die Volumeschattenkopie-Dienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f71e21ba0f20eaa0f3723cd0da6cb3efb89bae027678d154ab8b5b5568532ac8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866240"
---
# <a name="the-volume-shadow-copy-service"></a>Die Volumeschattenkopie-Dienst

Der Volumeschattenkopie-Dienst (VSS) stellt die Systeminfrastruktur zum Ausführen von VSS-Anwendungen auf Windows-basierten Systemen zur Verfügung.

VsS ist für Benutzer und Entwickler zwar größtenteils transparent, führt aber folgende Schritte aus:

-   Koordiniert Aktivitäten von Anbietern, Writern und Anfordernden bei der Erstellung und Verwendung von Schattenkopien
-   Aktiviert den Standardsystemanbieter.
-   Implementiert Treiberfunktionen auf niedriger Ebene, die erforderlich sind, damit jeder Anbieter funktioniert.

Der VSS-Dienst startet on demand. Dies bedeutet, dass dieser Dienst erst aktiviert werden muss, damit VSS-Vorgänge ausgeführt werden können.

 

 



