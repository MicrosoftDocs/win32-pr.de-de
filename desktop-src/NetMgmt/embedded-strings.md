---
title: Eingebettete Zeichenfolgen
description: Informationsstrukturen enthalten keine eingebetteten Zeichenfolgen. Dies verbessert die Ausrichtung der Informationsstrukturen und ermöglicht OEM-Flexibilität in den Kernfunktionen.
ms.assetid: a3272a0a-5352-4847-84fd-113b4467c32c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6121e805a1dbe329cee52a760c809ded21f1740b19adaa3e18eaa5033fd15897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912250"
---
# <a name="embedded-strings"></a>Eingebettete Zeichenfolgen

Informationsstrukturen enthalten keine eingebetteten Zeichenfolgen. Dies verbessert die Ausrichtung der Informationsstrukturen und ermöglicht OEM-Flexibilität in den Kernfunktionen.

Jedes Informationsfeld, das in einem Enumerationsaufruf zurückgegeben wird und anschließend als Schlüssel für den Aufruf einer GetInfo-Netzwerkverwaltungsfunktion verwendet werden kann, ist garantiert im Enumerationspuffer vorhanden. Wenn die Informationszeichenfolge variabler Länge, die den Schlüsselfeldwert angibt, nicht passt, wird die gesamte Struktur mit fester Länge für den Eintrag nicht zurückgegeben. Andere Felder variabler Länge werden als **NULL-Zeiger** für den Fall zurückgegeben, dass die Zeichenfolge nicht passt.

 

 




