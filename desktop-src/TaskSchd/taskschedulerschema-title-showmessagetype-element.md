---
title: Title (showMessageType)-Element
description: Enthält den Titel des Meldungsfelds.
ms.assetid: 089d2043-41ed-4050-b794-af24ab7ac8b9
keywords:
- Titelelement Taskplaner
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e5fe72b791a963e78d49ace14f7edec1210dc3bf23a5f7cee9550e6f6db53e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355677"
---
# <a name="title-showmessagetype-element"></a>Title (showMessageType)-Element

Enthält den Titel des Meldungsfelds.

``` syntax
<xs:element name="Title"
    type="nonEmptyString"
 />
```

Das **Title-Element** wird durch den komplexen [**ShowMessageType-Typ**](taskschedulerschema-showmessagetype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                  | Abgeleitet von                                                               | BESCHREIBUNG                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [**ShowMessage (actionGroup)**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | Stellt eine Aktion dar, die ein Meldungsfeld zeigt.<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie [**unter Title-Eigenschaft von IShowMessageAction.**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title)

Informationen zur Skriptentwicklung finden Sie unter [**ShowMessageAction.Title**](showmessageaction-title.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





