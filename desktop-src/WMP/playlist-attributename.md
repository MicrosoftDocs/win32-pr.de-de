---
title: Playlist.attributeName
description: Die attributeName-Eigenschaft ruft den Namen eines Attributs an einem angegebenen Index ab.
ms.assetid: 3ff68e78-5fa1-4ca6-aa59-4752dbaee52a
keywords:
- Playlist.attributeName-Windows Media Player
topic_type:
- apiref
api_name:
- Playlist.attributeName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 695e0ee00aca0fe7743a028e0e7830e1839c0b2f89b42a94e9ce1dbe29ef35ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003210"
---
# <a name="playlistattributename"></a>Playlist.attributeName

Die **attributeName-Eigenschaft** ruft den Namen eines Attributs an einem angegebenen Index ab.

## <a name="syntax"></a>Syntax

*Player*. *currentPlaylist*. **attributeName**( *Index* )

## <a name="parameters"></a>Parameter

*Index*

**Number** (**long**), die den Index enthält.

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge.**

## <a name="remarks"></a>Hinweise

Die Anzahl der Attribute wird von der **attributeCount-Eigenschaft** abgerufen. Bei einem Index gibt **attributeName** eine **Zeichenfolge** zurück, die in Verbindung mit **setItemInfo** oder **getItemInfo** verwendet werden kann, um einen Wert für das Attribut anzugeben oder abzurufen.

Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

Informationen zu den attributes, die von Windows Media Player unterstützt werden, finden Sie in der Windows Media Player [Attribute Reference](attribute-reference.md).

[Beispielcode, der diese Eigenschaft](playlist-attributecount.md) verwendet, finden Sie in der attributeCount-Eigenschaft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wiedergabelistenobjekt**](playlist-object.md)
</dt> <dt>

[**Playlist.attributeCount**](playlist-attributecount.md)
</dt> <dt>

[**Playlist.getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Playlist.setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





