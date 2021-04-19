---
description: Ändert die Replikationseinstellungen für einen virtuellen Computer. Wenn ein Client diese Methode für einen virtuellen Replikat Computer aufruft, ändert er die Replikationseinstellungen der Replikations Beziehung mit dem erweiterten Replikat.
ms.assetid: e68514a5-f508-4047-8dcc-6a95f3e3353e
title: Modifyreplicationsettings-Methode der Msvm_ReplicationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyReplicationSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d1c932f06350324e0d84559724f7ba0412dfb3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353829"
---
# <a name="modifyreplicationsettings-method-of-the-msvm_replicationservice-class"></a>Modifyreplicationsettings-Methode der MSVM- \_ replicationservice-Klasse

Ändert die Replikationseinstellungen für einen virtuellen Computer. Wenn ein Client diese Methode für einen virtuellen Replikat Computer aufruft, ändert er die Replikationseinstellungen der Replikations Beziehung mit dem erweiterten Replikat.

## <a name="syntax"></a>Syntax


```mof
uint32 ModifyReplicationSettings(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ReplicationSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Computersystem* \[ in\]
</dt> <dd>

Ein Verweis auf eine [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Instanz, die den virtuellen Computer darstellt, für den die Replikationseinstellungen geändert werden sollen.

</dd> <dt>

*Replicationsettingdata* \[ in\]
</dt> <dd>

Eine Zeichen folgen Darstellung der [**MSVM \_ replicationsettingdata**](msvm-replicationsettingdata.md) -Klasse, die die neuen Replikationseinstellungen definiert.

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
</dt> <dt>

Die **Datei wurde nicht gefunden** (32779).
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

**Modifyreplicationsettings** übernimmt eine [**MSVM- \_ replicationsettingdata**](msvm-replicationsettingdata.md) -Instanz (frsd) als Eingabe. Die zugehörige frsd-Datei für die virtuelle Maschine als Host-zu-Host-Anbieter ist die Standardauswahl. Die Eingabe-frsd wird auf gültige Einstellungen für jede Eigenschaft für den Standardanbieter überprüft. In dieser Tabelle werden die Validierungs Unterschiede in Bezug auf den externen Anbieter zusammengefasst.



| Eigenschaft                                             | Externe Anbieter                                 |
|------------------------------------------------------|----------------------------------------------------|
| Replicationprovider                                  | Identisch mit Standardanbieter                           |
| AuthenticationType                                   | Wird ignoriert.                                            |
| CertificateThumbPrint                                | Wird ignoriert.                                            |
| Rootcertifi-ethumschlag-Print (RO)                       | Wird ignoriert.                                            |
| Compressionaktiviert                                   | Identisch mit Standardanbieter                           |
| Bypassproxyserver                                    | Identisch mit Standardanbieter                           |
| Wiederherstellungsconnectionpoint                              | Ignoriert \* (kann sich ändern, wenn der Anbieter eine Anforderung hat) |
| Wiederherstellunghostsystem (RO)                              | Wird ignoriert.                                            |
| Primaryconnectionpoint (RO)                          | Identisch mit Standardanbieter                           |
| Primaryhostsystem (RO)                               | Identisch mit Standardanbieter                           |
| Wiederherstellserverportnummer                             | Ignoriert \* (kann sich ändern, wenn der Anbieter eine Anforderung hat) |
| Replicatehostkvpitems                                | Wird ignoriert.                                            |
| Applicationkonsistentsnapshotinterval                | Identisch mit Standardanbieter                           |
| Parameter recoveryhistory einen                                      | Identisch mit Standardanbieter                           |
| Includdisks\[\]                                    | Identisch mit Standardanbieter                           |
| Autoresynchronizeaktivierte                             | Identisch mit Standardanbieter                           |
| Autoresynchronizeingetervalstart                       | Identisch mit Standardanbieter                           |
| Autoresynchronizzutervalend                         | Identisch mit Standardanbieter                           |
| Enableschreiteorderkonservierungs ationacrossdisks (veraltet) | Identisch mit Standardanbieter                           |
| ReplicationInterval                                  | Identisch mit Standardanbieter                           |



 

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

[**MSVM \_ replicationservice**](msvm-replicationservice.md)
</dt> </dl>

 

