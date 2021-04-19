---
description: Bestimmt, ob das angegebene virtuelle System zu einem Zielsystem migriert werden kann.
ms.assetid: 2E340737-DEE9-4853-ACD8-BEE2A8C69D6D
title: CheckVirtualSystemIsMigratableToSystem-Methode der Msvm_VirtualSystemMigrationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3e8f294f7e30740e3afab8987c734dbbdbd12acf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345667"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-msvm_virtualsystemmigrationservice-class"></a>CheckVirtualSystemIsMigratableToSystem-Methode der MSVM \_ virtualsystemmigrationservice-Klasse

Bestimmt, ob das angegebene virtuelle System zu einem Zielsystem migriert werden kann.

## <a name="syntax"></a>Syntax


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  Msvm_ComputerSystem REF ComputerSystem,
  [in]  Msvm_ComputerSystem REF DestinationSystem,
  [in]  string                  MigrationSettingData,
  [in]  string                  NewSystemSettingData,
  [in]  string                  NewResourceSettingData[],
  [out] boolean                 IsMigratable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Computersystem* \[ in\]
</dt> <dd>

Ein Verweis auf eine Instanz der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse, die den virtuellen Computer zum Testen der Migrations Fähigkeit von darstellt.

</dd> <dt>

*DestinationSystem* \[ in\]
</dt> <dd>

Ein Verweis auf eine Instanz der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse, die den virtuellen Computer zum Testen der Migrations Fähigkeit darstellt.

</dd> <dt>

*Migrationsettingdata* \[ in\]
</dt> <dd>

Eine eingebettete Instanz der [**MSVM \_ virtualsystemmigrationsettingdata**](msvm-virtualsystemmigrationsettingdata.md) -Klasse, die Einstellungen für den Migrations Vorgang darstellt.

</dd> <dt>

*Newsystemsettingdata* \[ in\]
</dt> <dd>

Eine eingebettete Instanz der [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Klasse, die neue Eigenschaften darstellt, die für das virtuelle System nach der Migration gelten.

</dd> <dt>

*Newresourcesettingdata* \[ in\]
</dt> <dd>

Ein Array von Zeichen folgen, die eine eingebettete Instanz der [**MSVM \_ resourcezucationsettingdata**](msvm-resourceallocationsettingdata.md) -Klasse enthalten, die die neuen Eigenschaften darstellt, die für virtuelle Ressourcen des virtuellen Systems nach der Migration gelten.

</dd> <dt>

*IsMigratable* \[ vorgenommen\]
</dt> <dd>

Empfängt das Ergebnis der Migrations Überprüfung, das angibt, ob das virtuelle System erfolgreich migriert werden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

Fehler **(2** )
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Ungültiger Parameter** (4)
</dt> <dt>

**Ungültiger Status** (5)
</dt> <dt>

Nicht **kompatible Parameter** (6)
</dt> <dt>

**DMTF reserviert** (..)
</dt> <dt>

**Reservierte Methode** (4097.32767)
</dt> <dt>

**Hersteller spezifisch** (32768.65535)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ virtualsystemmigrationservice**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




