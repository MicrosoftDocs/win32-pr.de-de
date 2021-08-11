---
title: Schemaerweiterungen
description: Die Architektur des ADSI-Schemas bietet, dass dem Schemaklassencontainer neue Schemaklassen und zur Laufzeit neue Eigenschaften zu einem vorhandenen Schemaklassenobjekt hinzugefügt werden können.
ms.assetid: 935d39ca-cfb9-4aa3-aa0e-b614f7b359f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c7fdc4b363fea83029fc5526464bd5825fa851dbe82e874911a0ab45d869843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178819"
---
# <a name="schema-extensions"></a>Schemaerweiterungen

Die Architektur des ADSI-Schemas bietet, dass dem Schemaklassencontainer neue Schemaklassen und zur Laufzeit neue Eigenschaften zu einem vorhandenen Schemaklassenobjekt hinzugefügt werden können. Letztere Fähigkeit erfordert keinen neuen Code. Dies ist ein wichtiges Feature für Namespaces, die erweiterbare Verzeichnisdienste ermöglichen. Die Anbieterkomponente muss diese Erweiterbarkeit zulassen und wissen, wo auf die Klasseninstanz und die Werte ihrer Eigenschaften zugegriffen und gespeichert werden soll. In einem typischen erweiterbaren Verzeichnisdienst werden diese Informationen in der Verzeichnisdienstdatenbank auf die gleiche Weise wie alle anderen Schemaklassen- und Eigenschaftendefinitionen gespeichert.

> [!Note]  
> In der Terminologie der COM-Schnittstelle können einer vorhandenen Schemaklasse nur Eigenschaften hinzugefügt werden, keine Methoden. Das Hinzufügen einer neuen Methode erfordert das Hinzufügen einer neuen Implementierung dieser Methode und somit zusätzlichen Code.

 

Ein Beispiel für ein bestimmtes Anbieterschema finden Sie unter [Schemaverwaltung.](schema-management.md)

 

 




