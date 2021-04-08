---
title: Description-Element (registrationinfotype)
description: Gibt die Beschreibung des Tasks an.
ms.assetid: bf3552eb-01a6-4651-ae43-4b4e8eef3faf
keywords:
- Description-Element Taskplaner
topic_type:
- apiref
api_name:
- Description
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80815a1502060af231cae1b93b964b80345891e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740824"
---
# <a name="description-registrationinfotype-element"></a>Description-Element (registrationinfotype)

Gibt die Beschreibung des Tasks an.

``` syntax
<xs:element name="Description"
    type="string"
    minOccurs="0"
 />
```

Das **Description** -Element wird durch den komplexen Typ [**registrationinfotype**](taskschedulerschema-registrationinfotype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                           | Abgeleitet von                                                                         | BESCHREIBUNG                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationinfotype**](taskschedulerschema-registrationinfotype-complextype.md) | Gibt administrative Informationen zum Task an, z. b. den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert ist.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Skripterstellung wird die Beschreibung einer Aufgabe mithilfe der [**RegistrationInfo. Description**](registrationinfo-description.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung wird die Beschreibung einer Aufgabe mithilfe der [**iregistrationinfo::D escription**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_description) -Eigenschaft angegeben.

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

 

 





