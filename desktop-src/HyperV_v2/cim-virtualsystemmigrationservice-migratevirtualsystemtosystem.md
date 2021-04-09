---
description: Methode zum Verschieben, migrieren oder Verschieben eines virtuellen Systems in ein Zielsystem.
ms.assetid: 210d31f1-093f-4fd5-afd7-5f028b4cb343
title: MigrateVirtualSystemToSystem-Methode der CIM_VirtualSystemMigrationService-Klasse
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
ms.openlocfilehash: 1459d80785725914cbaa5dda5b81e8d2fabad5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864575"
---
# <a name="migratevirtualsystemtosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a>MigrateVirtualSystemToSystem-Methode der CIM \_ virtualsystemmigrationservice-Klasse

Methode zum Verschieben, migrieren oder Verschieben eines virtuellen Systems in ein Zielsystem.

Rückgabecode Beschreibung:

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

*Computersystem* \[ in\]
</dt> <dd>

Das zu migrierende virtuelle Quellcomputer System.

</dd> <dt>

*DestinationSystem* \[ in\]
</dt> <dd>

Ziel Host System für die Migration des virtuellen Systems.

</dd> <dt>

*Migrationsettingdata* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die eine eingebettete Instanz der [**CIM \_ virtualsystemmigrationsettingdata**](cim-virtualsystemmigrationsettingdata.md) -Klasse enthält, die für den Migrations Vorgang geltende Migrations Einstellungen darstellt.

</dd> <dt>

*Newsystemsettingdata* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die eine eingebettete Instanz der [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) -Klasse enthält, die neue Eigenschaften darstellt, die für das virtuelle System nach der Migration gelten.

</dd> <dt>

*Newresourcesettingdata* \[ in\]
</dt> <dd>

Ein Array von Zeichen folgen, das eine eingebettete Instanz der [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) -Klasse enthält, die neue Eigenschaften darstellt, die für virtuelle Ressourcen im Bereich des virtuellen Systems nach der Migration gelten.

</dd> <dt>

*Newcomputersystem* \[ vorgenommen\]
</dt> <dd>

Verweis auf eine Instanz der [**CIM \_ Computersystem**](cim-computersystem.md) -Klasse, die das virtuelle Computersystem nach der Migration darstellt.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang lange ausgeführt wird, kann optional ein [**CIM-" \_ concretejob**](cim-concretejob.md) " zurückgegeben werden, der den Auftrag darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.



| Rückgabecode/-wert                                                                                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt> </dl>                    | Das virtuelle System wurde migriert.<br/>                                                                                                                                                                                                                                                                    |
| <dl> <dt>**Nicht unterstützt**</dt> <dt>1</dt> </dl>                              | Die Methode wird von der Implementierung nicht unterstützt.<br/>                                                                                                                                                                                                                                                         |
| <dl> <dt></dt> Fehler <dt>2</dt> </dl>                                     | Die Migration des virtuellen Systems ist aus unbekannten Gründen fehlgeschlagen.<br/>                                                                                                                                                                                                                                        |
| <dl> <dt>**Timeout**</dt> <dt>3</dt> </dl>                                    | Timeout bei der Migration virtueller Systeme; der Status des virtuellen Systems ist unbekannt.<br/>                                                                                                                                                                                                                         |
| <dl> <dt>**Ungültiger Parameter**</dt> <dt>4</dt> </dl>                          | Mindestens ein Parameter ist formal ungültig, z. b., wenn der Wert des Ziel System Parameters keinen gültigen Objekt Pfad enthält.<br/>                                                                                                                                                    |
| <dl> <dt>**Ungültiger Status**</dt> <dt>5</dt> </dl>                              | Das virtuelle Quellsystem, das Quell Host System oder das Ziel Host System befinden sich in einem Zustand, der die Initiierung der angeforderten Migration des virtuellen Systems zulässt. Dabei kann es sich um eine temporäre Bedingung handeln.<br/>                                                                                             |
| <dl> Nicht <dt>**kompatible Parameter**</dt> <dt>6</dt> </dl>                    | Mindestens ein Eingabeparameter ist nicht als Satz oder in Bezug auf den Zielhost inkompatibel. Beispielsweise enthält der Wert des *migrationnewsettingdata* -Parameters Eigenschaften, die vom Ziel Host System, das durch den Wert des *DestinationSystem* -Parameters identifiziert wird, nicht unterstützt werden.<br/> |
| <dl> <dt>**DMTF reserviert**</dt> <dt>..</dt> </dl>                             |                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**Methoden Parameter aktiviert-Auftrag gestartet**</dt> <dt>4096</dt> </dl> |                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**Reservierte Methode**</dt> <dt>4097.. 32767</dt> </dl>                  |                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**Hersteller spezifischer**</dt> <dt>32768.. 65535</dt> </dl>                 |                                                                                                                                                                                                                                                                                                            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ virtualsystemmigrationservice**](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




