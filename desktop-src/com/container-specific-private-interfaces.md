---
title: Container-Specific private Schnittstellen
description: Container-Specific private Schnittstellen
ms.assetid: 429cf71c-9b9d-4d0b-b5de-91fbe1dde3cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a426ae67d3722406ca6c1428d46d0bc3b4a937a1bcdd105de6f376bbe53a5ccd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550634"
---
# <a name="container-specific-private-interfaces"></a>Container-Specific private Schnittstellen

Einige Container bieten containerspezifische private Schnittstellen für zusätzliche Funktionen oder verbesserte Leistung. Steuerelemente, die auf diesen containerspezifischen Schnittstellen basieren, sollten nach Möglichkeit funktionieren, ohne dass diese containerspezifischen Schnittstellen vorhanden sind, sodass das Steuerelement in verschiedenen Containern funktioniert. Beispielsweise implementiert Visual Basic Schnittstellen, die Zeichenfolgenformatierungsfunktionen für Steuerelemente bereitstellen. Wenn ein Steuerelement diese privaten Formatierungsschnittstellen verwendet, sollte es mit Standardformatierungsunterstützung ausgeführt werden können, wenn diese Schnittstellen nicht verfügbar sind. Wenn das Steuerelement ohne die privaten Schnittstellen funktionieren kann, sollte es entsprechende Maßnahmen ergreifen (z. B. den Benutzer vor eingeschränkter Funktionalität warnen), aber weiterhin funktionieren. Wenn dies keine Option ist, sollte eine Komponentenkategorie nach Bedarf registriert werden, damit nur Container, die diese Funktionalität unterstützen, diese Steuerelemente hosten können.

 

 




