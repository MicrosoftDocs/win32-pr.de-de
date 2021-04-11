---
title: Title (showmessagetype)-Element
description: Enthält den Titel des Meldungs Felds.
ms.assetid: 089d2043-41ed-4050-b794-af24ab7ac8b9
keywords:
- Title-Element Taskplaner
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca5baa7135579ff673ba9b01a672a126924d1d49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103110"
---
# <a name="title-showmessagetype-element"></a>Title (showmessagetype)-Element

Enthält den Titel des Meldungs Felds.

``` syntax
<xs:element name="Title"
    type="nonEmptyString"
 />
```

Das **Title** -Element wird durch den komplexen Typ " [**showmessagetype**](taskschedulerschema-showmessagetype-complextype.md) " definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                  | Abgeleitet von                                                               | BESCHREIBUNG                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [**ShowMessage (Aktionsgruppe)**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showmessagetype**](taskschedulerschema-showmessagetype-complextype.md) | Stellt eine Aktion dar, die ein Meldungs Feld anzeigt.<br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**Title-Eigenschaft von ishowmessageaction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title).

Informationen zur Skript Entwicklung finden Sie unter [**showmessageaction. Title**](showmessageaction-title.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





