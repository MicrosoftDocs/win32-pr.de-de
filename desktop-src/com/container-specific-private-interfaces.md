---
title: Private Schnittstellen Container-Specific
description: Private Schnittstellen Container-Specific
ms.assetid: 429cf71c-9b9d-4d0b-b5de-91fbe1dde3cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c6569a79e9f1801c6fd82543bc40408903c780
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311298"
---
# <a name="container-specific-private-interfaces"></a>Private Schnittstellen Container-Specific

Einige Container stellen Container spezifische private Schnittstellen für zusätzliche Funktionen oder eine verbesserte Leistung bereit. Steuerelemente, die sich auf diese Container spezifischen Schnittstellen stützen, sollten, wenn möglich, ohne diese Container spezifischen Schnittstellen funktionieren, damit das Steuerelement in verschiedenen Containern funktioniert. Beispielsweise implementiert Visual Basic Private Schnittstellen, die Zeichen folgen Formatierungsfunktionen für Steuerelemente bereitstellen. Wenn ein Steuerelement diese privaten Formatierungs Schnittstellen nutzt, sollte es in der Lage sein, mit standardmäßiger Formatierungs Unterstützung auszuführen, wenn diese Schnittstellen nicht verfügbar sind. Wenn das Steuerelement ohne die privaten Schnittstellen funktionieren kann, sollte es entsprechende Maßnahmen ergreifen (z. b. den Benutzer vor eingeschränkter Funktionalität warnen), aber weiterhin arbeiten. Wenn dies nicht möglich ist, sollte eine Komponenten Kategorie bei Bedarf registriert werden, damit nur Container, die diese Funktion unterstützen, diese Steuerelemente hosten können.

 

 




