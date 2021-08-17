---
description: Gewährt Zugriff auf die interaktive Sitzung des virtuellen Computers auf die angegebene Liste von Vertrauensnehmern.
ms.assetid: 8a82170d-067b-47e5-a15f-21d6c04128d2
title: GrantInteractiveSessionAccess-Methode der Msvm_TerminalService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.GrantInteractiveSessionAccess
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 39fd1e77eeea7429a2ef225226b964e44f1384295dc798c1b93611f282674fb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682330"
---
# <a name="grantinteractivesessionaccess-method-of-the-msvm_terminalservice-class"></a>GrantInteractiveSessionAccess-Methode der Msvm \_ TerminalService-Klasse

Gewährt Zugriff auf die interaktive Sitzung des virtuellen Computers auf die angegebene Liste von Vertrauensnehmern.

## <a name="syntax"></a>Syntax


```mof
uint32 GrantInteractiveSessionAccess(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 Trustees[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ComputerSystem* \[ In\]
</dt> <dd>

Ein Verweis auf eine Instanz der [**Msvm \_ ComputerSystem-Klasse, die**](msvm-computersystem.md) den virtuellen Computer darstellt, auf den Zugriff gewährt wird.

</dd> <dt>

*Vertrauensnehmer* \[ In\]
</dt> <dd>

Ein Array von Zeichenfolgen, die jeweils einen Vertrauensnehmer identifizieren, dem Zugriff auf die interaktive Sitzung des virtuellen Computers gewährt wird. Die Vertrauensnehmerbezeichner sollten in Windows SAM-kompatiblen Format oder Windows SID-Zeichenfolgenformat angegeben werden.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein objekt, das von [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))abgeleitet wurde.

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

 

