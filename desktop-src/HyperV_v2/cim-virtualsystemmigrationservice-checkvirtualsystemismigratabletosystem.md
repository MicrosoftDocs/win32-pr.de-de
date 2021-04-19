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
ms.openlocfilehash: be85c51cb507fea3cea14f1706ffa8f67af06c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348947"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a>CheckVirtualSystemIsMigratableToSystem-Methode der CIM \_ virtualsystemmigrationservice-Klasse

Methode zum Durchführen einer vorab Überprüfung, um zu bestimmen, ob ein virtuelles System wahrscheinlich erfolgreich zu einem Zielsystem migriert wird. Diese Methode garantiert nicht, dass eine nachfolgende Migration aufgrund dynamischer Ressourcen Verfügbarkeit immer erfolgreich ist. Rückgabecode Beschreibung:

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

*Computersystem* \[ in\]
</dt> <dd>

[**CIM \_ Computersystem**](cim-computersystem.md) Instanz, die auf das zu migrierende virtuelle Quellcomputer System verweist.

</dd> <dt>

*DestinationSystem* \[ in\]
</dt> <dd>

[**CIM \_ System**](cim-system.md) Instanz, die auf das Zielsystem verweist, auf das das virtuelle System migriert werden soll.

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

*IsMigratable* \[ vorgenommen\]
</dt> <dd>

Das Ergebnis der Migrations Überprüfung, das angibt, ob das virtuelle System erfolgreich migriert werden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.



| Rückgabecode/-wert                                                                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt> </dl>    | Überprüfung durchgeführt Das Ergebnis wurde über den Wert des \[ out \] *IsMigratable* -Parameters berichtet.<br/>                                                                                                                                                                                                                                                                          |
| <dl> <dt>**Nicht unterstützt**</dt> <dt>1</dt> </dl>              | Die Methode wird von der Implementierung nicht unterstützt. Es wurde kein Ergebnis über den Wert des \[ out \] *IsMigratable* -Parameters berichtet.<br/>                                                                                                                                                                                                                                                |
| <dl> <dt></dt> Fehler <dt>2</dt> </dl>                     | Überprüfen von nicht spezifizierten Gründen fehlgeschlagen. Es wurde kein Ergebnis über den Wert des \[ out \] *IsMigratable* -Parameters berichtet.<br/>                                                                                                                                                                                                                                                  |
| <dl> <dt>**Timeout**</dt> <dt>3</dt> </dl>                    | Timeout bei der Überprüfung. Es wurde kein Ergebnis über den Wert des \[ out \] *IsMigratable* -Parameters berichtet.<br/>                                                                                                                                                                                                                                                                       |
| <dl> <dt>**Ungültiger Parameter**</dt> <dt>4</dt> </dl>          | Mindestens ein Parameter ist formal ungültig. Beispielsweise besteht der Wert des *DestinationSystem* -Parameters nicht aus einem gültigen Objekt Pfad. Es wurde kein Ergebnis über den Wert des \[ out \] *IsMigratable* -Parameters berichtet.<br/>                                                                                                                                        |
| <dl> <dt>**Ungültiger Status**</dt> <dt>5</dt> </dl>              | Das virtuelle Quellsystem, das Quell Host System oder das Ziel Host System befinden sich in einem Zustand, der die Initiierung der angeforderten Migration des virtuellen Systems zulässt. Dabei kann es sich um eine temporäre Bedingung handeln. Es wurde kein Ergebnis über den Wert des \[ out \] *IsMigratable* -Parameters berichtet.<br/>                                                                                    |
| <dl> Nicht <dt>**kompatible Parameter**</dt> <dt>6</dt> </dl>    | Mindestens ein Eingabeparameter ist nicht als Satz oder in Bezug auf den Zielhost inkompatibel. Beispielsweise enthält der Wert des *newsettingdata* -Parameters Eigenschaften, die vom Ziel Host System, das durch den Wert des *DestinationSystem* -Parameters identifiziert wird, nicht unterstützt werden. Es wurde kein Ergebnis über den Wert des \[ out \] *IsMigratable* -Parameters berichtet.<br/> |
| <dl> <dt>**DMTF reserviert**</dt> <dt>..</dt> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**Reservierte Methode**</dt> <dt>4097.. 32767</dt> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**Hersteller spezifischer**</dt> <dt>32768.. 65535</dt> </dl> |                                                                                                                                                                                                                                                                                                                                                                                 |



 

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

 

 




