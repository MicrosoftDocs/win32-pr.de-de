---
title: Attribut "Peer Wert"
description: Das peakvalue-Attribut ist ein 16-Bit-Amplitude-Wert, der die maximale Volumeebene angibt.
ms.assetid: 5d80a1f3-015c-4740-bd1c-f3bbf88a9df2
keywords:
- Media Player "Peer Value"-Attribut
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74fde522e043adb8b11c25bede763bed6b252f2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354787"
---
# <a name="peakvalue-attribute"></a>Attribut "Peer Wert"

Das **peakvalue** -Attribut ist ein 16-Bit-Amplitude-Wert, der die maximale Volumeebene angibt.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [Häufig verwendete Windows Media-Dateien](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist sowohl in der Bibliothek als auch in der digitalen Mediendatei gespeichert.

Dieser Wert wird von Windows Media Player in einer der folgenden Instanzen festgelegt:

-   Nachdem eine Datei durch eine Datei gerissen wurde.
-   Nachdem eine Datei wiedergegeben wurde (bei aktivierter Erweiterung für das automatische Volume).

Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszpeer Value.

Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 





