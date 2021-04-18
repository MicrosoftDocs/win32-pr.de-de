---
description: Konfiguriert die Netzwerkadapter innerhalb des Gast Betriebssystems.
ms.assetid: 698e0c17-f8bd-433f-b982-5481f9701ba6
title: Setguestnetworkadapterconfiguration-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.SetGuestNetworkAdapterConfiguration
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 02c79df7aa08faa842e2b702b4cf18944e96bdfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529042"
---
# <a name="setguestnetworkadapterconfiguration-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Setguestnetworkadapterconfiguration-Methode der MSVM \_ virtualsystemmanagementservice-Klasse

Konfiguriert die Netzwerkadapter innerhalb des Gast Betriebssystems. Diese Konfigurationsparameter werden unmittelbar nach dem Einrichten der Kommunikation mit der in dem Gast Betriebssystem ausgelaufenden KVP Exchange-Integrations Komponente angewendet.

## <a name="syntax"></a>Syntax


```mof
uint32 SetGuestNetworkAdapterConfiguration(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 NetworkConfiguration[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Computersystem* \[ in\]
</dt> <dd>

Ein Verweis auf die [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, deren Netzwerkadapter konfiguriert werden sollen.

</dd> <dt>

*Network Configuration* \[ in\]
</dt> <dd>

Ein Array von eingebetteten Instanzen der [**MSVM \_ guestnetworkadapterconfiguration**](msvm-guestnetworkadapterconfiguration.md) -Klasse. Jede Instanz beschreibt die Konfigurationsparameter für einen der Netzwerkadapter innerhalb des virtuellen Computers. Die **dhcpabled** -Eigenschaft muss für jede Instanz angegeben werden.

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

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Status für diesen Vorgang** (32775).
</dt> <dt>

**Falscher Datentyp** (32776).
</dt> <dt>

Das **System ist nicht verfügbar** (32777).
</dt> <dt>

**Nicht** genügend Arbeitsspeicher (32778)
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

[**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

