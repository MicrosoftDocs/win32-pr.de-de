---
title: Body (sendemailtype)-Element
description: Enthält den Text im Textkörper der e-Mail-Nachricht.
ms.assetid: fac6ddd5-6f73-427b-b213-ab946512c87a
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
ms.openlocfilehash: 4659f2ff03f69b6bba40d9cd16e9b68515cc8889
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339341"
---
# <a name="body-sendemailtype-element"></a>Body (sendemailtype)-Element

Enthält den Text im Textkörper der e-Mail-Nachricht.

``` syntax
<xs:element name="Body"
    type="string"
 />
```

Das **Body** -Element wird durch den komplexen [**sendemailtype**](taskschedulerschema-sendemailtype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                              | Abgeleitet von                                                           | BESCHREIBUNG                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (Aktionsgruppe)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendemailtype**](taskschedulerschema-sendemailtype-complextype.md) | Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.<br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**Text-Eigenschaft von iemailaction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body).

Informationen zur Skript Entwicklung finden Sie unter [**emailaction. Body**](emailaction-body.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





