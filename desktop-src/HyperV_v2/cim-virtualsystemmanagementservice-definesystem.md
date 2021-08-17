---
description: Definiert ein virtuelles System.
ms.assetid: c3964e99-9227-4b98-af87-7caa59296306
title: DefineSystem-Methode der CIM_VirtualSystemManagementService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a18145a2b59e1ba93967ad7f1d529466dfc1e6ac094b74d139a36fbe6f77a57a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068640"
---
# <a name="definesystem-method-of-the-cim_virtualsystemmanagementservice-class"></a>DefineSystem-Methode der CIM \_ VirtualSystemManagementService-Klasse

Definiert ein virtuelles System.

Eingaben, die nicht vollständig angegeben sind, können mit Standardwerten ausgefüllt werden.

## <a name="syntax"></a>Syntax


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SystemSettings* \[ In\]
</dt> <dd>

Eine Zeichenfolge, die eine eingebettete Instanz der [**Klasse CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) enthält, die zum Definieren von Attributen des zu erstellenden virtuellen Systems verwendet wird.

</dd> <dt>

*ResourceSettings* \[ In\]
</dt> <dd>

Array von Zeichenfolgen, die jeweils eine eingebettete Instanz der [**Klasse CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) enthalten, die die virtuellen Aspekte einer virtuellen Ressource beschreibt, die im Bereich des neuen virtuellen Systems erstellt werden soll.

</dd> <dt>

*ReferenceConfiguration* \[ In\]
</dt> <dd>

Verweis auf eine [**CIM \_ VirtualSystemSettingDat-Objektinstanz,**](cim-virtualsystemsettingdata.md) die das Objekt der obersten Ebene einer Referenzkonfiguration des virtuellen Systems ist. Die Referenzkonfiguration wird verwendet, um die Konfiguration des neuen virtuellen Systems zu ergänzen, wenn die *Parameter SystemSettings* und *ResourceSettings* keine entsprechenden Informationen bereitstellen.

</dd> <dt>

*ResultingSystem* \[ out\]
</dt> <dd>

Wenn ein virtuelles Computersystem erfolgreich definiert wurde, wird ein Verweis auf eine Instanz der Klasse [**CIM \_ ComputerSystem**](cim-computersystem.md) zurückgegeben, die das neu definierte virtuelle Computersystem darstellt.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang lange ausgeführt wird, kann optional ein Auftrag zurückgegeben werden. In diesem Fall wird die Instanz der Klasse [**CIM \_ ComputerSystem,**](cim-computersystem.md) die das neue virtuelle System darstellt, über die Zuordnung [**CIM \_ AffectedJobElement**](cim-affectedjobelement.md) mit der **Eigenschaft AffectedElement** dargestellt, die auf die neue Instanz der **Klasse CIM \_ ComputerSystem** und die **Eigenschaft ElementEffects** verweist, die auf 5 (Create) festgelegt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg eine 0 zurück. andernfalls gibt einen Fehler zurück.

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

**Überprüfte Methodenparameter – Auftrag gestartet** (4096)
</dt> <dt>

**Reservierte Methode** (4097..32767)
</dt> <dt>

**Herstellerspezifisch** (32768..65535)
</dt> </dl>

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

[**CIM \_ VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




