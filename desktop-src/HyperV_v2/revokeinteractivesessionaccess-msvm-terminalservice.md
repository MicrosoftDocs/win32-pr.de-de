---
description: Widerruft den Zugriff auf die interaktive Sitzung des virtuellen Computers aus der angegebenen Vertrauensnehmerliste.
ms.assetid: c6d3df04-c31e-404a-9a04-3e8653bdc14f
title: RevokeInteractiveSessionAccess-Methode der Msvm_TerminalService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.RevokeInteractiveSessionAccess
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 48fa52d97e58e421442c77f1503e72bb6a3d793e35a4d1dbd12624bffdbcd9d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746200"
---
# <a name="revokeinteractivesessionaccess-method-of-the-msvm_terminalservice-class"></a>RevokeInteractiveSessionAccess-Methode der Msvm \_ TerminalService-Klasse

Widerruft den Zugriff auf die interaktive Sitzung des virtuellen Computers aus der angegebenen Vertrauensnehmerliste.

## <a name="syntax"></a>Syntax


```mof
uint32 RevokeInteractiveSessionAccess(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 Trustees[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ComputerSystem* \[ In\]
</dt> <dd>

Ein Verweis auf eine Instanz der [**CIM \_ ComputerSystem-Klasse,**](cim-computersystem.md) die den virtuellen Computer darstellt, auf den der Zugriff aufgehoben wird.

</dd> <dt>

*Vertrauensnehmer* \[ In\]
</dt> <dd>

Ein Array von Zeichenfolgen, die jeweils einen Vertrauensnehmer identifizieren, dessen Zugriffsrechte widerrufen werden. Die Vertrauensnehmerbezeichner sollten in Windows SAM-kompatiblen Format oder Windows SID-Zeichenfolgenformat angegeben werden.

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

 

