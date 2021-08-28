---
title: Entfernen von Metadatenattributen
description: Entfernen von Metadatenattributen
ms.assetid: 44546091-406f-4ae6-914a-942d1b89e0e4
keywords:
- Windows Medienformat-SDK, Entfernen von Metadatenattributen
- Advanced Systems Format (ASF),Entfernen von Metadatenattributen
- ASF (Advanced Systems Format), Entfernen von Metadatenattributen
- Metadaten,Entfernen von Attributen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e09e00fbba8ca5464ccec570a03bbd4e30935238bc531d36ce220a60150839e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110210"
---
# <a name="removing-metadata-attributes"></a>Entfernen von Metadatenattributen

Sie können ein Metadatenattribut entfernen, indem Sie dessen Index- und Streamnummer an die [**IWMHeaderInfo3::D eleteAttribute-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute) übergeben. Die Reihenfolge, in der die verbleibenden Attribute nach dem Entfernen eines Attributs indiziert werden, ändert sich nicht. Alle verbleibenden Attribute, deren Indexwert ursprünglich größer als das entfernte war, haben ihre Indexwerte um eins reduziert. Wenn Sie mehrere Attribute entfernen, führen Sie dies in absteigender Reihenfolge nach Index durch, um zu vermeiden, dass die Anpassung bei der Indizierung berechnet werden muss.

Der Einfachheit halber gibt die [**IWMHeaderInfo3::GetAttributeIndices-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) die Indexwerte in absteigender Reihenfolge zurück.

> [!Note]  
> Indexwerte, die mithilfe der Methoden von [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) ermittelt werden, sind nicht kompatibel mit Indexwerten, die mithilfe der Methoden von [**IWMHeaderInfo ermittelt wurden.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) Wenn Sie die Methoden einer Schnittstelle verwenden, um Attribute in einer Datei zu ändern, sollten Sie davon ausgehen, dass alle zuvor von der anderen Schnittstelle abgerufenen Indexwerte nicht mehr gültig sind und erneut abgerufen werden müssen. Sie sollten die Verwendung der Methoden von **IWMHeaderInfo** nach Möglichkeit vermeiden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Arbeiten mit Metadaten**](working-with-metadata.md)
</dt> </dl>

 

 




