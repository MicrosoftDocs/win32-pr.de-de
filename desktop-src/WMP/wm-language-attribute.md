---
title: WM/Language-Attribut
description: Das WM/Language-Attribut ist die Sprache des Elements.
ms.assetid: aebfb518-61ca-4b75-875a-ce2127a74b67
keywords:
- WM/sprach Attribut Fenster Media Player
topic_type:
- apiref
api_name:
- WM/Language
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172cc8498bf5360e29822a484bcc2ddacd70b8b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359320"
---
# <a name="wmlanguage-attribute"></a>WM/Language-Attribut

Das **WM/Language-** Attribut ist die Sprache des Elements.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [Häufig verwendete Windows Media-Dateiattribute](commonly-used-windows-media-file-attributes.md)
-   [Options Felder](radio-item-attributes.md)
-   [Video Elemente](video-item-attributes.md)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist sowohl in der Bibliothek als auch in der digitalen Mediendatei gespeichert.

Dieses Attribut kann mehrere Werte aufweisen. Wenn Sie alle Werte für ein mehr wertiges Attribut abrufen möchten, müssen Sie die Media. **getItemInfoByType** -Methode und nicht die **Media. getiteminfo** -Methode verwenden.

**Language** ist ein Alias für dieses Attribut.

Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszwmlanguage.

Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher (das Optionsfeld wird nur in Windows Media Player 9-Serie unterstützt)<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





