---
title: BCC (sendemailtype)-Element
description: Enthält die in der Bcc-Zeile einer e-Mail-Nachricht verwendeten e-Mail-Adressen.
ms.assetid: c80407d0-3b3f-4efe-91de-7a3a7abc996f
keywords:
- BCC-Element Taskplaner
topic_type:
- apiref
api_name:
- Bcc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f262b8f5d74018a4622f915def85df5e16108cdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104349"
---
# <a name="bcc-sendemailtype-element"></a>BCC (sendemailtype)-Element

Enthält die in der Bcc-Zeile einer e-Mail-Nachricht verwendeten e-Mail-Adressen.

``` syntax
<xs:element name="Bcc"
    type="string"
 />
```

Das **Bcc** -Element wird durch den komplexen [**sendemailtype**](taskschedulerschema-sendemailtype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                              | Abgeleitet von                                                           | BESCHREIBUNG                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (Aktionsgruppe)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendemailtype**](taskschedulerschema-sendemailtype-complextype.md) | Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.<br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**Bcc-Eigenschaft von iemailaction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc).

Informationen zur Skript Entwicklung finden Sie unter [**emailaction. BCC**](emailaction-bcc.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





