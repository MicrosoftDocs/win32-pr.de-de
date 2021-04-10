---
title: Aktualisieren von Erkennungsregeln für Sicherheitsanwendungen
description: Aktualisieren von Erkennungsregeln für Sicherheitsanwendungen
ms.assetid: A272C09B-A777-4119-BAB9-F91ABC03717A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242c6f9da8d474c16fab7573e216d3157f93b014
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104039739"
---
# <a name="security-app-detection-rules-update"></a>Aktualisieren von Erkennungsregeln für Sicherheitsanwendungen

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


### <a name="description"></a>BESCHREIBUNG

Die Windows Store-Apps, die in Windows 8 hinzugefügt werden, werden alle unter "Programme" (% Program Files%) an einem gemeinsamen Speicherort installiert. wird als \\ Programmdateien \\ Windowsapps bezeichnet.

### <a name="manifestation"></a>Ausstrahlung

Dies kann zu Konflikten mit vorhandenen Konfigurationen führen, und einige Virenschutz-und antischadsoftwareerkennungen sehen diesen Standort als potenziellen Speicherort an, der eine Ursache für die Sorge ist.

### <a name="mitigation"></a>Minderung

Die aktuellen Empfehlungen lauten:

-   Wechseln von den \\ Programmdateien \\ Windowsapps zum Speichern beliebiger benutzerdefinierter apps
-   Antiviren-/antischadsoftwarehersteller sollten ihre Heuristik aktualisieren, damit Sie diesen Standort nicht als Malware Speicherort identifizieren können.

 

 




