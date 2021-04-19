---
description: Starten Sie einen Auftrag, um einen untergeordneten Pool aus einem übergeordneten Pool mithilfe der angegebenen Zuordnungs Einstellungen zu erstellen.
ms.assetid: 9b09221a-7c4e-4648-a2a8-012df1818c3e
title: Methode "kreatechildresourcepool" der CIM_ResourcePoolConfigurationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateChildResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e4e709fd240c849581f6dcd343001a9b1dee7003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356797"
---
# <a name="createchildresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Methode "kreatechildresourcepool" der CIM \_ resourcepoolconfigurationservice-Klasse

Starten Sie einen Auftrag, um einen untergeordneten Pool aus einem übergeordneten Pool mithilfe der angegebenen Zuordnungs Einstellungen zu erstellen.

## <a name="syntax"></a>Syntax


```mof
uint32 CreateChildResourcePool(
  [in]  string               ElementName,
  [in]  string               Settings[],
  [in]  CIM_ResourcePool REF ParentPool[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ElementName* \[ in\]
</dt> <dd>

Ein Endbenutzer relevanter Name für den Pool, der erstellt wird. Wenn der Wert **null** ist, kann ein vom System bereitgestellter Standardname verwendet werden. Der Wert wird in der **ElementName** -Eigenschaft für das erstellte Element gespeichert.

</dd> <dt>

*Einstellungen* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die eine-Darstellung einer [**CIM \_ SettingData**](cim-settingdata.md) -Instanz enthält, die verwendet wird, um die Einstellungen für den untergeordneten Pool anzugeben.

</dd> <dt>

*Pool Pool* \[ in\]
</dt> <dd>

Ein [**CIM- \_ resourcepool**](cim-resourcepool.md) , aus dem der neue Pool erstellt werden soll.

</dd> <dt>

*Pool* \[ vorgenommen\]
</dt> <dd>

Ein [**CIM- \_ resourcepool**](cim-resourcepool.md) , der auf den resultierenden Pool verweist.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Verweis auf den Auftrag (kann NULL sein, wenn der Auftrag abgeschlossen ist).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.

<dl> <dt>

**Auftrag ohne Fehler abgeschlossen** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Unbekannt** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

Fehler **(4** )
</dt> <dt>

**Ungültiger Parameter** (5)
</dt> <dt>

**In Gebrauch** (6)
</dt> <dt>

**Falscher ResourceType für den Pool** (7).
</dt> <dt>

**Unzureichende Ressourcen** (8)
</dt> <dt>

**DMTF reserviert** (..)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

**Größe nicht unterstützt** (4097)
</dt> <dt>

**Reservierte Methode** (4098.32767)
</dt> <dt>

**Hersteller spezifisch** (32768.65535)
</dt> </dl>

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

[**CIM \_ resourcepoolconfigurationservice**](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




