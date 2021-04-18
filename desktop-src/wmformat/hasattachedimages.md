---
title: Hasattachedimages
description: Das hasattachedimages-Attribut ist ein Attribut auf Dateiebene, das angibt, ob es sich bei der Datei um eine MP3-Datei mit angefügten apischen ID3-Frames handelt
ms.assetid: 5c45f61c-3149-4b1b-b5de-f5817cc48c02
keywords:
- Hasattachedimages Windows Media-Format
topic_type:
- apiref
api_name:
- HasAttachedImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b89c8e8260bac7fa22c50460c57a77d4b3033e6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106339042"
---
# <a name="hasattachedimages"></a>Hasattachedimages

Das **hasattachedimages** -Attribut ist ein Attribut auf Dateiebene, das angibt, ob es sich bei der Datei um eine MP3-Datei mit angefügten apischen ID3-Frames handelt

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmhasattachedimages

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ \_ bool**

## <a name="remarks"></a>Bemerkungen

Dies ist ein codiertes Attribut.

Dieses Attribut kann nicht auf Dateiebene dupliziert werden. Wenn dieses Attribut für einen einzelnen Stream verwendet wird, wird es als benutzerdefinierte Metadaten behandelt und gibt seine normale Bedeutung nicht an die Objekte des Windows Media Format SDK aus.

**Hasattachedimages** wurde entwickelt, um eine Anwendung darüber zu informieren, dass Bilder vorhanden waren, damit Sie mithilfe der [**iwmimageingefo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) -Schnittstelle abgerufen werden können. Da nun Images mit dem [**WM/Bild-**](wmpicture.md) Attribut unterstützt werden, wird **hasattachedimages** nicht mehr benötigt.

Um zu ermitteln, ob eine Datei Bilder enthält, können Sie [**IWMHeaderInfo3:: getattributeindices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) aufrufen, die das **WM/Bild-** Attribut angeben.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




