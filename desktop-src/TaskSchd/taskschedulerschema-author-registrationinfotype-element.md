---
title: Author (registrationinfotype)-Element
description: Gibt den Autor der Aufgabe an.
ms.assetid: 1faa4952-0737-4313-afa5-4a9bad5daaff
keywords:
- Author-Element Taskplaner
topic_type:
- apiref
api_name:
- Author
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d368093a266827004cddf23dc7ba5d82f108f99f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956686"
---
# <a name="author-registrationinfotype-element"></a>Author (registrationinfotype)-Element

Gibt den Autor der Aufgabe an.

``` syntax
<xs:element name="Author"
    type="string"
    minOccurs="0"
 />
```

Das **Author** -Element wird durch den komplexen Typ [**registrationinfotype**](taskschedulerschema-registrationinfotype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                           | Abgeleitet von                                                                         | BESCHREIBUNG                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationinfotype**](taskschedulerschema-registrationinfotype-complextype.md) | Gibt administrative Informationen zum Task an, z. b. den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert ist.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Skripterstellung wird der Autor der Aufgabe mithilfe der [**RegistrationInfo. Author**](registrationinfo-author.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung wird der Autor der Aufgabe mithilfe der [**iregistrationinfo:: Author**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_author) -Eigenschaft angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert den Autor einer Aufgabe.


```XML
<RegistrationInfo>
    <Author></Author>
 </RegistrationInfo>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





