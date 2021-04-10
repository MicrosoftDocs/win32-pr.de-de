---
title: Format Bezeichner
description: Eigenschafts Satz Werte werden in einem Abschnitt gespeichert, der mit einer eindeutigen fmtid gekennzeichnet ist.
ms.assetid: 3ffb6c5e-72ce-4769-847a-72db6f145d61
keywords:
- Format Bezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0202cd1287c3b4fef6e9e2b56e272541a03425b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309812"
---
# <a name="format-identifiers"></a>Format Bezeichner

Eigenschafts Satz Werte werden in einem Abschnitt gespeichert, der mit einer eindeutigen fmtid gekennzeichnet ist. Beispielsweise ist die fmtid für den Eigenschaften Satz für com-Zusammenfassungs Informationen **F29F85E0-4FF9-1068-AB91-08002B27B3D9**.

Zum Definieren einer fmtid für den Eigenschaften Satz für Zusammenfassungs Informationen verwenden Sie das **\_ GUID** -Makro definieren in einer Includedatei für den Code, der den Eigenschaften Satz bearbeitet.


```C++
DEFINE_GUID(FMTID_SummaryInformation, 0xF29F85E0, 0x4FF9, 0x1068, 
0xAB, 0x91, 0x08, 0x00, 0x2B, 0x27, 0xB3, 0xD9);
```



Sämtlicher Code, der die fmtid für den Eigenschaften Satz für Zusammenfassungs Informationen erfordert, kann über die *fmtid \_ SummaryInformation* -Variable darauf zugreifen.

Beim Speichern von Eigenschafts Sätzen in [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Instanzen wird die fmtid in einen Zeichen folgen Namen für das Speicher Objekt konvertiert.

 

 




