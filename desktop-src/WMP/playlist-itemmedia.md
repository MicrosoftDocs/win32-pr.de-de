---
title: PLAYLIST.itemMedia
description: Das itemMedia-Attribut ruft das Media-Objekt ab, das dem angegebenen Index im PLAYLIST-Element entspricht.
ms.assetid: 38085798-7986-432f-8c88-de886bfc2ac5
keywords:
- PLAYLIST.itemMedia-Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemMedia
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52b3061ef83ec246878d51528e88a12b4f10dcb3085f584a2266dc64a163b866
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746866"
---
# <a name="playlistitemmedia"></a>PLAYLIST.itemMedia

Das **itemMedia-Attribut** ruft das **Media-Objekt** ab, das dem angegebenen Index im **PLAYLIST-Element entspricht.**

``` syntax
        elementID.itemMedia(index)
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein schreibgeschütztes **Medienobjekt.**

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Index*
</dt> <dd>

**Zahl**(**long**), die den Index eines Wiedergabelistenelements enthält.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **itemMedia-Eigenschaft** gibt Medienobjekte zurück, die im **PLAYLIST-Element** erweitert werden. Wenn beispielsweise eine Wiedergabeliste mit drei Medienclips vorhanden ist, die im **PLAYLIST-Element** nicht erweitert ist, gibt **itemMedia**(0) die Wiedergabeliste als Medienobjekt zurück. Wenn die Wiedergabeliste erweitert ist, gibt **itemMedia**(0) den ersten Medienclip in der Wiedergabeliste zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9er Serie oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**PLAYLIST-Element**](playlist-element.md)
</dt> </dl>

 

 





