---
description: Gibt eine Art von Dienststatusänderung für Überwachung und Berichterstellung an.
ms.assetid: 7508526c-02ce-4ac2-8616-491390a4afad
title: SC_EVENT_TYPE -Enumeration (Winsvcp.h)
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
ms.openlocfilehash: fa10f1e9a9691dde815fef7ce1d7822287dff970efd32499938f0f6bcf866593
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117967809"
---
# <a name="sc_event_type-enumeration"></a>SC \_ EVENT \_ TYPE-Enumeration

Gibt eine Art von Dienststatusänderung für Überwachung und Berichterstellung an.

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

<span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span>**SC \_ EVENT \_ DATABASE \_ CHANGE**
</dt> <dd>

Ein Dienst wurde hinzugefügt oder gelöscht. Der *hService-Parameter* der [**SubscribeServiceChangeNotifications-Funktion**](subscribeservicechangenotifications.md) muss ein Handle für den SCM sein.

</dd> <dt>

<span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span>**ÄNDERUNG \_ DER \_ SC-EREIGNISEIGENSCHAFT \_**
</dt> <dd>

Mindestens eine Diensteigenschaften wurde aktualisiert. Der *hService-Parameter* der [**SubscribeServiceChangeNotifications-Funktion**](subscribeservicechangenotifications.md) muss ein Handle für den Dienst sein.

</dd> <dt>

<span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span>**\_ \_ SC-EREIGNISSTATUSÄNDERUNG \_**
</dt> <dd>

Der Status eines Diensts hat sich geändert. Der *hService-Parameter* der [**SubscribeServiceChangeNotifications-Funktion**](subscribeservicechangenotifications.md) muss ein Handle für den Dienst sein.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winsvcp.h</dt> </dl> |



 

 




