---
title: Domänenstrukturen
description: Eine Domänenstruktur besteht aus mehreren Domänen, die ein gemeinsames Schema und eine gemeinsame Konfiguration aufweisen und einen zusammenhängenden Namespace bilden.
ms.assetid: 3deb4053-3124-4180-8ab0-35fff689a37e
ms.tgt_platform: multiple
keywords:
- Active Directory-Domänenstruktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40a1e2ed05284d2a08735b048fb41d97d6597634f711094d0a3763c2d7f8be67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430516"
---
# <a name="domain-trees"></a>Domänenstrukturen

Eine *Domänenstruktur* besteht aus mehreren Domänen, die ein gemeinsames Schema und eine gemeinsame Konfiguration aufweisen und einen zusammenhängenden Namespace bilden. Domänen in einer Struktur werden auch über Vertrauensstellungen miteinander verknüpft. Active Directory besteht aus einer oder mehreren Strukturen.

Strukturen können auf zwei Arten angezeigt werden. Eine Ansicht sind die Vertrauensstellungen zwischen Domänen. Die andere Ansicht ist der Namespace der Domänenstruktur.

## <a name="viewing-trust-relationships"></a>Anzeigen von Vertrauensstellungen

Sie können ein Diagramm einer Domänenstruktur basierend auf den einzelnen Domänen und der vorhandenen Vertrauensstellung zeichnen.

Windows 2000 werden Vertrauensstellungen zwischen Domänen basierend auf dem Kerberos-Sicherheitsprotokoll eingerichtet. Die Kerberos-Vertrauensstellung ist transitiv und hierarchisch: Wenn Domäne A Domäne B vertraut und Domäne B Domäne C vertraut, dann vertraut Domäne A Domäne C.

![Domänenstruktur-Vertrauensstellung](images/domain-trust.png)

## <a name="viewing-the-namespace"></a>Anzeigen des Namespace

Sie können auch ein Diagramm einer Domänenstruktur basierend auf dem Namespace zeichnen. Sie können den Distinguished Name eines Objekts ermitteln, indem Sie dem Pfad nach oben in der Hierarchie des Domänenstrukturnamespace folgen. Diese Ansicht ist nützlich, um Objekte in einer logischen Hierarchie zu gruppieren. Der Hauptvorteil eines zusammenhängenden Namespaces besteht darin, dass eine tiefe Suche aus dem Stamm des Namespace die gesamte Hierarchie durchsucht.

![Namespacedomänenstruktur](images/namespace.png)

 

 




