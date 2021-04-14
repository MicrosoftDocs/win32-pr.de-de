---
title: Source-Element (registrationinfotype)
description: Gibt an, woher die Aufgabe stammt. Beispielsweise aus einer Komponente, einem Dienst, einer Anwendung oder einem Benutzer.
ms.assetid: 174e2aac-7cd0-4c19-9441-2c93a3260c6f
keywords:
- Quell Element Taskplaner
topic_type:
- apiref
api_name:
- Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 65437fa0e06c303c7c2c29151f33f74f1678296d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391630"
---
# <a name="source-registrationinfotype-element"></a>Source-Element (registrationinfotype)

Gibt an, woher die Aufgabe stammt. Beispielsweise aus einer Komponente, einem Dienst, einer Anwendung oder einem Benutzer.

``` syntax
<xs:element name="Source"
    type="string"
    minOccurs="0"
 />
```

Das **Source** -Element wird durch den komplexen Typ [**registrationinfotype**](taskschedulerschema-registrationinfotype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                           | Abgeleitet von                                                                         | BESCHREIBUNG                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationinfotype**](taskschedulerschema-registrationinfotype-complextype.md) | Gibt administrative Informationen zum Task an, z. b. den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert ist.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Skripterstellung wird die Quelle einer Aufgabe mithilfe der [**RegistrationInfo. Source**](registrationinfo-source.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung wird die Quelle einer Aufgabe mithilfe der [**iregistrationinfo:: Source**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_source) -Eigenschaft angegeben.

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

 

 





