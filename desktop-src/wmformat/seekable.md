---
title: Seekable
description: Das Seekable-Attribut ist ein Attribut auf Dateiebene, das angibt, ob eine Anwendung nach Punkten innerhalb des Inhalts suchen kann.
ms.assetid: 9653e368-4782-4506-9c44-54c9406b61b5
keywords:
- Suchbare Fenster – Medienformat
topic_type:
- apiref
api_name:
- Seekable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a254d06b36230bb6920f2f13d646edc5f1cdac75efe15864e0c84ba847cf50f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699986"
---
# <a name="seekable"></a>Seekable

Das **Seekable-Attribut** ist ein Attribut auf Dateiebene, das angibt, ob eine Anwendung nach Punkten innerhalb des Inhalts suchen kann.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMSeekable

## <a name="data-type"></a>Datentyp

**\_WMT-TYP \_ BOOL**

## <a name="remarks"></a>Hinweise

Dies ist ein codiertes Attribut.

Dieses Attribut kann nicht auf Dateiebene dupliziert werden. Wenn dieses Attribut für einen einzelnen Stream verwendet wird, wird es als benutzerdefinierte Metadaten behandelt und vermittelt den Objekten des Windows Media Format SDK nicht seine normale Bedeutung.

Der Wert dieses Attributs für eine Datei kann abhängig von dem Objekt variieren, das die [**IWMHeaderInfo-**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) oder [**IWMHeaderInfo3-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) verfügbar macht, die zum Abrufen verwendet wird. Dies liegt daran, dass die Readerobjekte (sowohl synchron als auch asynchron) eine gründlichere Überprüfung durchführen als das Metadaten-Editor-Objekt, um festzustellen, ob Sie zu einem Punkt in einer Datei suchen können. Der von einem Readerobjekt zurückgegebene **Seekable-Attributwert** ist genauer.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




