---
title: Averagelevel-Attribut
description: Das averagelevel-Attribut ist ein 16-Bit-Amplitude-Wert, der die durchschnittliche Volumeebene angibt.
ms.assetid: 04ff19f1-a9a5-4e47-86a6-50c6f08b0d7d
keywords:
- Averagelevel-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594612f3675d818f94270b1952d2a9ca7bed15d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366940"
---
# <a name="averagelevel-attribute"></a>Averagelevel-Attribut

Das **averagelevel** -Attribut ist ein 16-Bit-Amplitude-Wert, der die durchschnittliche Volumeebene angibt.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [Häufig verwendete Windows Media-Dateien](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist sowohl in der Bibliothek als auch in der digitalen Mediendatei gespeichert.

Dieser Wert wird von Windows Media Player in einer der folgenden Instanzen festgelegt:

-   Nachdem eine Datei durch eine Datei gerissen wurde.
-   Nachdem eine Datei wiedergegeben wurde (bei aktivierter Erweiterung für das automatische Volume).

Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszaveragelevel.

Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 





