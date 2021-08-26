---
description: Fügt einer VM-Konfiguration Ressourcen hinzu.
ms.assetid: e2878b60-dc8c-48fb-b163-29457a96d130
title: AddResourceSettings-Methode der Msvm_VirtualSystemManagementService-Klasse
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
ms.openlocfilehash: 0092b19a0fa4bf41492c42db0b3346607bd3b587a2e57e789815424d94a89850
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900470"
---
# <a name="addresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>AddResourceSettings-Methode der Msvm \_ VirtualSystemManagementService-Klasse

Fügt einer VM-Konfiguration Ressourcen hinzu. Bei Anwendung auf eine Zustandskonfiguration des virtuellen Computers werden dem aktiven virtuellen Computer als Nebeneffekt Ressourcen hinzugefügt.

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

*AffectedConfiguration* \[ In\]
</dt> <dd>

Ein Verweis auf ein [**CIM \_ VirtualSystemSettingData-Objekt,**](/previous-versions//cc136954(v=vs.85)) das die betroffene VM-Konfiguration darstellt.

</dd> <dt>

*ResourceSettings* \[ In\]
</dt> <dd>

Ein Array von Zeichenfolgen, die eine eingebettete Instanz der [**CIM \_ ResourceAllocationSettingData-Klasse**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) enthalten, die die virtuellen Aspekte einer virtuellen Ressource beschreibt, die dem virtuellen Computer hinzugefügt werden soll.

</dd> <dt>

*ResultingResourceSettings* \[ out\]
</dt> <dd>

Ein Array von Verweisen auf Instanzen der [**CIM \_ ResourceAllocationSettingData-Klasse,**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) das virtuelle Aspekte der hinzugefügten virtuellen Ressourcen darstellt.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein objekt, das von [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))abgeleitet wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Fehler** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Ungültiger Parameter** (4)
</dt> <dt>

**DMTF Reserved** (..)
</dt> <dt>

**Überprüfte Methodenparameter – Auftragsstart** (4096)
</dt> <dt>

**Reservierte Methode** (4097..32767)
</dt> <dt>

**Herstellerspezifisch** (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

