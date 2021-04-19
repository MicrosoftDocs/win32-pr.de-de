---
title: Wiedergabeliste. AttributeName
description: Die AttributeName-Eigenschaft ruft den Namen eines Attributs an einem angegebenen Index ab.
ms.assetid: 3ff68e78-5fa1-4ca6-aa59-4752dbaee52a
keywords:
- Wiedergabeliste. AttributeName Windows Media Player
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
ms.openlocfilehash: 4560a7ca2766ee0bbadc582af878bca87e0834e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366692"
---
# <a name="playlistattributename"></a>Wiedergabeliste. AttributeName

Die **attributeName** -Eigenschaft ruft den Namen eines Attributs an einem angegebenen Index ab.

## <a name="syntax"></a>Syntax

*Player*. *currentwiedergabe*. **attributeName**( *Index* )

## <a name="parameters"></a>Parameter

*Index*

Die **Zahl** (**Long**), die den Index enthält.

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Die Anzahl der Attribute wird von der **AttributeCount** -Eigenschaft abgerufen. Bei einem Index gibt **attributeName** eine **Zeichenfolge** zurück, die zusammen mit "stiteminfo" oder " **getiteminfo** " verwendet werden kann, um einen Wert für das Attribut anzugeben oder abzurufen. 

Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.

Einen Beispielcode, der diese Eigenschaft verwendet, finden Sie unter der [AttributeCount](playlist-attributecount.md) -Eigenschaft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wiedergabelisten Objekt**](playlist-object.md)
</dt> <dt>

[**Wiedergabeliste. AttributeCount**](playlist-attributecount.md)
</dt> <dt>

[**Wiedergabeliste. getiteminfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Wiedergabeliste. Einstellungs Element**](playlist-setiteminfo.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





