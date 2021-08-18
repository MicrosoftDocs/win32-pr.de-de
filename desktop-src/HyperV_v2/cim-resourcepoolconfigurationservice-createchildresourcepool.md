---
description: Starten Sie einen Auftrag zum Erstellen eines Unterpools aus einem übergeordneten Pool unter Verwendung der angegebenen Zuordnungseinstellungen.
ms.assetid: 9b09221a-7c4e-4648-a2a8-012df1818c3e
title: CreateChildResourcePool-Methode der CIM_ResourcePoolConfigurationService-Klasse
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
ms.openlocfilehash: 48a43baeefcbc56707fa6327930d9c18eaa57a2442b81fbc5f5cff17633b2148
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648152"
---
# <a name="createchildresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>CreateChildResourcePool-Methode der CIM \_ ResourcePoolConfigurationService-Klasse

Starten Sie einen Auftrag zum Erstellen eines Unterpools aus einem übergeordneten Pool unter Verwendung der angegebenen Zuordnungseinstellungen.

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

*ElementName* \[ In\]
</dt> <dd>

Ein für den Endbenutzer relevanter Name für den pool, der erstellt wird. Bei **NULL** kann ein vom System bereitgestellter Standardname verwendet werden. Der Wert wird in der **ElementName-Eigenschaft** für das erstellte Element gespeichert.

</dd> <dt>

*Einstellungen* \[ In\]
</dt> <dd>

Zeichenfolge, die eine Darstellung einer [**CIM \_ SettingData-Instanz**](cim-settingdata.md) enthält, die zum Angeben der Einstellungen für den untergeordneten Pool verwendet wird.

</dd> <dt>

*ParentPool* \[ In\]
</dt> <dd>

Ein [**\_ CIM-Ressourcenpool,**](cim-resourcepool.md) aus dem der neue Pool erstellt werden soll.

</dd> <dt>

*Pool* \[ out\]
</dt> <dd>

Ein [**CIM \_ ResourcePool,**](cim-resourcepool.md) der auf den resultierenden Pool verweist.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Verweis auf den Auftrag (kann NULL sein, wenn der Auftrag abgeschlossen ist).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 zurück. andernfalls wird ein Fehler zurückgegeben.

<dl> <dt>

**Auftrag ohne Fehler abgeschlossen** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Unbekannt** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Fehler** (4)
</dt> <dt>

**Ungültiger Parameter** (5)
</dt> <dt>

**In Verwendung** (6)
</dt> <dt>

**Falscher ResourceType für den Pool** (7)
</dt> <dt>

**Unzureichende Ressourcen** (8)
</dt> <dt>

**DMTF Reserved** (..)
</dt> <dt>

**Überprüfte Methodenparameter – Auftragsstart** (4096)
</dt> <dt>

**Größe wird nicht unterstützt** (4097)
</dt> <dt>

**Reservierte Methode** (4098..32767)
</dt> <dt>

**Herstellerspezifisch** (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ ResourcePoolConfigurationService**](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




