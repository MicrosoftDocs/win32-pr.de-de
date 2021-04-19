---
title: Sortieren (ADSI)
description: Ein Client kann einen Server zum Sortieren des Resultsets anfordern.
ms.assetid: 795d27f0-0bfa-417e-aa1f-f2471f92dc45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4ee790a646367366afe33639abd8f5aa57ed4f
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2019
ms.locfileid: "106341500"
---
# <a name="sorting-adsi"></a>Sortieren (ADSI)

Ein Client kann einen Server zum Sortieren des Resultsets anfordern. Sie können Folgendes angeben:

-   Sortierreihenfolge: entweder eine aufsteigende oder absteigende Sortierreihenfolge.
-   Sortier Attribute: in einer Sortier Zeichenfolge können mehrere Attribute angegeben werden. Sortieren Sie z. b. nach Nachname und Vorname.

Wenn Sie die Sortierreihenfolge angeben, sollten Sie versuchen, eines der indizierten Attribute zu verwenden. Andernfalls muss der Server ein vervollständigen-Resultset berechnen, bevor es an den Client gesendet wird. Dies gilt auch, wenn Sie eine seitenweise Suche angefordert und eine Seitengröße angegeben haben.

> [!Note]  
> Nicht alle Verzeichnisserver unterstützen mehrere Attribut Sortierungen oder eine Sortierreihenfolge.

 

 

 




