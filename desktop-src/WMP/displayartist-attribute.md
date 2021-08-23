---
title: DisplayArtist-Attribut
description: Das DisplayArtist-Attribut ist der Name des Interpreten, der für ein Element angezeigt wird.
ms.assetid: 8cf5a4e6-ce96-4fd4-b01a-6cd4264a5c09
keywords:
- DisplayArtist-Windows Media Player
topic_type:
- apiref
api_name:
- DisplayArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6c20e3d693aa7d5be5be0236d9eefebe7efcb70bc236db3f84389e5a3ceeccf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997320"
---
# <a name="displayartist-attribute"></a>DisplayArtist-Attribut

Das **DisplayArtist-Attribut** ist der Name des Interpreten, der für ein Element angezeigt wird.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)

## <a name="remarks"></a>Hinweise

Im Allgemeinen **hat DisplayArtist** den gleichen Wert wie das **WM/AlbumArtist-Attribut,** wenn dieses Attribut festgelegt wird. Andernfalls ist der Wert der Name des Interpreten, der dem ersten Titel des Albums zugeordnet ist.

Um zu bestimmen, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media.isReadOnlyItem-Methode.](media-isreadonlyitem.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------|
| Version<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributreferenz**](attribute-reference.md)
</dt> <dt>

[**WM/AlbumArtist-Attribut**](wm-albumartist-attribute.md)
</dt> </dl>

 

 





