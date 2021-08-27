---
title: WM/Language-Attribut
description: Das WM/Language-Attribut ist die Sprache des Elements.
ms.assetid: aebfb518-61ca-4b75-875a-ce2127a74b67
keywords:
- WM/Language Attribute Windows Media Player
topic_type:
- apiref
api_name:
- WM/Language
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8902d36ebe9e8227d22f55273e8351d7ed09c592953b44a31e45c06b838f9871
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122650"
---
# <a name="wmlanguage-attribute"></a>WM/Language-Attribut

Das **WM/Language-Attribut** ist die Sprache des Elements.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [Häufig verwendete Windows Mediendateiattribute](commonly-used-windows-media-file-attributes.md)
-   [Optionselemente](radio-item-attributes.md)
-   [Videoelemente](video-item-attributes.md)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird sowohl in der Bibliothek als auch in der digitalen Mediendatei gespeichert.

Dieses Attribut kann mehrere Werte haben. Um alle Werte für ein mehrwertiges Attribut abzurufen, müssen Sie die **Media.getItemInfoByType-Methode** und nicht die **Media.getItemInfo-Methode** verwenden.

**Language** ist ein Alias für dieses Attribut.

Die Windows Media Format SDK-Konstante für dieses Attribut ist g \_ wszWMLanguage.

Um zu bestimmen, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media.isReadOnlyItem-Methode.](media-isreadonlyitem.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9er Serie oder höher (das Optionselement wird nur in der 9 Windows Media Player Unterstützt)<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributreferenz**](attribute-reference.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





