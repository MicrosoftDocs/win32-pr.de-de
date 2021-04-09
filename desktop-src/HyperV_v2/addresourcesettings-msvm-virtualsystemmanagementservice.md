---
description: Fügt der Konfiguration einer virtuellen Maschine Ressourcen hinzu.
ms.assetid: e2878b60-dc8c-48fb-b163-29457a96d130
title: Adresssourcesettings-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4b35379e0fe3925bbf0f7c4d753f77d1d207199b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865224"
---
# <a name="addresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Adresssourcesettings-Methode der MSVM \_ virtualsystemmanagementservice-Klasse

Fügt der Konfiguration einer virtuellen Maschine Ressourcen hinzu. Wenn Sie auf eine VM-Konfiguration mit dem Status "State" angewendet werden, werden dem aktiven virtuellen Computerressourcen als Nebeneffekte hinzugefügt.

## <a name="syntax"></a>Syntax


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Affectedconfiguration* \[ in\]
</dt> <dd>

Ein Verweis auf ein [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85)) -Objekt, das die betroffene Konfiguration der virtuellen Maschine darstellt.

</dd> <dt>

*Resourcesettings* \[ in\]
</dt> <dd>

Ein Array von Zeichen folgen, das eine eingebettete Instanz der [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) -Klasse enthält, die die virtuellen Aspekte einer virtuellen Ressource beschreibt, die der virtuellen Maschine hinzugefügt werden soll.

</dd> <dt>

*Resultingresourcesettings* \[ vorgenommen\]
</dt> <dd>

Ein Array von Verweisen auf Instanzen der [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) -Klasse, die virtuelle Aspekte der hinzugefügten virtuellen Ressourcen darstellt.

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

**Nicht unterstützt** (1)
</dt> <dt>

Fehler **(2** )
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Ungültiger Parameter** (4)
</dt> <dt>

**DMTF reserviert** (..)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

**Reservierte Methode** (4097.32767)
</dt> <dt>

**Hersteller spezifisch** (32768.65535)
</dt> </dl>

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

[**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

