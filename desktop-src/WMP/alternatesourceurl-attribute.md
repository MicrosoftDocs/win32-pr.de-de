---
title: AlternateSourceURL-Attribut
description: Das AlternateSourceURL-Attribut ist ein einheitlicher Ressourcenlocator für das Medienelement, der als Alternative zu den Attributen DLNASourceURI und SourceURL dient.
ms.assetid: 2be88d9b-4fd8-4e70-9a4d-114a2bf8b23c
keywords:
- AlternateSourceURL-Attribut Windows Media Player
topic_type:
- apiref
api_name:
- AlternateSourceURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765c7a3945224e82a0112c0f4dd7249e4340ec13e0d78adbd59039d25f234aaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055238"
---
# <a name="alternatesourceurl-attribute"></a>AlternateSourceURL-Attribut

Das **AlternateSourceURL-Attribut** ist ein einheitlicher Ressourcenlocator für das Medienelement, der als Alternative zu den [**Attributen DLNASourceURI**](dlnasourceuri-attribute.md) und [**SourceURL**](sourceurl-attribute.md) dient.

## <a name="applies-to"></a>Gilt für

-   [**Audioelemente**](audio-item-attributes.md)
-   [**Fotoelemente**](photo-item-attributes.md)
-   [**Wiedergabelistenelemente**](playlist-attributes-ref.md)
-   [**Videoelemente**](video-item-attributes.md)

## <a name="remarks"></a>Hinweise

Dieses Attribut ist für Medienelemente in der lokalen Bibliothek des aktuellen Benutzers nicht verfügbar. Sie ist nur für Medienelemente verfügbar, die zu einer Remotebibliothek gehören. das heißt, eine Bibliothek, die von einem anderen Benutzer im Heimnetzwerk zur Verfügung gestellt wurde. Um zu bestimmen, ob eine Medienbibliothek remote ist, rufen Sie [**IWMPLibrary::get \_ type auf.**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------|
| Version<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributreferenz**](attribute-reference.md)
</dt> </dl>

 

 





