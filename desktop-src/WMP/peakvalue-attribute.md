---
title: PeakValue-Attribut
description: Das PeakValue-Attribut ist ein 16-Bit-Amplitudenwert, der die Spitzenvolumenebene angibt.
ms.assetid: 5d80a1f3-015c-4740-bd1c-f3bbf88a9df2
keywords:
- PeakValue-Attribut Windows Media Player
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa2a661342b305155717f4f11336f540e1ae53524ff2d303a2ab790e2c73af7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118573584"
---
# <a name="peakvalue-attribute"></a>PeakValue-Attribut

Das **PeakValue-Attribut** ist ein 16-Bit-Amplitudenwert, der die Spitzenvolumenebene angibt.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [Häufig verwendete Windows Mediendateien](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird sowohl in der Bibliothek als auch in der digitalen Mediendatei gespeichert.

Windows Media Player legt diesen Wert in einer der folgenden Instanzen fest:

-   Nachdem eine Datei gezippt wurde.
-   Nachdem eine Datei abgespielt wurde (wenn die Erweiterung für automatisches Volumeleveling aktiviert ist).

Die Windows Media Format SDK-Konstante für dieses Attribut ist g \_ wszPeakValue.

Um zu bestimmen, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media.isReadOnlyItem-Methode.](media-isreadonlyitem.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9er Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributreferenz**](attribute-reference.md)
</dt> </dl>

 

 





