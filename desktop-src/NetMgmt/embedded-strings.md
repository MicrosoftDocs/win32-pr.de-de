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
# <a name="embedded-strings"></a><span data-ttu-id="652c7-104">Eingebettete Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="652c7-104">Embedded Strings</span></span>

<span data-ttu-id="652c7-105">Informationsstrukturen enthalten keine eingebetteten Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="652c7-105">Information structures will not contain embedded strings.</span></span> <span data-ttu-id="652c7-106">Dies verbessert die Ausrichtung der Informationsstrukturen und ermöglicht OEM-Flexibilität in den Kernfunktionen.</span><span class="sxs-lookup"><span data-stu-id="652c7-106">This improves the alignment of the information structures and allows for OEM flexibility in the core functions.</span></span>

<span data-ttu-id="652c7-107">Alle Informationsfelder, die in einem enumerationsrückruf zurückgegeben werden, die anschließend als Schlüssel für den Aufrufen einer GetInfo-Netzwerk Verwaltungsfunktion verwendet werden können, sind im enumerationspuffer garantiert vorhanden.</span><span class="sxs-lookup"><span data-stu-id="652c7-107">Any information field that is returned in an enumeration call that can be subsequently used as a key for the call to a GetInfo network management function is guaranteed to be present in the enumeration buffer.</span></span> <span data-ttu-id="652c7-108">Wenn die Informations Zeichenfolge mit variabler Länge, die den Schlüssel Feldwert angeben würde, nicht passt, wird die gesamte Struktur mit fester Länge für den Eintrag nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="652c7-108">If the variable-length information string that would specify the key field value will not fit, then the entire fixed-length structure for the entry is not returned.</span></span> <span data-ttu-id="652c7-109">Andere Felder mit variabler Länge werden als **null** -Zeiger für die Groß-/Kleinschreibung zurückgegeben, in der die Zeichenfolge nicht passt.</span><span class="sxs-lookup"><span data-stu-id="652c7-109">Other variable-length fields will be returned as a **NULL** pointer for the case in which the string does not fit.</span></span>

 

 




