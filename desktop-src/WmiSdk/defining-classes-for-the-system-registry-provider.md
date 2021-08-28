---
description: Eine Verwaltungsanwendung, die den Systemregistrierungsanbieter verwendet, kann Klassen mit Eigenschaften definieren, die Registrierungsdaten für bestimmte Schlüssel darstellen, und die Klassen dann im WMI-Repository speichern.
ms.assetid: e8707a3d-a393-4be0-9e86-297f0af15d99
ms.tgt_platform: multiple
title: Definieren von Klassen für den Systemregistrierungsanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deecdbc419c5a245e609380732474a39089f28cb8c2fd76c2ac57546f2d00110
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097290"
---
# <a name="defining-classes-for-the-system-registry-provider"></a>Definieren von Klassen für den Systemregistrierungsanbieter

Eine Verwaltungsanwendung, die den Systemregistrierungsanbieter verwendet, kann Klassen mit Eigenschaften definieren, die Registrierungsdaten für bestimmte Schlüssel darstellen, und die Klassen dann im WMI-Repository speichern. Die meisten Prozesse zum Definieren einer Klasse für die Systemregistrierung sind identisch mit der Definition einer anderen Klasse. Der Systemregistrierungsanbieter erfordert jedoch, dass Sie bestimmte Datentypen und Qualifizierer verwenden.

Im folgenden Verfahren wird beschrieben, wie eine Klasse für den Systemregistrierungsanbieter definiert wird.

**So definieren Sie eine Klasse für den Systemregistrierungsanbieter**

1.  Erstellen Sie die -Klasse wie jede andere Klasse.

    Weitere Informationen finden Sie unter [Erstellen einer Klasse.](creating-a-class.md)

2.  Ordnen Sie die entsprechenden Registrierungsdatentypen den entsprechenden WMI-Typen zu.

    Der Systemregistrierungsanbieter ordnet die Registrierungsdatentypen bestimmten WMI-Datentypen zu. Weitere Informationen finden Sie unter [Zuordnen eines Registrierungsdatentyps zu einem WMI-Datentyp.](mapping-a-registry-data-type-to-a-wmi-data-type.md)

3.  Verwenden Sie die erforderlichen Qualifizierer, um den Speicherort des Registrierungsanbieters und den Speicherort des entsprechenden Registrierungsschlüssels zu definieren.

    Der Systemregistrierungsanbieter verwendet drei Qualifizierer, um den Speicherort verschiedener Klassen, Anbieter und Registrierungseinträge zu definieren. Weitere Informationen finden Sie unter [Definieren einer Registrierungsklasse mit Qualifizierern.](defining-a-registry-class-with-qualifiers.md)

 

 



