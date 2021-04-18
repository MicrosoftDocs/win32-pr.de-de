---
title: WM/albumcoverurl-Attribut
description: Das WM/albumcoverurl-Attribut ist die URL (Uniform Resource Serverlocatorpunkt) für Albumkunst oder ein Miniaturbild.
ms.assetid: 0134867a-7c11-4d50-9ab5-b48c1ca6c473
keywords:
- WM/albumcoverurl-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- WM/AlbumCoverURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939c5451f3ae8f41214a817293e3c7f3cb3b66c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357637"
---
# <a name="wmalbumcoverurl-attribute"></a>WM/albumcoverurl-Attribut

Das **WM/albumcoverurl-** Attribut ist die URL (Uniform Resource Serverlocatorpunkt) für Albumkunst oder ein Miniaturbild.

## <a name="applies-to"></a>Gilt für

-   [**Audioelemente**](audio-item-attributes.md)
-   [**Foto Elemente**](photo-item-attributes.md)
-   [**Video Elemente**](video-item-attributes.md)

## <a name="remarks"></a>Bemerkungen

Bei einem Audioelement ist dieses Attribut die URL der Albumgrafik. Bei einem Foto-oder Video Element ist dieses Attribut die URL eines Miniatur Bilds.

Dieses Attribut ist für Medienelemente in der lokalen Bibliothek des aktuellen Benutzers nicht verfügbar. Sie ist nur für Medienelemente verfügbar, die zu einer Remote Bibliothek gehören. Das heißt, eine Bibliothek, die von einem anderen Benutzer im Heimnetzwerk verfügbar gemacht wurde. Um zu ermitteln, ob eine Medienbibliothek Remote ist, nennen Sie den [**\_ Typ iwmplibrary:: Get**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------|
| Version<br/> | Windows Media Player 12 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 





