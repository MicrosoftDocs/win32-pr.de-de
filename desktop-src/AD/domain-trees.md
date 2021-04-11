---
title: Domänen Strukturen
description: Eine Domänen Struktur besteht aus mehreren Domänen, die über ein gemeinsames Schema und eine gemeinsame Konfiguration verfügen und einen zusammenhängenden Namespace bilden.
ms.assetid: 3deb4053-3124-4180-8ab0-35fff689a37e
ms.tgt_platform: multiple
keywords:
- Domänen Struktur Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21d2b36968615fd4e92912fdd94246ef8dda0c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206278"
---
# <a name="domain-trees"></a>Domänen Strukturen

Eine *Domänen* Struktur besteht aus mehreren Domänen, die über ein gemeinsames Schema und eine gemeinsame Konfiguration verfügen und einen zusammenhängenden Namespace bilden. Domänen in einer Struktur werden auch über Vertrauens Stellungen miteinander verknüpft. Active Directory ist ein Satz aus einer oder mehreren Strukturen.

Strukturen können auf zwei Arten angezeigt werden. Eine Ansicht sind die Vertrauens Stellungen zwischen Domänen. Die andere Ansicht ist der Namespace der Domänen Struktur.

## <a name="viewing-trust-relationships"></a>Anzeigen von Vertrauens Stellungen

Sie können ein Diagramm einer Domänen Struktur basierend auf den einzelnen Domänen und der vorhandenen Vertrauensbeziehung zeichnen.

Windows 2000 richtet Vertrauens Stellungen zwischen Domänen basierend auf dem Kerberos-Sicherheitsprotokoll ein. Die Kerberos-Vertrauensstellung ist transitiv und hierarchisch – Wenn Domäne a Domäne b vertraut und Domäne b Domäne c vertraut, vertraut Domäne a Domäne c.

![Vertrauensbeziehung der Domänen Struktur](images/domain-trust.png)

## <a name="viewing-the-namespace"></a>Anzeigen des Namespace

Sie können auch ein Diagramm einer Domänen Struktur basierend auf dem-Namespace zeichnen. Sie können den Distinguished Name eines Objekts ermitteln, indem Sie dem Pfad in der Hierarchie des Domänen Struktur-Namespace folgen. Diese Sicht ist nützlich für das Gruppieren von Objekten in einer logischen Hierarchie. Der Hauptvorteil eines zusammenhängenden Namespace besteht darin, dass eine Tiefe Suche aus dem Stamm des-Namespace die gesamte Hierarchie durchsucht.

![Namespace-Domänen Struktur](images/namespace.png)

 

 




