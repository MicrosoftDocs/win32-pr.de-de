---
title: Schema Erweiterungen
description: Die Architektur des ADSI-Schemas stellt dar, dass dem Schema Klassencontainer neue Schema Klassen und neuen Eigenschaften zur Laufzeit hinzugefügt werden können.
ms.assetid: 935d39ca-cfb9-4aa3-aa0e-b614f7b359f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b86491966e2bfddbef72d68d7a96869448c38188
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100558"
---
# <a name="schema-extensions"></a>Schema Erweiterungen

Die Architektur des ADSI-Schemas stellt dar, dass dem Schema Klassencontainer neue Schema Klassen und neuen Eigenschaften zur Laufzeit hinzugefügt werden können. Die zweite Möglichkeit erfordert keinen neuen Code. Dies ist ein wichtiges Feature für Namespaces, die erweiterbare Verzeichnisdienste ermöglichen. Die Anbieter Komponente muss diese Erweiterbarkeit zulassen und wissen, wo Sie auf die Klasseninstanz und die Werte ihrer Eigenschaften zugreifen und diese speichern können. In einem typischen erweiterbaren Verzeichnisdienst werden diese Informationen in der Verzeichnisdienst Datenbank auf die gleiche Weise gespeichert wie alle anderen Schema Klassen-und Eigenschafts Definitionen.

> [!Note]  
> In der Terminologie der COM-Schnittstelle können nur Eigenschaften zu einer vorhandenen Schema Klasse und nicht zu Methoden hinzugefügt werden. Das Hinzufügen einer neuen Methode erfordert das Hinzufügen einer neuen Implementierung dieser Methode und erfordert daher zusätzlichen Code.

 

Ein Beispiel für ein bestimmtes Anbieter Schema finden Sie unter [Schema Verwaltung](schema-management.md).

 

 




