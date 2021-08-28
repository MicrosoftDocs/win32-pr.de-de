---
title: File (attachmentsType)-Element
description: Enthält den Pfad zu einer Datei, die als Anlage in einer E-Mail gesendet wird.
ms.assetid: a53f591b-ac59-43b4-8cc2-661e76d307cc
keywords:
- File-Element Taskplaner
topic_type:
- apiref
api_name:
- File
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 793b23bc6b9d75ac809c42063fa9c300542705b718cd22253f6f2d3a1a76caa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125850"
---
# <a name="file-attachmentstype-element"></a>File (attachmentsType)-Element

Enthält den Pfad zu einer Datei, die als Anlage in einer E-Mail gesendet wird.

``` syntax
<xs:element name="File"
    type="nonEmptyString"
 />
```

Das **File-Element** wird durch den [**komplexen attachmentsType-Typ**](taskschedulerschema-attachmentstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                      | Abgeleitet von                                                               | Beschreibung                                                     |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**Anlagen (sendEmailType)**](taskschedulerschema-attachments-sendemailtype-element.md) | [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md) | Enthält eine Liste der Anlagen in der E-Mail-Nachricht.<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**Attachments-Eigenschaft von IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).

Informationen zur Skriptentwicklung finden Sie unter [**EmailAction.Attachments.**](emailaction-attachments.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





