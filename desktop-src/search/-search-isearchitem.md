---
description: Stellt Methoden bereit, die die Interaktion zwischen einer Benutzeroberfläche (UI) und den vom Indexer erstellten Search-Namespaceobjekten definieren.
ms.assetid: e48c9e5b-9b15-4bc1-91ef-81ba7a05bfbd
title: ISearchItem-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem
api_type:
- COM
api_location: ''
ms.openlocfilehash: de3769f869838cd3a6660229a452ea7fbd96f943ac7421523c523662da205dac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863953"
---
# <a name="isearchitem-interface"></a>ISearchItem-Schnittstelle

Stellt Methoden bereit, die die Interaktion zwischen einer Benutzeroberfläche (UI) und den vom Indexer erstellten Search-Namespaceobjekten definieren.

## <a name="members"></a>Member

Die **ISearchItem-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ISearchItem** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ISearchItem-Schnittstelle** verfügt über diese Methoden.



| Methode                                                         | Beschreibung                                                                                                                               |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetParentFolder**](-search-isearchitem-getparentfolder.md) | Ruft das **ISearchItem-Objekt** ab, wenn die URL eine tatsächliche Shell-Datenquelle darstellt (auch als Shellnamespaceerweiterung bekannt).<br/> |
| [**GetUIObjectOf**](/previous-versions/windows/desktop/legacy/dd756721(v=vs.85))     | Ruft das Benutzeroberflächenobjekt von **ISearchItem ab.**<br/>                                                                        |



 

## <a name="remarks"></a>Hinweise

[**ISearchItem::GetParentFolder**](-search-isearchitem-getparentfolder.md) wird nur auf Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

Um eine Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern anzuzeigen, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die **ISearchItem-Schnittstelle** und die folgenden APIs zu verwenden: die [**Schnittstellen IItemPreviewerExt,**](-search-iitempreviewerext.md) [**IItemPropertyBag**](iitempropertybag.md)und [**ISearchProtocolUI,**](-search-isearchprotocolui.md) die [**LINKINFO-Struktur**](-search-linkinfo.md) und die [**LINKTYPE-Enumeration.**](-search-linktype.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 3.0<br/>          |



 

 
