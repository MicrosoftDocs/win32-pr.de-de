---
title: Durchsuchbar
description: Das suchbare Attribut ist ein Attribut auf Dateiebene, das angibt, ob eine Anwendung auf Punkte innerhalb des Inhalts suchen kann.
ms.assetid: 9653e368-4782-4506-9c44-54c9406b61b5
keywords:
- Suchbares Windows Media-Format
topic_type:
- apiref
api_name:
- Seekable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4db701be363c194c75bd698062d79a0c0c407cc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104314500"
---
# <a name="seekable"></a>Durchsuchbar

Das suchbare Attribut ist **ein Attribut auf** Dateiebene, das angibt, ob eine Anwendung auf Punkte innerhalb des Inhalts suchen kann.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmseekable

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ \_ bool**

## <a name="remarks"></a>Bemerkungen

Dies ist ein codiertes Attribut.

Dieses Attribut kann nicht auf Dateiebene dupliziert werden. Wenn dieses Attribut für einen einzelnen Stream verwendet wird, wird es als benutzerdefinierte Metadaten behandelt und gibt seine normale Bedeutung nicht an die Objekte des Windows Media Format SDK aus.

Der Wert dieses Attributs für eine Datei kann variieren, je nachdem, welches Objekt die zum Abrufen verwendete [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) -oder [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) -Schnittstelle verfügbar macht. Dies liegt daran, dass die Reader-Objekte (sowohl synchrone als auch asynchron) eine gründlichere Überprüfung durchführen als das Metadateneditor-Objekt, um zu ermitteln, ob Sie einen Punkt in einer Datei suchen können. Der **von** einem Reader-Objekt zurückgegebene suchbare Attribut Wert ist präziser.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




