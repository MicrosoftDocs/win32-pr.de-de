---
title: WM/wmcontentid-Attribut
description: Das WM/wmcontentid-Attribut ist eine GUID, die den Inhalt des Elements identifiziert.
ms.assetid: 1e741286-cdd8-4c2f-8fef-5d91d81d6387
keywords:
- WM/wmcontentid-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- WM/WMContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04366991a37b727f2693bc42ce2050139ce5c211
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354653"
---
# <a name="wmwmcontentid-attribute"></a>WM/wmcontentid-Attribut

Das **WM/wmcontentid-** Attribut ist eine GUID, die den Inhalt des Elements identifiziert.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [CD-Spuren](cd-track-attributes.md)
-   [Häufig verwendete Windows Media-Dateiattribute](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist sowohl in der Bibliothek (oder im Cache) als auch in der digitalen Mediendatei gespeichert.

**Wmcontentid** ist ein Alias für dieses Attribut.

Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszwmcontentid.

Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 





