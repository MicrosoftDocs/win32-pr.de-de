---
title: DLNASourceURI-Attribut
description: Das DLNASourceURI-Attribut ist der URI (Universal Resource Identifier) des Elements.
ms.assetid: 323c897b-9b76-44f7-9313-c51595589583
keywords:
- DLNASourceURI-Attribut Windows Media Player
topic_type:
- apiref
api_name:
- DLNASourceURI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07e5383de75fef1a0e1957f270a8a5238951bce4ede1418dbf79ba2038777372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997170"
---
# <a name="dlnasourceuri-attribute"></a>DLNASourceURI-Attribut

Das **DLNASourceURI-Attribut** ist der URI (Universal Resource Identifier) des Elements.

## <a name="applies-to"></a>Gilt für

-   [**Audioelemente**](audio-item-attributes.md)
-   [**Andere Elemente**](other-item-attributes.md)
-   [**Fotoelemente**](photo-item-attributes.md)
-   [**Wiedergabelistenelemente**](playlist-attributes-ref.md)
-   [**Videoelemente**](video-item-attributes.md)

## <a name="remarks"></a>Hinweise

Wenn sich das Element in der lokalen Bibliothek des aktuellen Benutzers befindet, sind dieses Attribut, das [**SourceURL-Attribut**](sourceurl-attribute.md) und der von [**IWMPMedia::get \_ sourceURL**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl) zurückgegebene Wert identisch.

Wenn sich das Element nicht in der lokalen Bibliothek des aktuellen Benutzers befindet, sondern zu einer Remotebibliothek gehört, ist dieses Attribut ein Bezeichner im Format dlna-playsingle://*xxx*.

Sie können einen dlna-playsingle-URI an die [**IWMPCore3::newMedia-Methode**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore3-newmedia) übergeben, um eine [**IWMPMedia-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) abzurufen, mit der Sie die Metadaten des Medienelements anzeigen und möglicherweise die Sternbewertung des Medienelements bearbeiten können. Beachten Sie jedoch, dass der dlna-playsingle-URI für einen Inhaltsverzeichnisdienst (Content Directory Service, CDS) sein muss, der Windows Media Player bereits ermittelt hat. Die **newMedia-Methode** initiiert keine UPnP-Ermittlung und sucht nicht nach dem CDS.

Sie können die Sternbewertung eines Medienelements in einer Remotebibliothek nur bearbeiten, wenn die Remotebibliothek den Bearbeitungsvorgang unterstützt. Remotebibliotheken, die auf einem Computer mit Windows 7 gehostet werden, unterstützen den Bearbeitungsvorgang. Remotebibliotheken, die auf einem Computer gehostet werden, auf dem ein Windows Betriebssystem vor Windows 7 ausgeführt wird, unterstützen den Bearbeitungsvorgang nicht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------|
| Version<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributverweis**](attribute-reference.md)
</dt> </dl>

 

 





