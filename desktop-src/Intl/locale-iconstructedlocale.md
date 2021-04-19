---
description: Gebiets Schema- \_ iconstructedlocale-Konstante Beschreibung
ms.assetid: 5557ee1e-09bf-0d0b-8e73-df32d9a406dd
title: LOCALE_ICONSTRUCTEDLOCALE
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 120c206a14030a182378977c9e68fb7dcd77200d
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/30/2021
ms.locfileid: "106374062"
---
# <a name="locale_iconstructedlocale"></a>Gebiets Schema \_ iconstructedlocale

Bezeichner für die Anforderung, wenn das Gebiets Schema ein "konstruiertes" Gebiets Schema ist. Die Verwendung dieses LCTYPE ist nicht empfehlenswert.

Dadurch wird ein Gebiets Schema identifiziert, für das Windows viele nicht über umfassende Informationen verfügt und zur Laufzeit Informationen erstellen muss. In der Regel sind die von LOCALE_ICONSTRUCTEDLOCALE bereitgestellten Informationen eingeschränkt, da Windows so viele Daten bereitstellt, wie es für jedes Gebiets Schema verfügbar ist. Daher wird von der Verwendung dieses LCTYPE abgeraten.


| Wert | Bedeutung                 |
|-------|-------------------------|
| 0     | Nicht erstellt         |
| 1     | Ist ein konstruiertes Gebiets Schema |


Ein Beispiel wäre eine Anforderung für "de-US" oder Deutsch im USA. NLS verwendet die deutschen Sprach Daten, die gefunden werden können, und die USA Regions Daten, die gefunden werden können. 

Dies ist möglicherweise nicht perfekt, da das System wahrscheinlich keine Informationen über den Namen USA in Deutsch hat. Wenn die Anwendung oder der Benutzer jedoch einen "de-US"-Kontext wünscht, sind die zurückgegebenen Daten die beste Verfügbarkeit. 

Apps, die LOCALE_ICONSTRUCTEDLOCALE zum ablehnen von Gebiets Schemas verwenden und auf ein anderes Gebiets Schema zurückgreifen, haben in der Regel eine schlechtere Darstellung, wie z. b. die Landung von de-de oder en-US in diesem Beispiel. Keines der beiden Bereiche entspricht der ursprünglichen Anforderung für deutschsprachige Sprache mit einer USA Region.

