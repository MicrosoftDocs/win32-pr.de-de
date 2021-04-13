---
title: Entfernen von Metadatenattributen
description: Entfernen von Metadatenattributen
ms.assetid: 44546091-406f-4ae6-914a-942d1b89e0e4
keywords:
- Windows Media-Format-SDK, Entfernen von Metadatenattributen
- Advanced Systems Format (ASF), Entfernen von Metadatenattributen
- ASF (Advanced Systems Format), Entfernen von Metadatenattributen
- Metadaten, Entfernen von Attributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b10176452dcc78cc3eca898b61c350a157e568
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104390050"
---
# <a name="removing-metadata-attributes"></a>Entfernen von Metadatenattributen

Sie können ein Metadatenattribut entfernen, indem Sie den Index und die streamnummer an die [**IWMHeaderInfo3::D eleteattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute) -Methode übergeben. Die Reihenfolge, in der die übrigen Attribute nach dem Entfernen eines Attributs indiziert werden, ändert sich nicht. alle verbleibenden Attribute, die ursprünglich einen Indexwert aufweisen, der größer als der entfernte Wert war, haben die Indexwerte um 1 reduziert. Wenn Sie mehrere Attribute entfernen, führen Sie dies in absteigender Reihenfolge nach Index durch, um die Anpassung der Indizierung zu vermeiden.

Der [**IWMHeaderInfo3:: getattributeindices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) -Methode gibt die Indexwerte in absteigender Reihenfolge zurück, um die Werte zu entfernen.

> [!Note]  
> Indexwerte, die mit den Methoden von [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) abgerufen werden, sind nicht mit Indexwerten kompatibel, die mit den Methoden von [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)abgerufen werden. Wenn Sie die Methoden einer Schnittstelle verwenden, um Attribute in einer Datei zu ändern, sollten Sie davon ausgehen, dass alle zuvor von der anderen Schnittstelle abgerufenen Indexwerte nicht mehr gültig sind und erneut abgerufen werden müssen. Vermeiden Sie die Verwendung der Methoden von **iwmheaderinfo** , wenn dies möglich ist.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Arbeiten mit Metadaten**](working-with-metadata.md)
</dt> </dl>

 

 




