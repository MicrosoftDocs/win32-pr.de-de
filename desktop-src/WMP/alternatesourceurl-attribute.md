---
title: "\"Alternative\"-Attribut"
description: Das Attribut "appliesourceurl" ist ein einheitlicher ressourcenlocator für das Medien Element, das als Alternative zu den Attributen "dlnasourceuri" und "SourceUrl" fungiert.
ms.assetid: 2be88d9b-4fd8-4e70-9a4d-114a2bf8b23c
keywords:
- Media Player des alternativen ceurdeurl-Attributs
topic_type:
- apiref
api_name:
- AlternateSourceURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574a355dfa862c4db004fa2df942e464934a38ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364967"
---
# <a name="alternatesourceurl-attribute"></a>"Alternative"-Attribut

Das Attribut " **appliesourceurl** " ist ein einheitlicher ressourcenlocator für das Medien Element, das als Alternative zu den Attributen " [**dlnasourceuri**](dlnasourceuri-attribute.md) " und " [**SourceUrl**](sourceurl-attribute.md) " fungiert.

## <a name="applies-to"></a>Gilt für

-   [**Audioelemente**](audio-item-attributes.md)
-   [**Foto Elemente**](photo-item-attributes.md)
-   [**Wiedergabelisten Elemente**](playlist-attributes-ref.md)
-   [**Video Elemente**](video-item-attributes.md)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist für Medienelemente in der lokalen Bibliothek des aktuellen Benutzers nicht verfügbar. Sie ist nur für Medienelemente verfügbar, die zu einer Remote Bibliothek gehören. Das heißt, eine Bibliothek, die von einem anderen Benutzer im Heimnetzwerk verfügbar gemacht wurde. Um zu ermitteln, ob eine Medienbibliothek Remote ist, nennen Sie den [**\_ Typ iwmplibrary:: Get**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------|
| Version<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 





