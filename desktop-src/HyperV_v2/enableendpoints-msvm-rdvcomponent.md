---
description: Fordert das virtuelle Remotedesktopdienste virtuellen Gerät auf, eine Pipe-Verbindung mit dem virtuellen Computer zu starten.
ms.assetid: e53238ee-8264-416b-8855-193c28089cfa
title: Enableendpoints-Methode der Msvm_RdvComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponent.EnableEndPoints
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a668e6a2605a52c7021f630145d6e4897e1c76ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214747"
---
# <a name="enableendpoints-method-of-the-msvm_rdvcomponent-class"></a>Enableendpoints-Methode der MSVM \_ rdvcomponent-Klasse

Fordert das virtuelle Remotedesktopdienste virtuellen Gerät auf, eine Pipe-Verbindung mit dem virtuellen Computer zu starten.

## <a name="syntax"></a>Syntax


```mof
uint32 EnableEndPoints();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

Fehler **(32768** )
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

Der **Status ist "Unknown** " (32771).
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

**Nicht** genügend Arbeitsspeicher (32774)
</dt> <dt>

Die **Datei wurde nicht gefunden** (32775).
</dt> <dt>

 (32776)
</dt> <dt>

 (32777)
</dt> <dt>

 (32778)
</dt> <dt>

 (32779)
</dt> <dt>

 (32780)
</dt> <dt>

 (32781)
</dt> <dt>

 (32782)
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

[**MSVM \_ rdvcomponent**](msvm-rdvcomponent.md)
</dt> </dl>

 

 




