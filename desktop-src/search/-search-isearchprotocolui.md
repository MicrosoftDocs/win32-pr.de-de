---
description: Stellt eine Methode zum Aufrufen von isearchitem-Objekten bereit.
ms.assetid: b52fd64b-b03a-4d02-a64f-201f6b7d5045
title: Isearchprotocolui-Schnittstelle
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
ms.openlocfilehash: 3923ddaff014d393690be31c0e0ca2be94a3cb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356711"
---
# <a name="isearchprotocolui-interface"></a>Isearchprotocolui-Schnittstelle

Stellt eine Methode zum Aufrufen von [**isearchitem**](-search-isearchitem.md) -Objekten bereit. Methoden in dieser Schnittstelle werden vom Protokoll Host aufgerufen, wenn URLs aus dem Gatherer verarbeitet werden. Der Protokollhandler implementiert das Protokoll für den Zugriff auf eine Inhaltsquelle im systemeigenen Format, und diese Schnittstelle implementiert einen benutzerdefinierten Protokollhandler, um die Datenquellen zu erweitern, die indiziert werden können.

## <a name="members"></a>Member

Die **isearchprotocolui** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Isearchprotocolui** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **isearchprotocolui** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                       | BESCHREIBUNG                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getsearchitemforurl**](-search-isearchprotocolui-getsearchitemforurl.md) | Ruft das Suchelement für die angegebenen Daten ab. Diese Methode wird einmal für jede URL aufgerufen, die vom Gatherer verarbeitet wird, und Ruft einen Zeiger auf das [**isearchitem**](-search-isearchitem.md) -Objekt ab. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Die **isearchprotocolui** -Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler von Drittanbietern auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, kann es erforderlich sein, die **isearchprotocolui** -Schnittstelle und die folgenden APIs zu verwenden: die Schnittstellen [**iitempreviewerext**](-search-iitempreviewerext.md), [**iitempropertybag**](iitempropertybag.md) und [**isearchitem**](-search-isearchitem.md) , die [**linkinfo**](-search-linkinfo.md) -Struktur und die [**linktype**](-search-linktype.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 3,0<br/>          |



 

 
