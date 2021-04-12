---
description: Stellt Methoden bereit, die die Interaktion zwischen einer Benutzeroberfläche (UI) und den durch den Indexer erstellten suchnamespace-Objekten definieren.
ms.assetid: e48c9e5b-9b15-4bc1-91ef-81ba7a05bfbd
title: Isearchitem-Schnittstelle
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
ms.openlocfilehash: c6c0fd5b534c13f8fae2e6759645ac812fc3986c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393462"
---
# <a name="isearchitem-interface"></a>Isearchitem-Schnittstelle

Stellt Methoden bereit, die die Interaktion zwischen einer Benutzeroberfläche (UI) und den durch den Indexer erstellten suchnamespace-Objekten definieren.

## <a name="members"></a>Member

Die **isearchitem** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Isearchitem** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **isearchitem** -Schnittstelle verfügt über diese Methoden.



| Methode                                                         | BESCHREIBUNG                                                                                                                               |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getpartfolder**](-search-isearchitem-getparentfolder.md) | Ruft das **isearchitem** -Objekt ab, wenn die URL eine tatsächliche shelldatenquelle darstellt (wird auch als Shellnamespace-Erweiterung bezeichnet).<br/> |
| [**Getuiobjectof**](/previous-versions/windows/desktop/legacy/dd756721(v=vs.85))     | Ruft das Benutzeroberflächen Objekt (UI) von **isearchitem** ab.<br/>                                                                        |



 

## <a name="remarks"></a>Bemerkungen

[**Isearchitem:: getzientfolder**](-search-isearchitem-getparentfolder.md) wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, kann es erforderlich sein, die **isearchitem** -Schnittstelle und die folgenden APIs zu verwenden: die Schnittstellen [**iitempreviewerext**](-search-iitempreviewerext.md), [**iitempropertybag**](iitempropertybag.md)und [**isearchprotocolui**](-search-isearchprotocolui.md) , die [**linkinfo**](-search-linkinfo.md) -Struktur und die [**linktype**](-search-linktype.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 3,0<br/>          |



 

 
