---
title: IWMPPlaylist (VB und C )-Schnittstelle (Wmp.h)
description: Bietet Eigenschaften und Methoden zum Organisieren, Verwalten und Bearbeiten von Medienelementen in einer Wiedergabeliste. Die IWMPPlaylist-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: c3f4f9dd-eb5f-493a-b8d0-22e70c63a2d1
keywords:
- IWMPPlaylist-Schnittstelle (VB und C) Windows Media Player
- IWMPPlaylist -Schnittstelle (VB und C) Windows Media Player , beschrieben
topic_type:
- apiref
api_name:
- IWMPPlaylist (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3fc1d8be09596d89dd87748811846d6dee1e8af8f28bebec56fa852c42ed6bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119004"
---
# <a name="iwmpplaylist-vb-and-c-interface"></a>IWMPPlaylist-Schnittstelle (VB und C#)

Bietet Eigenschaften und Methoden zum Organisieren, Verwalten und Bearbeiten von Medienelementen in einer Wiedergabeliste.

Die **IWMPPlaylist-Schnittstelle** macht die folgenden Eigenschaften verfügbar.

## <a name="members"></a>Member

Die **IWMPPlaylist-Schnittstelle (VB und C#)** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IWMPPlaylist-Schnittstelle (VB und C#)** verfügt über diese Methoden.



| Methode                                                                       | Beschreibung                                                             |
|:-----------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**appendItem**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)   | Fügt am Ende der Wiedergabeliste ein Medienelement hinzu.<br/>                |
| [**Klar**](iwmpplaylist-iwmpplaylist-clear--vb-and-c.md)                   | Für die zukünftige Verwendung reserviert.<br/>                                     |
| [**getItemInfo**](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) | Gibt den Wert eines Wiedergabelistenattributs zurück, das durch den Namen angegeben wird.<br/> |
| [**insertItem**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)   | Fügt ein Medienelement an einer angegebenen Position in eine Wiedergabeliste ein.<br/>  |
| [**moveItem**](wmplibiwmpplaylist-iwmpplaylist-moveitem--vb-and-c.md)       | Ändert den Speicherort eines Medienelements in der Wiedergabeliste.<br/>        |
| [**removeItem**](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)   | Entfernt das angegebene Medienelement aus der Wiedergabeliste.<br/>          |
| [**setItemInfo**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md) | Legt den Wert eines Wiedergabelistenattributs fest.<br/>                      |



 

### <a name="properties"></a>Eigenschaften

Die **IWMPPlaylist-Schnittstelle (VB und C#)** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                      | Zugriffstyp           | Beschreibung                                                                                                                                         |
|:----------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attributeCount**](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)<br/> | Schreibgeschützt<br/>  | Ruft die Anzahl von Attributen ab, die einer Wiedergabeliste zugeordnet sind.<br/>                                                                                |
| [**Attributename**](iwmpplaylist-attributename--vb-and-c.md)<br/>                      | Schreibgeschützt<br/>  | Ruft den Namen eines Wiedergabelistenattributs ab, das von einem Index angegeben wird. In C# ist dies die get \_ attributeName-Methode.<br/>                               |
| [**Count**](wmplibiwmpplaylist-iwmpplaylist-count--vb-and-c.md)<br/>                   | Schreibgeschützt<br/>  | Ruft die Anzahl der Medienelemente in einer Wiedergabeliste ab.<br/>                                                                                            |
| [**isIdentical**](iwmpplaylist-isidentical--vb-and-c.md)<br/>                          | Schreibgeschützt<br/>  | Ruft einen Wert ab, der angibt, ob die angegebene Wiedergabeliste mit der aktuellen Wiedergabeliste identisch ist. In C# ist dies die get \_ isIdentical-Methode.<br/> |
| [**Element**](iwmpplaylist-item--vb-and-c.md)<br/>                                        | Schreibgeschützt<br/>  | Ruft eine Schnittstelle zum Medienelement am angegebenen Index ab. In C# ist dies die get \_ Item-Methode.<br/>                                         |
| [**Namen**](wmplibiwmpplaylist-iwmpplaylist-name--vb-and-c.md)<br/>                     | Lesen/Schreiben<br/> | Ruft den Namen der Wiedergabeliste ab oder legt den Namen fest.<br/>                                                                                                   |



 

Verwenden Sie die folgenden Eigenschaften oder Methoden, auf die über das folgende Objekt oder die folgende Schnittstelle zugegriffen wird, um eine **IWMPPlaylist-Schnittstelle** zu erhalten.



| Objekt oder Schnittstelle                                                | Eigenschaft oder Methode                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMPC wie**](iwmpcdrom--vb-and-c.md)                           | [**Wiedergabeliste**](wmplibiwmpcdrom-iwmpcdrom-playlist--vb-and-c.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**IWMPMediaCollection**](iwmpmediacollection--vb-and-c.md)       | [**getAll,**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md) [**getByAttribute,**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum) [**getByAttribute,**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md) [**getByAuthor,**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md) [**getByGenre,**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md) [**getByName**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md) |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md)  | [**currentPlaylist,**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md) [ **newPlaylist**](axwmplib-axwindowsmediaplayer-newplaylist.md)                                                                                                                                                                                                                                                                                                                                                                   |
| [**IWMPPlaylistArray**](iwmpplaylistarray--vb-and-c.md)           | [**Element**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistarray-item)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**IWMPPlaylistCollection**](iwmpplaylistcollection--vb-and-c.md) | [**newPlaylist**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-newplaylist)                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Schnittstellen für Visual Basic .NET und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





