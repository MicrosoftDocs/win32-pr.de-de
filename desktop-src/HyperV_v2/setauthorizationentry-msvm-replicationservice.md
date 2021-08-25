---
description: Legt den Replikationsautorisierungseintrag für einen virtuellen Computer fest.
ms.assetid: 39b6b0c4-5515-4863-9038-4c37421abe65
title: SetAuthorizationEntry-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.SetAuthorizationEntry
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7ce51997399a7ea028f39156e31a67144f415f37d4d028694d674f8aff8fe522
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913930"
---
# <a name="setauthorizationentry-method-of-the-msvm_replicationservice-class"></a>SetAuthorizationEntry-Methode der Msvm \_ ReplicationService-Klasse

Legt den Replikationsautorisierungseintrag für einen virtuellen Computer fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetAuthorizationEntry(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 AuthorizationEntry,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ComputerSystem* \[ In\]
</dt> <dd>

Ein Verweis auf eine [**CIM \_ ComputerSystem-Instanz,**](/windows/desktop/CIMWin32Prov/cim-computersystem) die den virtuellen Computer darstellt, für den der Autorisierungseintrag festgelegt werden soll.

</dd> <dt>

*AuthorizationEntry* \[ In\]
</dt> <dd>

Eine Zeichenfolgendarstellung einer Instanz der [**Msvm \_ ReplicationAuthorizationSettingData-Klasse,**](msvm-replicationauthorizationsettingdata.md) die den Autorisierungseintrag definiert, der für den virtuellen Computer verwendet werden soll.

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

**Überprüfte Methodenparameter – Auftragsstart** (4096)
</dt> <dt>

**Fehler** (32768)
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

**Status ist unbekannt** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Zustand für diesen Vorgang** (32775)
</dt> <dt>

**Falscher Datentyp** (32776)
</dt> <dt>

**System ist nicht verfügbar** (32777)
</dt> <dt>

**Nicht genügend Arbeitsspeicher** (32778)
</dt> <dt>

**Datei nicht gefunden** (32779)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AddAuthorizationEntry**](addauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[**ModifyAuthorizationEntry**](modifyauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[**RemoveAuthorizationEntry**](removeauthorizationentry-msvm-replicationservice.md)
</dt> <dt>

[**Msvm \_ ReplicationService**](msvm-replicationservice.md)
</dt> </dl>

 

