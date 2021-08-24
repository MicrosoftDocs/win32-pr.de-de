---
title: Formatbezeichner
description: Eigenschaftssatzwerte werden in einem Abschnitt gespeichert, der mit einer eindeutigen FMTID gekennzeichnet ist.
ms.assetid: 3ffb6c5e-72ce-4769-847a-72db6f145d61
keywords:
- Formatbezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ec9e9843b1dfe843e89ebf85eadbbcb5da8cb58dfc1b289eb88c844aae7456
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663150"
---
# <a name="format-identifiers"></a>Formatbezeichner

Eigenschaftssatzwerte werden in einem Abschnitt gespeichert, der mit einer eindeutigen FMTID gekennzeichnet ist. Beispielsweise ist der FMTID-Eigenschaftssatz für die COM-Zusammenfassungsinformationen **F29F85E0-4FF9-1068-AB91-08002B27B3D9.**

Verwenden Sie zum Definieren einer FMTID für den Eigenschaftssatz Zusammenfassungsinformationen das **DEFINE \_ GUID-Makro** in einer Includedatei für den Code, der den Eigenschaftensatz bearbeitet.


```C++
DEFINE_GUID(FMTID_SummaryInformation, 0xF29F85E0, 0x4FF9, 0x1068, 
0xAB, 0x91, 0x08, 0x00, 0x2B, 0x27, 0xB3, 0xD9);
```



Jeder Code, der FMTID für den Eigenschaftssatz Zusammenfassungsinformationen erfordert, kann über die *Variable FMTID \_ SummaryInformation darauf* zugreifen.

Konvertieren Sie beim Speichern von Eigenschaftensätzen in [**IStorage-Instanzen**](/windows/desktop/api/Objidl/nn-objidl-istorage) die FMTID in einen Zeichenfolgennamen für das Speicherobjekt.

 

 




