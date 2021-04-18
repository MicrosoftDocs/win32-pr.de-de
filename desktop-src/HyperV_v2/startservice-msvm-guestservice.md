---
description: Versetzt den Gast Dienst in den Zustand "gestartet".
ms.assetid: 1DC6A5B3-0F91-4AC1-99D5-0E8CF5ED35A2
title: 'Msvm_GuestService:: StartService-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1a87bc9933bd7b3a54bd59169b0099e34eb04c52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355080"
---
# <a name="msvm_guestservicestartservice-method"></a>MSVM \_ guestservice:: StartService-Methode

Versetzt den Gast Dienst in den Zustand "gestartet".

## <a name="syntax"></a>Syntax


```C++
uint32 StartService();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.



| Rückgabecode/-wert                                                                                                                                             | BESCHREIBUNG         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt> </dl> | Erfolg.<br/> |
| <dl> <dt>**Nicht unterstützt**</dt> <dt>1</dt> </dl>           |                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\\\\\Stammvirtualisierung \\ v2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM- \_ guestservice**](msvm-guestservice.md)
</dt> </dl>

 

 




