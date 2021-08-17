---
title: WM/AlbumCoverURL-Attribut
description: Das WM/AlbumCoverURL-Attribut ist der Uniform Resource Locator (URL) für Albumart oder ein Miniaturbild.
ms.assetid: 0134867a-7c11-4d50-9ab5-b48c1ca6c473
keywords:
- WM/AlbumCoverURL-Attribut Windows Media Player
topic_type:
- apiref
api_name:
- WM/AlbumCoverURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3e3d2948419761a139139493e737df1a9a709147613eadd3e077f0f5101f3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332626"
---
# <a name="wmalbumcoverurl-attribute"></a>WM/AlbumCoverURL-Attribut

Das **WM/AlbumCoverURL-Attribut** ist der Uniform Resource Locator (URL) für Albumart oder ein Miniaturbild.

## <a name="applies-to"></a>Gilt für

-   [**Audioelemente**](audio-item-attributes.md)
-   [**Fotoelemente**](photo-item-attributes.md)
-   [**Videoelemente**](video-item-attributes.md)

## <a name="remarks"></a>Hinweise

Bei einem Audioelement ist dieses Attribut die URL der Albumart. Bei einem Foto- oder Videoelement ist dieses Attribut die URL eines Miniaturbilds.

Dieses Attribut ist für Medienelemente in der lokalen Bibliothek des aktuellen Benutzers nicht verfügbar. Sie ist nur für Medienelemente verfügbar, die zu einer Remotebibliothek gehören. Das heißt, eine Bibliothek, die von einem anderen Benutzer im Heimnetzwerk zur Verfügung gestellt wurde. Um zu bestimmen, ob es sich bei einer Medienbibliothek um eine Remotebibliothek handelt, rufen [**Sie IWMPLibrary::get \_ type auf.**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------|
| Version<br/> | Windows Media Player 12 oder höher.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributverweis**](attribute-reference.md)
</dt> </dl>

 

 





