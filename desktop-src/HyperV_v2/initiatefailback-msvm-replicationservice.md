---
description: Initiiert das Failback für einen virtuellen Wiederherstellungs Computer.
ms.assetid: F4AE1911-46B2-4412-A17F-3CA7D388276F
title: 'Msvm_ReplicationService:: initiatefailback-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.InitiateFailback
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b356982296427212287ea11b528a7878dc166245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348867"
---
# <a name="msvm_replicationserviceinitiatefailback-method"></a>MSVM \_ replicationservice:: initiatefailback-Methode

Initiiert das Failback für einen virtuellen Wiederherstellungs Computer.

## <a name="syntax"></a>Syntax


```C++
uint32 InitiateFailback(
  [in]  CIM_ComputerSystem ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [in]  string                 RecoveryPointIdentifier,
  [out] CIM_ConcreteJob    Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Computersystem* \[ in\]
</dt> <dd>

Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer darstellt, für den ein Failback initiiert werden soll.

</dd> <dt>

*Replicationsettingdata* \[ in\]
</dt> <dd>

Eine Zeichen folgen Darstellung einer eingebetteten Instanz der [**MSVM \_ replicationsettingdata**](msvm-replicationsettingdata.md) -Klasse, die die Replikationseinstellungen für das Failback definiert.

</dd> <dt>

*Wiederherstellungspointidentifier* \[ in\]
</dt> <dd>

Optionale Eingabe, die den Wiederherstellungspunkt identifiziert, an den das Failback angefordert wird.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird. Dieser Verweis kann verwendet werden, um den Fortschritt zu überwachen und das Ergebnis der Methode abzurufen.

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
</dt> <dt>

Die **Datei wurde nicht gefunden** (32779).
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

**Initiatefailback** funktioniert auf einem virtuellen Wiederherstellungs Computer und übernimmt die virtuelle Maschine in den Status " *waitingforfailback* ". **Initiatefailback** leitet die failbackanforderung an den entsprechenden Anbieter weiter, der den Wiederherstellungspunkt von der neuen primären Seite umkehren. Nachdem das Failback des angeforderten Wiederherstellungs Punkts abgeschlossen ist, wechselt der Replikations Status in den Zustand " *failbackabgeschlossene* ".

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

[**MSVM \_ replicationservice**](msvm-replicationservice.md)
</dt> </dl>

 

