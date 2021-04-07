---
title: Eingebettete Zeichen folgen
description: Informationsstrukturen enthalten keine eingebetteten Zeichen folgen. Dies verbessert die Ausrichtung der Informationsstrukturen und ermöglicht OEM-Flexibilität in den Kernfunktionen.
ms.assetid: a3272a0a-5352-4847-84fd-113b4467c32c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365a9c71ed50971661f9ad06855024ecba2796f1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711579"
---
# <a name="embedded-strings"></a>Eingebettete Zeichen folgen

Informationsstrukturen enthalten keine eingebetteten Zeichen folgen. Dies verbessert die Ausrichtung der Informationsstrukturen und ermöglicht OEM-Flexibilität in den Kernfunktionen.

Alle Informationsfelder, die in einem enumerationsrückruf zurückgegeben werden, die anschließend als Schlüssel für den Aufrufen einer GetInfo-Netzwerk Verwaltungsfunktion verwendet werden können, sind im enumerationspuffer garantiert vorhanden. Wenn die Informations Zeichenfolge mit variabler Länge, die den Schlüssel Feldwert angeben würde, nicht passt, wird die gesamte Struktur mit fester Länge für den Eintrag nicht zurückgegeben. Andere Felder mit variabler Länge werden als **null** -Zeiger für die Groß-/Kleinschreibung zurückgegeben, in der die Zeichenfolge nicht passt.

 

 




