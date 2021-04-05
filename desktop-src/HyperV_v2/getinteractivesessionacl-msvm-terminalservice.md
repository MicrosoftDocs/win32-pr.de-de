---
description: Ruft die aktuelle DACL (diskreter Zugriffs Steuerungs Liste) ab, mit der der Zugriff auf die interaktive Sitzung eines virtuellen Computers gesteuert wird.
ms.assetid: 9b81f6d5-20fa-4277-b943-756d85359fd2
title: Getinteractivesessionacl-Methode der Msvm_TerminalService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.GetInteractiveSessionACL
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f08c8514a2f65a08b4b9350b38988da8e49b4985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752233"
---
# <a name="getinteractivesessionacl-method-of-the-msvm_terminalservice-class"></a>Getinteractivesessionacl-Methode der MSVM \_ Terminalservice-Klasse

Ruft die aktuelle DACL ( *diskreter Zugriffs Steuerungs Liste* ) ab, mit der der Zugriff auf die interaktive Sitzung eines virtuellen Computers gesteuert wird.

## <a name="syntax"></a>Syntax


```mof
uint32 GetInteractiveSessionACL(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 AccessControlList[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Computersystem* \[ in\]
</dt> <dd>

Ein Verweis auf eine Instanz der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse, die den virtuellen Computer darstellt, dessen DACL abgerufen wird.

</dd> <dt>

*AccessControlList* \[ vorgenommen\]
</dt> <dd>

Ein Array von Zeichen folgen, die jeweils eine eingebettete Instanz der [**MSVM \_ interactivesessionace**](msvm-interactivesessionace.md) -Klasse enthalten, die einen *Zugriffs Steuerungs Eintrag* (ACE) in der interaktiven Sitzungs-DACL der virtuellen Maschine darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

Fehler **(2** )
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Ungültiger Parameter** (4)
</dt> <dt>

**Ungültiger Status** (5)
</dt> <dt>

Nicht **kompatible Parameter** (6)
</dt> <dt>

**DMTF reserviert** (..)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

**Reservierte Methode** (4097.32767)
</dt> <dt>

**Hersteller spezifisch** (32768.65535)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ Terminalservice**](msvm-terminalservice.md)
</dt> </dl>

 

 




