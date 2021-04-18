---
description: Definiert ein virtuelles System.
ms.assetid: c3964e99-9227-4b98-af87-7caa59296306
title: Definesystem-Methode der CIM_VirtualSystemManagementService-Klasse
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
ms.openlocfilehash: 2e38111d52044ed385fdd8cd19dd9094834e794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354637"
---
# <a name="definesystem-method-of-the-cim_virtualsystemmanagementservice-class"></a>Definesystem-Methode der CIM \_ virtualsystemmanagementservice-Klasse

Definiert ein virtuelles System.

Eingaben, die nicht vollständig angegeben sind, können mit Standardwerten aufgefüllt werden.

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

*SystemSettings* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die eine eingebettete Instanz der Klasse [**CIM \_ virtualsystemsettingdata**](cim-virtualsystemsettingdata.md) enthält, die zum Definieren von Attributen des zu erstellenden virtuellen Systems verwendet wird.

</dd> <dt>

*Resourcesettings* \[ in\]
</dt> <dd>

Ein Array von Zeichen folgen, die eine eingebettete Instanz der Klasse [**CIM \_ resourcezucationsettingdata**](cim-resourceallocationsettingdata.md) enthalten, in der die virtuellen Aspekte einer virtuellen Ressource beschrieben werden, die im Bereich des neuen virtuellen Systems erstellt werden soll.

</dd> <dt>

*Referenceconfiguration* \[ in\]
</dt> <dd>

Verweis auf eine [**CIM \_ virtualsystemsettingdat**](cim-virtualsystemsettingdata.md) -Objektinstanz, bei der es sich um das Objekt der obersten Ebene einer virtuellen Referenz Konfiguration handelt. Die Referenz Konfiguration wird verwendet, um die Konfiguration des neuen virtuellen Systems zu ergänzen, wenn die Parameter " *SystemSettings* " und " *resourcesettings* " keine entsprechenden Informationen bereitgestellt haben.

</dd> <dt>

*Resultingsystem* \[ vorgenommen\]
</dt> <dd>

Wenn ein virtuelles Computersystem erfolgreich definiert wurde, wird ein Verweis auf eine Instanz der Klasse " [**CIM \_ Computersystem**](cim-computersystem.md) " zurückgegeben, die das neu definierte System des virtuellen Computers darstellt.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang lange ausgeführt wird, kann optional ein Auftrag zurückgegeben werden. In diesem Fall wird die Instanz der Klasse [**CIM \_ Computersystem**](cim-computersystem.md) , die das neue virtuelle System repräsentiert, über [**Association CIM \_ affectedjobelate**](cim-affectedjobelement.md) mit der Eigenschaft " **affectedelta** " angezeigt, die auf die neue Instanz der Klasse " **CIM \_ Computersystem** " und die Eigenschaft " **elementeffects** " auf 5 (Create) festgelegt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.

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
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ virtualsystemmanagementservice**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




