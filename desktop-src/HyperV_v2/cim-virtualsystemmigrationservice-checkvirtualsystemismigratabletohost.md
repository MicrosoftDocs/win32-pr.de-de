---
description: Methode zum Durchführen einer Vorabüberprüfung, um zu bestimmen, ob ein virtuelles System wahrscheinlich erfolgreich zu einem Zielhost migriert wird, der durch einen Netzwerknamen oder eine IP-Adresse angegeben wird.
ms.assetid: bfcd4063-30fe-4d18-9df9-7b84a680814c
title: CheckVirtualSystemIsMigratableToHost-Methode der CIM_VirtualSystemMigrationService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 061cf41d2c509a1fb670f2fc8fb5d56c98d54e3619bfddae59857c2cf9cc51b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980520"
---
# <a name="checkvirtualsystemismigratabletohost-method-of-the-cim_virtualsystemmigrationservice-class"></a>CheckVirtualSystemIsMigratableToHost-Methode der CIM \_ VirtualSystemMigrationService-Klasse

Methode zum Durchführen einer Vorabüberprüfung, um zu bestimmen, ob ein virtuelles System wahrscheinlich erfolgreich zu einem Zielhost migriert wird, der durch einen Netzwerknamen oder eine IP-Adresse angegeben wird. Diese Methode garantiert nicht, dass eine nachfolgende Migration aufgrund der dynamischen Ressourcenverfügbarkeit immer erfolgreich ist.

Rückgabecodebeschreibung:

Hinweis: Diese Methode ist nur als Übergangslösung vorgesehen, bis die Modellierung der Clusterunterstützung verfügbar ist.

## <a name="syntax"></a>Syntax


```mof
uint32 CheckVirtualSystemIsMigratableToHost(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
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

Ein [**\_ CIM-ComputerSystemverweis**](cim-computersystem.md) auf das zu migrierende virtuelle Quellcomputersystem.

</dd> <dt>

*DestinationHost* \[ In\]
</dt> <dd>

Zielhostsystem für die Migration.

Akzeptable Formate für diesen Parameter werden durch Werte von Elementen der **DestinationHostFormatsSupported-Arrayeigenschaft** in der Instanz der CIM \[ \] [**\_ VirtualSystemMigrationCapabilities**](cim-virtualsystemmigrationcapabilities.md) vermittelt, die durch die [**\_ CIM-ElementCapabilities-Zuordnung zugeordnet**](cim-elementcapabilities.md) ist.

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

*IsMigratable* \[ out\]
</dt> <dd>

Das Migrationsüberprüfungsergebnis, das angibt, ob das virtuelle System erfolgreich migriert werden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg eine 0 zurück. andernfalls gibt einen Fehler zurück.



| Rückgabecode/-wert                                                                                                                                                | Beschreibung                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt> </dl>    | Durchgeführte Überprüfung; Ergebnis, das über den Wert des \[ Out \] *IsMigratable-Parameters gemeldet* wird.<br/>                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**Nicht unterstützt**</dt> <dt>1</dt> </dl>              | Methode, die von der Implementierung nicht unterstützt wird. Über den Wert des Out \[ \] *IsMigratable-Parameters* wird kein Ergebnis gemeldet.<br/>                                                                                                                                                                                                                                                       |
| <dl> <dt>**Fehler**</dt> <dt>2</dt> </dl>                     | Fehler bei der Überprüfung aus nicht angegebenen Gründen. Über den Wert des Out \[ \] *IsMigratable-Parameters* wird kein Ergebnis gemeldet.<br/>                                                                                                                                                                                                                                                         |
| <dl> <dt>**Timeout**</dt> <dt>3</dt> </dl>                    | Check timed out (Timed beim Überprüfen). Über den Wert des Out \[ \] *IsMigratable-Parameters* wird kein Ergebnis gemeldet.<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**Ungültiger Parameter**</dt> <dt>4</dt> </dl>          | Mindestens ein Parameter ist formal ungültig. Beispielsweise hätte der Wert des *Parameters DestinationHost* in einem nicht unterstützten Format angegeben werden können. Über den Wert des Out \[ \] *IsMigratable-Parameters* wird kein Ergebnis gemeldet.<br/>                                                                                                                                    |
| <dl> <dt>**Ungültiger Zustand**</dt> <dt>5</dt> </dl>              | Das virtuelle Quellsystem, das Quellhostsystem oder das Zielhostsystem befinden sich in einem Zustand, der die Initiierung der angeforderten Migration des virtuellen Systems ermöglicht. dies kann eine vorübergehende Bedingung sein. Über den Wert des Out \[ \] *IsMigratable-Parameters* wird kein Ergebnis gemeldet.<br/>                                                                                           |
| <dl> <dt>**Inkompatible Parameter**</dt> <dt>6</dt> </dl>    | Mindestens ein Eingabeparameter ist als Satz oder in Bezug auf den Zielhost inkompatibel. Der Wert des Parameters *MigrationNewSettingData* enthält beispielsweise Eigenschaften, die nicht vom Zielhostsystem unterstützt werden, das durch den Wert des *DestinationHost-Parameters identifiziert* wird. Über den Wert des Out \[ \] *IsMigratable-Parameters* wird kein Ergebnis gemeldet.<br/> |
| <dl> <dt>**DMTF Reserved**</dt> <dt>..</dt> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**Reservierte**</dt> <dt>Methode 4097..32767</dt> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**Herstellerspezifisch**</dt> <dt>32768..65535</dt> </dl> |                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




