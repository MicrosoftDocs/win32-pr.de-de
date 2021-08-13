---
description: Ruft die aktuelle DACL (Discretionary Access Control List) ab, die den Zugriff auf die interaktive Sitzung eines virtuellen Computers steuert.
ms.assetid: 9b81f6d5-20fa-4277-b943-756d85359fd2
title: GetInteractiveSessionACL-Methode der Msvm_TerminalService-Klasse
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
ms.openlocfilehash: 37f33ce16d0b5eb2b998f4f08a37a6e601f82d3aecf49a2e8e68b2a7f571a01e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253720"
---
# <a name="getinteractivesessionacl-method-of-the-msvm_terminalservice-class"></a>GetInteractiveSessionACL-Methode der Msvm \_ TerminalService-Klasse

Ruft die aktuelle *DACL (Discretionary Access Control List)* ab, die den Zugriff auf die interaktive Sitzung eines virtuellen Computers steuert.

## <a name="syntax"></a>Syntax


```mof
uint32 GetInteractiveSessionACL(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 AccessControlList[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ComputerSystem* \[ In\]
</dt> <dd>

Ein Verweis auf eine Instanz der [**Msvm \_ ComputerSystem-Klasse, die**](msvm-computersystem.md) den virtuellen Computer darstellt, dessen DACL abgerufen wird.

</dd> <dt>

*AccessControlList* \[ out\]
</dt> <dd>

Ein Array von Zeichenfolgen, die jeweils eine eingebettete Instanz der [**Msvm \_ InteractiveSessionACE-Klasse**](msvm-interactivesessionace.md) enthalten, die einen *Zugriffssteuerungseintrag (ACE)* in der interaktiven Sitzungs-DACL des virtuellen Computers darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Fehler** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Ungültiger Parameter** (4)
</dt> <dt>

**Ungültiger Zustand** (5)
</dt> <dt>

**Inkompatible Parameter** (6)
</dt> <dt>

**DMTF Reserved** (..)
</dt> <dt>

**Überprüfte Methodenparameter – Auftragsstart** (4096)
</dt> <dt>

**Reservierte Methode** (4097..32767)
</dt> <dt>

**Herstellerspezifisch** (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ TerminalService**](msvm-terminalservice.md)
</dt> </dl>

 

 




