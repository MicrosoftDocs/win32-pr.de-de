---
title: Dlnasourceuri-Attribut
description: Das dlnasourceuri-Attribut ist der universelle Ressourcen Bezeichner (URI) des Elements.
ms.assetid: 323c897b-9b76-44f7-9313-c51595589583
keywords:
- Dlnasourceuri-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- DLNASourceURI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ebe21a39a67dec9356c5dd5360efb48f4ef029
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366033"
---
# <a name="dlnasourceuri-attribute"></a>Dlnasourceuri-Attribut

Das **dlnasourceuri** -Attribut ist der universelle Ressourcen Bezeichner (URI) des Elements.

## <a name="applies-to"></a>Gilt für

-   [**Audioelemente**](audio-item-attributes.md)
-   [**Andere Elemente**](other-item-attributes.md)
-   [**Foto Elemente**](photo-item-attributes.md)
-   [**Wiedergabelisten Elemente**](playlist-attributes-ref.md)
-   [**Video Elemente**](video-item-attributes.md)

## <a name="remarks"></a>Bemerkungen

Wenn sich das Element in der lokalen Bibliothek des aktuellen Benutzers befindet, sind dieses Attribut, das [**SourceUrl**](sourceurl-attribute.md) -Attribut und der von [**iwmpmedia:: get \_ SourceUrl**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl) zurückgegebene Wert identisch.

Wenn sich das Element nicht in der lokalen Bibliothek des aktuellen Benutzers befindet, aber zu einer Remote Bibliothek gehört, ist dieses Attribut ein Bezeichner der Form DLNA-playsingle://*xxx*.

Sie können einen DLNA-playsingle-URI an die [**IWMPCore3:: newmedia**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore3-newmedia) -Methode übergeben, um eine [**iwmpmedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) -Schnittstelle zu erhalten, die es Ihnen ermöglicht, die Metadaten des Medien Elements anzuzeigen und ggf. die Stern Bewertung des Medien Elements zu bearbeiten. Beachten Sie jedoch, dass der DLNA-playsingle-URI für einen Inhaltsverzeichnis Dienst (CDs) gelten muss, den Windows Media Player bereits ermittelt hat. Die **newmedia** -Methode initiiert keine UPnP-Ermittlung und sucht nach den CDs.

Sie können die Stern Bewertung eines Medien Elements nur in einer Remote Bibliothek bearbeiten, wenn die Remote Bibliothek den Bearbeitungsvorgang unterstützt. Remote Bibliotheken, die auf einem Computer unter Windows 7 gehostet werden, unterstützen den Bearbeitungsvorgang. Bei Remote Bibliotheken, die auf einem Computer mit einem älteren Windows-Betriebssystem als Windows 7 gehostet werden, wird der Bearbeitungsvorgang nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------|
| Version<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 





