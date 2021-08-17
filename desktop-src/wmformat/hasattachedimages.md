---
title: HasAttachedImages
description: Das HasAttachedImages-Attribut ist ein Attribut auf Dateiebene, das angibt, ob es sich bei der Datei um eine MP3-Datei mit angefügten APIC ID3-Frames handelt.
ms.assetid: 5c45f61c-3149-4b1b-b5de-f5817cc48c02
keywords:
- HasAttachedImages windows Media Format
topic_type:
- apiref
api_name:
- HasAttachedImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46ec38d0961ffc6ffc50434cdecf69e6dde663dfeaff5e331455a9575b3426e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930860"
---
# <a name="hasattachedimages"></a>HasAttachedImages

Das **HasAttachedImages-Attribut** ist ein Attribut auf Dateiebene, das angibt, ob es sich bei der Datei um eine MP3-Datei mit angefügten APIC ID3-Frames handelt.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMHasAttachedImages

## <a name="data-type"></a>Datentyp

**\_WMT-TYP \_ BOOL**

## <a name="remarks"></a>Hinweise

Dies ist ein codiertes Attribut.

Dieses Attribut kann nicht auf Dateiebene dupliziert werden. Wenn dieses Attribut für einen einzelnen Stream verwendet wird, wird es als benutzerdefinierte Metadaten behandelt und vermittelt den Objekten des Windows Media Format SDK nicht seine normale Bedeutung.

**HasAttachedImages** wurde entwickelt, um eine Anwendung darüber zu informieren, dass Bilder vorhanden sind, damit sie über die [**IWMImageInfo-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) abgerufen werden können. Da Images nun mithilfe des [**WM/Picture-Attributs**](wmpicture.md) unterstützt werden, wird **HasAttachedImages** nicht mehr benötigt.

Um zu bestimmen, ob eine Datei Bilder enthält, rufen Sie [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) auf, und geben Sie dabei das **WM/Picture-Attribut** an.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




