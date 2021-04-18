---
description: Speicherzuweisung
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Speicherzuweisung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be12e25886eda968a00b10386a6eac3fd36e7279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522203"
---
# <a name="memory-allocator"></a>Speicherzuweisung

Das arbeitsspeicherzuordnerobjekt weist Puffer für Medien Beispiele zu. Filter können dieses Objekt verwenden, um freigegebene Speicherpuffer zuzuordnen. ein Filter mit speziellen Anforderungen kann jedoch auch ein eigenes Speicher zuordnerobjekt implementieren. Erstellen Sie dieses Objekt durch Aufrufen von **CoCreateInstance**.



|                  |                                        |
|------------------|----------------------------------------|
| Klassen Bezeichner | CLSID- \_ memoryzuweisung                 |
| Schnittstellen       | [**Imemzuordcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Objekte](directshow-objects.md)
</dt> </dl>

 

 



