---
description: Der Volumeschattenkopie-Dienst (VSS) stellt die Systeminfrastruktur zum Ausführen von VSS-Anwendungen auf Windows-basierten Systemen bereit.
ms.assetid: 237b2729-1e9b-4d0e-9c59-990e047a0360
title: Der Volumeschattenkopie-Dienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274e1e561b702dc2e69782fa5e9c2b47e6ea6a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751601"
---
# <a name="the-volume-shadow-copy-service"></a>Der Volumeschattenkopie-Dienst

Der Volumeschattenkopie-Dienst (VSS) stellt die Systeminfrastruktur zum Ausführen von VSS-Anwendungen auf Windows-basierten Systemen bereit.

VSS ist zwar größtenteils für Benutzer und Entwickler transparent, doch führt VSS Folgendes aus:

-   Koordiniert Aktivitäten von Anbietern, Writern und Anforderern bei der Erstellung und Verwendung von Schatten Kopien.
-   Gibt den Standardsystem Anbieter an.
-   Implementiert die Treiber Funktionalität auf niedriger Ebene, die für jeden Anbieter erforderlich ist.

Der VSS-Dienst startet on demand. Dies bedeutet, dass dieser Dienst erst aktiviert werden muss, damit VSS-Vorgänge ausgeführt werden können.

 

 



