---
title: Playlist.attributeCount
description: Die attributeCount-Eigenschaft ruft die Anzahl der Attribute ab, die der Wiedergabeliste zugeordnet sind.
ms.assetid: 92063131-0118-4458-9122-0539628a9821
keywords:
- Playlist.attributeCount-Windows Media Player
topic_type:
- apiref
api_name:
- Playlist.attributeCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63616096dbfc3989a93d3dc8010dd0ed1f256ccd9e9bf2cc7b3c825c88a63d0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054298"
---
# <a name="playlistattributecount"></a>Playlist.attributeCount

Die **attributeCount-Eigenschaft** ruft die Anzahl der Attribute ab, die der Wiedergabeliste zugeordnet sind.

## <a name="syntax"></a>Syntax

*Player*. *currentPlaylist*. **attributeCount**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**long**).

## <a name="remarks"></a>Hinweise

Da Wiedergabelisten aus vielen verschiedenen Quellen stammen können, können sie über mehrere unterschiedliche Eigenschaftensätze verfügen. Diese Methode ruft die Gesamtzahl der verfügbaren Eigenschaften ab, sodass die anderen Methoden des **Playlist-Objekts** darauf zugreifen können.

Um den Wert dieser Eigenschaft abzurufen, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

Informationen zu den attributen, die von Windows Media Player unterstützt werden, finden Sie in der Windows Media Player [Attributreferenz.](attribute-reference.md)

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird veranschaulicht, wie verschiedene Eigenschaften und Methoden der **Wiedergabelisten-** und **Medienobjekte** verwendet werden.


```JScript
function onLoad() {
    var display;
    var pl = player.currentPlaylist;

    pl.setItemInfo("custom playlist attribute", "changed");
    pl.item(0).setItemInfo("new custom attribute", "5");

    display = pl.attributeCount + " Playlist Attributes:\r\r";

    for (var i = 0; i < pl.attributeCount; ++i) {
        display = display + pl.attributeName(i) + ": ";
        display = display + pl.getItemInfo(pl.attributeName(i)) + "\r";
    }

    for (var j = 0; j < pl.count; ++j) {
        display = display + "\rTrack " + j + "\r"
        display = display + pl.item(j).attributeCount + " Attributes:\r\r";

        for (var k = 0; k < pl.item(j).attributeCount; ++k) {
            var it = pl.item(j);  // Media object
            display = display + it.getAttributeName(k) + ": ";
            display = display + it.getItemInfo(it.getAttributeName(k)) + "\r";
        }
    }

    myText.value = display;
}

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wiedergabelistenobjekt**](playlist-object.md)
</dt> <dt>

[**Playlist.attributeName**](playlist-attributename.md)
</dt> <dt>

[**Playlist.getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Playlist.setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





