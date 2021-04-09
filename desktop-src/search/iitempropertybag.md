---
description: Definiert Methoden zum Abrufen von Informationen zu den Eigenschaften eines Such Elements. Diese Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.
ms.assetid: 0fef34c5-f20f-475a-9223-5cb73079c842
title: Iitempropertybag-Schnittstelle
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
ms.openlocfilehash: 4da3db21947de6d35ef5e848499efc7f22633f7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128504"
---
# <a name="iitempropertybag-interface"></a>Iitempropertybag-Schnittstelle

Definiert Methoden zum Abrufen von Informationen zu den Eigenschaften eines Such Elements. Diese Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

## <a name="members"></a>Member

Die **iitempropertybag** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iitempropertybag** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iitempropertybag** -Schnittstelle verfügt über diese Methoden.



| Methode                                                      | BESCHREIBUNG                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**CountProperties**](/previous-versions/windows/desktop/legacy/ff684387(v=vs.85)) | Ruft die Anzahl der Eigenschaften in der Eigenschaften Sammlung ab.<br/>                     |
| [**GetPropertyInfo**](iitempropertybag-getpropertyinfo.md) | Ruft die Informationen ab, die erforderlich sind, um die Eigenschaften in der Eigenschaften Sammlung zu lesen oder zu speichern.<br/> |
| [**Lesen**](iitempropertybag-read.md)                       | Bewirkt, dass eine oder mehrere Eigenschaften aus dem Eigenschaften Behälter gelesen werden.<br/>                   |
| [**Schreiben**](iitempropertybag-write.md)                     | Bewirkt, dass eine oder mehrere Eigenschaften im Eigenschaften Behälter gespeichert werden.<br/>                  |



 

## <a name="remarks"></a>Bemerkungen

Die **iitempropertybag** -Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die **iitempropertybag** -Schnittstelle und die folgenden APIs zu verwenden: die Schnittstellen [**isearchprotocolui**](-search-isearchprotocolui.md), [**iitempreviewerext**](-search-iitempreviewerext.md) und [**isearchitem**](-search-isearchitem.md) [**, die-und**](-search-linkinfo.md) [**linktype**](-search-linktype.md) [**-**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) Enumeration.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 3,0<br/>          |



 

 
