---
description: 'StartService-Methode der Msvm_SecurityService-Klasse: Startet den Dienst.'
ms.assetid: 59918c15-7216-4cf7-9215-b27532febc72
title: StartService-Methode der Msvm_SecurityService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31e16eea84cf61ace11c241b6409a5810f74b8f1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111398"
---
# <a name="startservice-method-of-the-msvm_securityservice-class"></a>StartService-Methode der Msvm \_ SecurityService-Klasse

Startet den Dienst.

## <a name="syntax"></a>Syntax


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 zurück. andernfalls wird ein Fehler zurückgegeben.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1703 \[\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ SecurityService**](msvm-securityservice.md)
</dt> </dl>

 

 




