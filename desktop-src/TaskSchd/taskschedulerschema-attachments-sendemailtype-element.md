---
title: Anhänge (sendemailtype)-Element
description: Enthält eine Liste der Anlagen in der e-Mail-Nachricht.
ms.assetid: 5ae22481-af70-42eb-a964-e63d800be17d
keywords:
- Anhänge-Element Taskplaner
topic_type:
- apiref
api_name:
- Attachments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 67eed8f82f0caa27f44070bd109d4fa4560472eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742769"
---
# <a name="attachments-sendemailtype-element"></a>Anhänge (sendemailtype)-Element

Enthält eine Liste der Anlagen in der e-Mail-Nachricht.

``` syntax
<xs:element name="Attachments"
    type="attachmentsType"
 />
```

Das **Anhänge** -Element wird durch den komplexen [**sendemailtype**](taskschedulerschema-sendemailtype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                              | Abgeleitet von                                                           | BESCHREIBUNG                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (Aktionsgruppe)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendemailtype**](taskschedulerschema-sendemailtype-complextype.md) | Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                          | type                                                                    | BESCHREIBUNG                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**Datei**](taskschedulerschema-file-attachmentstype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Gibt den Pfad zu einer Datei an, die als Anlage in einer e-Mail-Nachricht gesendet wird.<br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**der Eigenschaft "Anhänge" von iemailaction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).

Informationen zur Skript Entwicklung finden Sie unter [**emailaction. Anhänge**](emailaction-attachments.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





