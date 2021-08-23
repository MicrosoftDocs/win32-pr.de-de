---
description: 'Weitere Informationen finden Sie unter: CheckVirtualSystemIsMigratableToSystem-Methode der CIM_VirtualSystemMigrationService-Klasse'
ms.assetid: d3f7c926-804f-4c7c-8964-a8e464155417
title: CheckVirtualSystemIsMigratableToSystem-Methode der CIM_VirtualSystemMigrationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4f2f543cff29464d76f1b2729efa9bca1a0c677d3cd7173975f59d2007aafb7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682711"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a>CheckVirtualSystemIsMigratableToSystem-Methode der CIM \_ VirtualSystemMigrationService-Klasse

Methode zum Durchführen einer Vorabüberprüfung, um zu bestimmen, ob ein virtuelles System wahrscheinlich erfolgreich zu einem Zielsystem migriert wird. Diese Methode garantiert aufgrund der dynamischen Ressourcenverfügbarkeit nicht, dass eine nachfolgende Migration immer erfolgreich ist. Rückgabecodebeschreibung:

## <a name="syntax"></a>Syntax


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] boolean                IsMigratable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ComputerSystem* \[ In\]
</dt> <dd>

[**CIM \_ ComputerSystem-Instanz,**](cim-computersystem.md) die auf das zu migrierende virtuelle Quellcomputersystem verweist.

</dd> <dt>

*DestinationSystem* \[ In\]
</dt> <dd>

[**CIM \_ Systeminstanz,**](cim-system.md) die auf das Zielsystem verweist, zu dem das virtuelle System migriert werden soll.

</dd> <dt>

*MigrationSettingData* \[ In\]
</dt> <dd>

Zeichenfolge, die eine eingebettete Instanz der [**CIM \_ VirtualSystemMigrationSettingData-Klasse**](cim-virtualsystemmigrationsettingdata.md) enthält, die migrationseinstellungen darstellt, die für den Migrationsvorgang gelten.

</dd> <dt>

*NewSystemSettingData* \[ In\]
</dt> <dd>

Zeichenfolge, die eine eingebettete Instanz der [**CIM \_ VirtualSystemSettingData-Klasse**](cim-virtualsystemsettingdata.md) enthält, die neue Eigenschaften darstellt, die nach der Migration auf das virtuelle System anwendbar sind.

</dd> <dt>

*NewResourceSettingData* \[ In\]
</dt> <dd>

Array von Zeichenfolgen, die jeweils eine eingebettete Instanz der [**CIM \_ ResourceAllocationSettingData-Klasse**](cim-resourceallocationsettingdata.md) enthalten, die neue Eigenschaften darstellen, die nach der Migration auf virtuelle Ressourcen im Bereich des virtuellen Systems anwendbar sind.

</dd> <dt>

*IsMigratable* \[ out\]
</dt> <dd>

Das Ergebnis der Migrationsprüfung gibt an, ob das virtuelle System erfolgreich migriert werden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 zurück. andernfalls wird ein Fehler zurückgegeben.



| Rückgabecode/-wert                                                                                                                                                | Beschreibung                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt> </dl>    | Durchgeführte Überprüfung; Ergebnis, das über den Wert des \[ \] *Out IsMigratable-Parameters* gemeldet wird.<br/>                                                                                                                                                                                                                                                                          |
| <dl> <dt>**Nicht unterstützt**</dt> <dt>1</dt> </dl>              | Die -Methode wird von der -Implementierung nicht unterstützt. Über den Wert des \[ \] *Out IsMigratable-Parameters wird* kein Ergebnis gemeldet.<br/>                                                                                                                                                                                                                                                |
| <dl> <dt>**Fehler**</dt> <dt>2</dt> </dl>                     | Fehler bei der Überprüfung aus unbekannten Gründen. Über den Wert des \[ \] *Out IsMigratable-Parameters wird* kein Ergebnis gemeldet.<br/>                                                                                                                                                                                                                                                  |
| <dl> <dt>**Timeout**</dt> <dt>3</dt> </dl>                    | Check timed out (Timed out überprüfen). Über den Wert des \[ \] *Out IsMigratable-Parameters wird* kein Ergebnis gemeldet.<br/>                                                                                                                                                                                                                                                                       |
| <dl> <dt>**Ungültiger Parameter**</dt> <dt>4</dt> </dl>          | Mindestens ein Parameter ist formal ungültig. Der Wert des *DestinationSystem-Parameters* umfasst beispielsweise keinen gültigen Objektpfad. Über den Wert des \[ \] *Out IsMigratable-Parameters wird* kein Ergebnis gemeldet.<br/>                                                                                                                                        |
| <dl> <dt>**Ungültiger Zustand**</dt> <dt>5</dt> </dl>              | Das virtuelle Quellsystem, das Quellhostsystem oder das Zielhostsystem befinden sich in einem Zustand, der die Initiierung der angeforderten Migration des virtuellen Systems zulässt. Dies kann eine temporäre Bedingung sein. Über den Wert des \[ \] *Out IsMigratable-Parameters wird* kein Ergebnis gemeldet.<br/>                                                                                    |
| <dl> <dt>**Inkompatible Parameter**</dt> <dt>6</dt> </dl>    | Mindestens ein Eingabeparameter ist als Satz oder in Bezug auf den Zielhost nicht kompatibel. Der Wert des *NewSettingData-Parameters* enthält beispielsweise Eigenschaften, die vom Zielhostsystem, das durch den Wert des *DestinationSystem-Parameters* identifiziert wird, nicht unterstützt werden. Über den Wert des \[ \] *Out IsMigratable-Parameters wird* kein Ergebnis gemeldet.<br/> |
| <dl> <dt>**DMTF Reserved**</dt> <dt>..</dt> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**Reservierte Methode**</dt> <dt>4097..32767</dt> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**Herstellerspezifisch**</dt> <dt>32768..65535</dt> </dl> |                                                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




