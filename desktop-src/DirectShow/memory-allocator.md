---
description: Speicherzuweisung
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Speicherzuweisung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2412adb78be18ac8c14eb4706624424f97ff13
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909419"
---
# <a name="memory-allocator"></a>Speicherzuweisung

Das Speicherzuweisungsobjekt ordnet Puffer für Medienbeispiele zu. Filter können dieses Objekt verwenden, um Freigegebene Speicherpuffer zu reservieren. Ein Filter mit speziellen Anforderungen kann jedoch auch ein eigenes Speicherzuweisungsobjekt implementieren. Erstellen Sie dieses Objekt, indem Sie **CoCreateInstance aufrufen.**



| Bezeichnung | Wert |
|------------------|----------------------------------------|
| Klassenbezeichner | CLSID \_ MemoryAllocator                 |
| Schnittstellen       | [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Objekte](directshow-objects.md)
</dt> </dl>

 

 



