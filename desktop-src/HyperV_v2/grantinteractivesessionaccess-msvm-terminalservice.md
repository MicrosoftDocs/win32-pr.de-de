---
description: Ermöglicht den Zugriff auf die interaktive Sitzung des virtuellen Computers auf die angegebene Liste von Treuhändern.
ms.assetid: 8a82170d-067b-47e5-a15f-21d6c04128d2
title: Grantinteractivesessionaccess-Methode der Msvm_TerminalService-Klasse
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
ms.openlocfilehash: b8bd49805b5fdc5545a81e4f0b816fe35a6c37b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356655"
---
# <a name="grantinteractivesessionaccess-method-of-the-msvm_terminalservice-class"></a>Grantinteractivesessionaccess-Methode der MSVM \_ Terminalservice-Klasse

Ermöglicht den Zugriff auf die interaktive Sitzung des virtuellen Computers auf die angegebene Liste von Treuhändern.

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

*Computersystem* \[ in\]
</dt> <dd>

Ein Verweis auf eine Instanz der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse, die den virtuellen Computer darstellt, dem der Zugriff gewährt wird.

</dd> <dt>

*Treuhänder* \[ in\]
</dt> <dd>

Ein Array von Zeichen folgen, das jeweils einen Vertrauens nehmer identifiziert, dem Zugriff auf die interaktive Sitzung des virtuellen Computers gewährt wird. Die Treuhänder-IDs müssen im Windows Sam-kompatiblen Format oder im Windows-SID-Zeichen folgen Format angegeben werden.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.

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

 

