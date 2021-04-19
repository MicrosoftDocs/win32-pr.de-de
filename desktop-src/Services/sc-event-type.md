---
description: Gibt einen Typ von Dienststatus Änderungen für die Überwachung und Berichterstellung an.
ms.assetid: 7508526c-02ce-4ac2-8616-491390a4afad
title: SC_EVENT_TYPE-Enumeration (winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SC_EVENT_TYPE
api_type:
- HeaderDef
api_location:
- Winsvcp.h
ms.openlocfilehash: 55853d13844d3bb255ab0e84a50e8cbbea2d76ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360834"
---
# <a name="sc_event_type-enumeration"></a>SC \_ - \_ Ereignistyp-Enumeration

Gibt einen Typ von Dienststatus Änderungen für die Überwachung und Berichterstellung an.

## <a name="syntax"></a>Syntax


```C++
typedef enum _SC_EVENT_TYPE { 
  SC_EVENT_DATABASE_CHANGE  = 0,
  SC_EVENT_PROPERTY_CHANGE  = 1,
  SC_EVENT_STATUS_CHANGE    = 2
} SC_EVENT_TYPE, *PSC_EVENT_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span>**Änderung der SC- \_ Ereignis \_ Datenbank \_**
</dt> <dd>

Es wurde ein Dienst hinzugefügt oder gelöscht. Der *hservice* -Parameter der Funktion " [**abonnebeservicechangenotifications**](subscribeservicechangenotifications.md) " muss ein Handle für den SCM sein.

</dd> <dt>

<span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span>**SC- \_ Ereignis \_ Eigenschafts \_ Änderung**
</dt> <dd>

Mindestens eine der Dienst Eigenschaften wurde aktualisiert. Der *hservice* -Parameter der Funktion " [**abonnebeservicechangenotifications**](subscribeservicechangenotifications.md) " muss ein Handle für den Dienst sein.

</dd> <dt>

<span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span>**SC- \_ Ereignis \_ Status \_ Änderung**
</dt> <dd>

Der Status eines Dienstanbieter hat sich geändert. Der *hservice* -Parameter der Funktion " [**abonnebeservicechangenotifications**](subscribeservicechangenotifications.md) " muss ein Handle für den Dienst sein.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winsvcp. h</dt> </dl> |



 

 




