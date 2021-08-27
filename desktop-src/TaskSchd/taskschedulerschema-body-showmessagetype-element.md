---
title: Body (showMessageType)-Element
description: Enthält den Text, der im Text des Meldungsfelds angezeigt werden soll.
ms.assetid: 69ea872a-7ca1-4464-9380-b35f74c9cb8e
keywords:
- Body-Element Taskplaner
topic_type:
- apiref
api_name:
- Body
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c6b1fbacd450c05b8ff71521dacfa6e95c7efc70fc7d8909ca66f3390bf22295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010870"
---
# <a name="body-showmessagetype-element"></a>Body (showMessageType)-Element

Enthält den Text, der im Text des Meldungsfelds angezeigt werden soll.

``` syntax
<xs:element name="Body"
    type="nonEmptyString"
 />
```

Das **Body-Element** wird durch den komplexen [**showMessageType-Typ**](taskschedulerschema-showmessagetype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                  | Abgeleitet von                                                               | Beschreibung                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [**ShowMessage (actionGroup)**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | Stellt eine Aktion dar, die ein Meldungsfeld anzeigt.<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**MessageBody-Eigenschaft von IShowMessageAction.**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody)

Informationen zur Skriptentwicklung finden Sie unter [**ShowMessageAction.MessageBody**](showmessageaction-messagebody.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





