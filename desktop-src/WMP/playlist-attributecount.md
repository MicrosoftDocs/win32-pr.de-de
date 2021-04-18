---
title: Wiedergabeliste. AttributeCount
description: Die AttributeCount-Eigenschaft ruft die Anzahl der Attribute ab, die der Wiedergabeliste zugeordnet sind.
ms.assetid: 92063131-0118-4458-9122-0539628a9821
keywords:
- Wiedergabeliste. AttributeCount Windows Media Player
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
ms.openlocfilehash: 8e42d72e029f232bb6dabc074b412406a1bb64c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368594"
---
# <a name="playlistattributecount"></a>Wiedergabeliste. AttributeCount

Die **AttributeCount** -Eigenschaft ruft die Anzahl der Attribute ab, die der Wiedergabeliste zugeordnet sind.

## <a name="syntax"></a>Syntax

*Player*. *currentwiedergabe*. **AttributeCount**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).

## <a name="remarks"></a>Bemerkungen

Da Wiedergabelisten aus vielen verschiedenen Quellen stammen können, können Sie mehrere verschiedene Gruppen von Eigenschaften haben. Diese Methode ruft die Gesamtzahl der verfügbaren Eigenschaften ab, sodass die anderen Methoden des **Wiedergabe** Listen Objekts darauf zugreifen können.

Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird veranschaulicht, wie verschiedene Eigenschaften und Methoden der **Wiedergabeliste** und der **Medien** Objekte verwendet werden.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wiedergabelisten Objekt**](playlist-object.md)
</dt> <dt>

[**Wiedergabeliste. AttributeName**](playlist-attributename.md)
</dt> <dt>

[**Wiedergabeliste. getiteminfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Wiedergabeliste. Einstellungs Element**](playlist-setiteminfo.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





