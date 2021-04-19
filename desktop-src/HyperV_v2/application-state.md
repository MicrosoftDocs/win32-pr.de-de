---
description: Gibt den Integritäts Status einer Anwendung an.
ms.assetid: CA06AA34-A549-4CFC-9B52-D2E0B200C3E9
title: APPLICATION_STATE-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPLICATION_STATE
api_type:
- IDLDef
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 4b7e288f41c863dc3f0365db3c6aae867605e5c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348617"
---
# <a name="application_state-enumeration"></a>\_Enumeration des Anwendungs Zustands

Gibt den Integritäts Status einer Anwendung an.

## <a name="syntax"></a>Syntax


```C++
typedef enum _APPLICATION_STATE { 
  ApplicationStateHealthy   = 0,
  ApplicationStateCritical
} APPLICATION_STATE, *PAPPLICATION_STATE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="ApplicationStateHealthy"></span><span id="applicationstatehealthy"></span><span id="APPLICATIONSTATEHEALTHY"></span>**Applicationstatuehealthy**
</dt> <dd>

Der Anwendungs Status ist fehlerfrei.

</dd> <dt>

<span id="ApplicationStateCritical"></span><span id="applicationstatecritical"></span><span id="APPLICATIONSTATECRITICAL"></span>**Applicationstatuecritical**
</dt> <dd>

Der Anwendungs Status ist kritisch.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Um dieses Programmier Element zu verwenden, müssen die Windows 8-Integrations Komponenten auf dem virtuellen Computer installiert sein, auf dem die Anwendung ausgeführt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                      |
| Version<br/>                  | Integrations Komponenten für Windows 8<br/>                                                           |
| IDL<br/>                      | <dl> <dt>Vmapplicationhealthmonitor. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**"Standort Status"**](ivmapplicationhealthmonitor-setapplicationstate.md)
</dt> </dl>

 

 




