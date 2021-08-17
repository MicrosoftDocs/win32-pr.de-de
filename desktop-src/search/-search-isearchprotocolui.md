---
description: Stellt eine Methode zum Aufrufen von ISearchItem-Objekten bereit.
ms.assetid: b52fd64b-b03a-4d02-a64f-201f6b7d5045
title: ISearchProtocolUI-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4794c0a2de43c08645af5ea7d44d0dbd872fe6fc88c33f5fcdb830955fc594be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463015"
---
# <a name="isearchprotocolui-interface"></a>ISearchProtocolUI-Schnittstelle

Stellt eine Methode zum Aufrufen von [**ISearchItem-Objekten**](-search-isearchitem.md) bereit. Methoden in dieser Schnittstelle werden vom Protokollhost aufgerufen, wenn URLs vom Gatherer verarbeitet werden. Der Protokollhandler implementiert das Protokoll für den Zugriff auf eine Inhaltsquelle im systemeigenen Format, und diese Schnittstelle implementiert einen benutzerdefinierten Protokollhandler, um die Datenquellen zu erweitern, die indiziert werden können.

## <a name="members"></a>Member

Die **ISearchProtocolUI-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ISearchProtocolUI** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ISearchProtocolUI-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                       | BESCHREIBUNG                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSearchItemForUrl**](-search-isearchprotocolui-getsearchitemforurl.md) | Ruft das Suchelement für die angegebenen Daten ab. Diese Methode wird einmal für jede vom Gatherer verarbeitete URL aufgerufen und ruft einen Zeiger auf das [**ISearchItem-Objekt**](-search-isearchitem.md) ab. <br/> |



 

## <a name="remarks"></a>Hinweise

Die **ISearchProtocolUI-Schnittstelle** wird nur auf Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die **ISearchProtocolUI-Schnittstelle** und die folgenden APIs zu verwenden: [**die Schnittstellen IItemPreviewerExt,**](-search-iitempreviewerext.md) [**IItemPropertyBag**](iitempropertybag.md) und [**ISearchItem,**](-search-isearchitem.md) die [**LINKINFO-Struktur**](-search-linkinfo.md) und die [**LINKTYPE-Enumeration.**](-search-linktype.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 3.0<br/>          |



 

 
