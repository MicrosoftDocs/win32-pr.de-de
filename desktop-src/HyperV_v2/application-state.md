---
description: Gibt den Integritätsstatus einer Anwendung an.
ms.assetid: CA06AA34-A549-4CFC-9B52-D2E0B200C3E9
title: APPLICATION_STATE Enumeration
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
ms.openlocfilehash: 5f873e7a30a4cff6dc4cc89eaea225201a367f7c24ead11ad95da04c2ff1ab32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914160"
---
# <a name="application_state-enumeration"></a>APPLICATION \_ STATE-Enumeration

Gibt den Integritätsstatus einer Anwendung an.

## <a name="syntax"></a>Syntax


```C++
typedef enum _APPLICATION_STATE { 
  ApplicationStateHealthy   = 0,
  ApplicationStateCritical
} APPLICATION_STATE, *PAPPLICATION_STATE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="ApplicationStateHealthy"></span><span id="applicationstatehealthy"></span><span id="APPLICATIONSTATEHEALTHY"></span>**ApplicationStateHealthy**
</dt> <dd>

Der Anwendungsstatus ist fehlerfrei.

</dd> <dt>

<span id="ApplicationStateCritical"></span><span id="applicationstatecritical"></span><span id="APPLICATIONSTATECRITICAL"></span>**ApplicationStateCritical**
</dt> <dd>

Der Anwendungsstatus ist kritisch.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Um dieses Programmierelement verwenden zu können, Windows 8 Integrationskomponenten auf dem virtuellen Computer installiert sein, auf dem die Anwendung ausgeführt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                      |
| Version<br/>                  | Integrationskomponenten für Windows 8<br/>                                                           |
| Idl<br/>                      | <dl> <dt>VmApplicationHealthMonitor.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SetApplicationState**](ivmapplicationhealthmonitor-setapplicationstate.md)
</dt> </dl>

 

 




