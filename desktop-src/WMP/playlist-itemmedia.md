---
title: Wiedergabeliste. itemmedia
description: Das itemmedia-Attribut ruft das Medienobjekt ab, das dem angegebenen Index im Wiedergabelisten Element entspricht.
ms.assetid: 38085798-7986-432f-8c88-de886bfc2ac5
keywords:
- Wiedergabeliste. itemmedia Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemMedia
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 269e9011ade69ee61d99c29c1fa5bd1b9fa3deeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360417"
---
# <a name="playlistitemmedia"></a>Wiedergabeliste. itemmedia

Das **itemmedia** -Attribut ruft das **Medien** Objekt ab, das dem angegebenen Index im **Wiedergabe** Listenelement entspricht.

``` syntax
        elementID.itemMedia(index)
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein Schreib geschütztes **Medien** Objekt.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Sin*
</dt> <dd>

**Zahl**(**Long**), die den Index eines Wiedergabelisten Elements enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **itemmedia** -Eigenschaft gibt Medienobjekte zurück, die im **Wiedergabe** Listenelement erweitert werden. Wenn beispielsweise eine Wiedergabeliste mit drei Medienclips vorhanden ist, die nicht im **Wiedergabe** Listenelement erweitert werden, gibt **itemmedia**(0) die Wiedergabeliste als Medienobjekt zurück. Wenn die Wiedergabeliste erweitert ist, gibt **itemmedia**(0) den ersten Medien Clip in der Wiedergabeliste zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Wiedergabelisten Element**](playlist-element.md)
</dt> </dl>

 

 





