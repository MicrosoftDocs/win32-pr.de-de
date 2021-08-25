---
description: Methode zum Verschieben, Migrieren oder Verschieben eines virtuellen Systems in ein Zielsystem.
ms.assetid: 210d31f1-093f-4fd5-afd7-5f028b4cb343
title: MigrateVirtualSystemToSystem-Methode der CIM_VirtualSystemMigrationService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.MigrateVirtualSystemToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7b60e691f2f873a26a52f59def32b35005d45914f7fe379af14b5260b02a0c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393418"
---
# <a name="migratevirtualsystemtosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a>MigrateVirtualSystemToSystem-Methode der CIM \_ VirtualSystemMigrationService-Klasse

Methode zum Verschieben, Migrieren oder Verschieben eines virtuellen Systems in ein Zielsystem.

Rückgabecodebeschreibung:

## <a name="syntax"></a>Syntax


```mof
uint32 MigrateVirtualSystemToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ComputerSystem REF NewComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ComputerSystem* \[ In\]
</dt> <dd>

Quellsystem für virtuelle Computer, das migriert werden soll.

</dd> <dt>

*DestinationSystem* \[ In\]
</dt> <dd>

Zielhostsystem, in das das virtuelle System migriert werden soll.

</dd> <dt>

*MigrationSettingData* \[ In\]
</dt> <dd>

Eine Zeichenfolge, die eine eingebettete Instanz der [**CIM \_ VirtualSystemMigrationSettingData-Klasse**](cim-virtualsystemmigrationsettingdata.md) enthält, die migrationseinstellungen darstellt, die für den Migrationsvorgang gelten.

</dd> <dt>

*NewSystemSettingData* \[ In\]
</dt> <dd>

Eine Zeichenfolge, die eine eingebettete Instanz der [**CIM \_ VirtualSystemSettingData-Klasse**](cim-virtualsystemsettingdata.md) enthält, die neue Eigenschaften darstellt, die nach der Migration auf das virtuelle System anwendbar sind.

</dd> <dt>

*NewResourceSettingData* \[ In\]
</dt> <dd>

Array von Zeichenfolgen, die jeweils eine eingebettete Instanz der [**\_ CIM-Klasse ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) enthalten, die neue Eigenschaften darstellt, die nach der Migration auf virtuelle Ressourcen im Bereich des virtuellen Systems anwendbar sind.

</dd> <dt>

*NewComputerSystem* \[ out\]
</dt> <dd>

Verweis auf eine Instanz der [**\_ CIM-ComputerSystem-Klasse,**](cim-computersystem.md) die das virtuelle Computersystem nach der Migration darstellt.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang lange ausgeführt wird, kann optional ein [**CIM \_ ConcreteJob**](cim-concretejob.md) zurückgegeben werden, der den Auftrag darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg eine 0 zurück. andernfalls gibt einen Fehler zurück.



| Rückgabecode/-wert                                                                                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt> </dl>                    | Das virtuelle System wurde migriert.<br/>                                                                                                                                                                                                                                                                    |
| <dl> <dt>**Nicht unterstützt**</dt> <dt>1</dt> </dl>                              | Methode, die von der Implementierung nicht unterstützt wird.<br/>                                                                                                                                                                                                                                                         |
| <dl> <dt>**Fehler**</dt> <dt>2</dt> </dl>                                     | Fehler bei der Migration des virtuellen Systems aus nicht angegebenen Gründen.<br/>                                                                                                                                                                                                                                        |
| <dl> <dt>**Timeout**</dt> <dt>3</dt> </dl>                                    | Time out für die Migration virtueller Systeme; Der Status des virtuellen Systems ist unbekannt.<br/>                                                                                                                                                                                                                         |
| <dl> <dt>**Ungültiger Parameter**</dt> <dt>4</dt> </dl>                          | Mindestens ein Parameter ist formal ungültig. Der Wert des Zielsystemparameters enthält beispielsweise keinen gültigen Objektpfad.<br/>                                                                                                                                                    |
| <dl> <dt>**Ungültiger Zustand**</dt> <dt>5</dt> </dl>                              | Das virtuelle Quellsystem, das Quellhostsystem oder das Zielhostsystem befinden sich in einem Zustand, der die Initiierung der angeforderten Migration des virtuellen Systems ermöglicht. dies kann eine vorübergehende Bedingung sein.<br/>                                                                                             |
| <dl> <dt>**Inkompatible Parameter**</dt> <dt>6</dt> </dl>                    | Mindestens ein Eingabeparameter ist als Satz oder in Bezug auf den Zielhost inkompatibel. Der Wert des Parameters *MigrationNewSettingData* enthält beispielsweise Eigenschaften, die nicht vom Zielhostsystem unterstützt werden, das durch den Wert des *DestinationSystem-Parameters identifiziert* wird.<br/> |
| <dl> <dt>**DMTF Reserved**</dt> <dt>..</dt> </dl>                             |                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**Überprüfte Methodenparameter – Auftrag gestartet**</dt> <dt>4096</dt> </dl> |                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**Reservierte**</dt> <dt>Methode 4097..32767</dt> </dl>                  |                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**Herstellerspezifisch**</dt> <dt>32768..65535</dt> </dl>                 |                                                                                                                                                                                                                                                                                                            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




