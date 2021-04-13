---
title: File (attachmentstype)-Element
description: Enthält den Pfad zu einer Datei, die in einer e-Mail-Nachricht als Anlage gesendet wurde.
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
ms.openlocfilehash: ed07d4b31f9054f6caefcff0585d9683faa90c7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391764"
---
# <a name="file-attachmentstype-element"></a>File (attachmentstype)-Element

Enthält den Pfad zu einer Datei, die in einer e-Mail-Nachricht als Anlage gesendet wurde.

``` syntax
<xs:element name="File"
    type="nonEmptyString"
 />
```

Das **File** -Element wird durch den komplexen [**attachmentstype**](taskschedulerschema-attachmentstype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                      | Abgeleitet von                                                               | BESCHREIBUNG                                                     |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**Anlagen (sendemailtype)**](taskschedulerschema-attachments-sendemailtype-element.md) | [**attachmentstype**](taskschedulerschema-attachmentstype-complextype.md) | Enthält eine Liste der Anlagen in der e-Mail-Nachricht.<br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**der Eigenschaft "Anhänge" von iemailaction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).

Informationen zur Skript Entwicklung finden Sie unter [**emailaction. Anhänge**](emailaction-attachments.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





