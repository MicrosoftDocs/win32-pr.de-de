---
title: Leistungs Attribute
description: Verwenden Sie die folgenden Attribute in einer IDL-Datei, um die Größe des stubcodes zu verringern oder die Leistung anderweitig zu verbessern.
ms.assetid: 0f23265e-7f3e-4a15-ac3b-1d852a8110eb
keywords:
- IDL-Mittell, Attribute, Leistung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbfa518b400d237c9fd3789f61b7e74a0c38276
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037601"
---
# <a name="performance-attributes"></a>Leistungs Attribute

Verwenden Sie die folgenden Attribute in einer IDL-Datei, um die Größe des stubcodes zu verringern oder die Leistung anderweitig zu verbessern.



| Attribut                             | Verbrauch                                                                                                                                                |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**lassen**](ignore.md)              | Gibt an, dass ein in einer Struktur oder Union enthaltener Zeiger und das vom Zeiger festgestellte Objekt nicht übertragen werden soll.                        |
| [**nah**](local.md)                | Gibt eine Funktion an, die für die Anwendung lokal ist, für die die Mittel-l keinen Stub-Code generieren muss.                                           |
| [**Wire \_ Marshal**](wire-marshal.md) | Definiert einen Datentyp als einfacheren Typ für die Übertragung über ein Netzwerk und ermöglicht das Implementieren von Marshalling-und unmarshallingroutinen für den Typ. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ACF-Attribute für die Speicherverwaltung](memory-management-acf-attributes.md)
</dt> <dt>

[ACF-Attribute der Stub-Optimierung](stub-optimization-acf-attributes.md)
</dt> </dl>

 

 




