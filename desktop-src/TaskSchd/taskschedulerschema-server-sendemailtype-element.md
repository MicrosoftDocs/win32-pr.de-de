---
title: Server (sendemailtype)-Element
description: Enthält den e-Mail-Server zum Senden der e-Mail-Nachricht.
ms.assetid: 4c6084d1-70c5-4d8b-8fcb-ab4cd8aab441
keywords:
- Server-Element Taskplaner
topic_type:
- apiref
api_name:
- Server
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5fc57ddf5deee52ff9b118a8267eec4069108030
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391631"
---
# <a name="server-sendemailtype-element"></a>Server (sendemailtype)-Element

Enthält den e-Mail-Server zum Senden der e-Mail-Nachricht.

``` syntax
<xs:element name="Server"
    type="nonEmptyString"
 />
```

Das **Server** -Element wird durch den komplexen [**sendemailtype**](taskschedulerschema-sendemailtype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                              | Abgeleitet von                                                           | BESCHREIBUNG                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (Aktionsgruppe)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendemailtype**](taskschedulerschema-sendemailtype-complextype.md) | Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.<br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**Server-Eigenschaft von iemailaction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server).

Informationen zur Skript Entwicklung finden Sie unter [**emailaction. Server**](emailaction-server.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





