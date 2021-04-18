---
title: WM/Year-Attribut
description: Das WM/Year-Attribut ist das Jahr, an dem der Inhalt veröffentlicht wurde.
ms.assetid: b64e37f1-6f12-43a6-8a66-7d61b470853c
keywords:
- WM/Jahr-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- WM/Year
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10bf10d4e905e10c74cfaf9986445ce9a68dc9b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361328"
---
# <a name="wmyear-attribute"></a>WM/Year-Attribut

Das **WM/Year-** Attribut ist das Jahr, an dem der Inhalt veröffentlicht wurde.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [Häufig verwendete Windows Media-Dateiattribute](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird nur in der digitalen Mediendatei gespeichert.

Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.

Dieses Attribut sollte nicht als Teil einer Abfrage Bedingung verwendet werden. Sie wird von einem anderen Attribut abgeleitet und kann in einer Medien Auflistung nicht direkt abgefragt werden.

Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszwmyear.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie Windows Media Player 10 oder höher unterstützt dieses Attribut nicht.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 





