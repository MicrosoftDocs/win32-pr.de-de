---
description: Definiert Methoden zum Abrufen von Informationen zu den Eigenschaften eines Suchelements. Diese Schnittstelle wird nur auf Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.
ms.assetid: 0fef34c5-f20f-475a-9223-5cb73079c842
title: IItemPropertyBag-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2657fea53c4e7021e17df4b74cc210bd8547180566ff579524f85b7663a0c247
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226561"
---
# <a name="iitempropertybag-interface"></a>IItemPropertyBag-Schnittstelle

Definiert Methoden zum Abrufen von Informationen zu den Eigenschaften eines Suchelements. Diese Schnittstelle wird nur auf Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

## <a name="members"></a>Member

Die **IItemPropertyBag-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IItemPropertyBag** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IItemPropertyBag-Schnittstelle** verfügt über diese Methoden.



| Methode                                                      | BESCHREIBUNG                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**CountProperties**](/previous-versions/windows/desktop/legacy/ff684387(v=vs.85)) | Ruft die Anzahl der Eigenschaften im Eigenschaften bag ab.<br/>                     |
| [**GetPropertyInfo**](iitempropertybag-getpropertyinfo.md) | Ruft die Informationen ab, die zum Lesen oder Speichern der Eigenschaften in der Eigenschaftentüte erforderlich sind.<br/> |
| [**Überwachungsdaten**](iitempropertybag-read.md)                       | Bewirkt, dass eine oder mehrere Eigenschaften aus dem Eigenschaften bag gelesen werden.<br/>                   |
| [**Schreiben**](iitempropertybag-write.md)                     | Bewirkt, dass eine oder mehrere Eigenschaften in der Eigenschaftentüte gespeichert werden.<br/>                  |



 

## <a name="remarks"></a>Hinweise

Die **IItemPropertyBag-Schnittstelle** wird nur auf Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

Um eine Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern anzuzeigen, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die **IItemPropertyBag-Schnittstelle** und die folgenden APIs zu verwenden: die [**ISearchProtocolUI-,**](-search-isearchprotocolui.md) [**IItemPreviewerExt-**](-search-iitempreviewerext.md) und [**ISearchItem-Schnittstelle,**](-search-isearchitem.md) die [**LINKINFO-**](-search-linkinfo.md) und [**ITEMPROP-Strukturen**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) und die [**LINKTYPE-Enumeration.**](-search-linktype.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 3.0<br/>          |



 

 
