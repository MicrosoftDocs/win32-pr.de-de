---
description: Erstellt eine neue VM-Instanz.
ms.assetid: 15BC967D-F392-45A6-ACF6-5C2F2334AAE6
title: DefineSystem-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 47b01a2fb0935873b5a36d69376eb09bfe6d4555613c0eb8dc8907589d4f5f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118645809"
---
# <a name="definesystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a>DefineSystem-Methode der Msvm \_ VirtualSystemManagementService-Klasse

Erstellt eine neue VM-Instanz. Eigenschaften, die nicht angegeben sind, werden mit Standardwerten aufgefüllt.

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

Typ: **Zeichenfolge**

Eine eingebettete Instanz der [**Msvm \_ VirtualSystemSettingData-Klasse,**](msvm-virtualsystemsettingdata.md) die zum Definieren der Attribute des zu erstellenden virtuellen Computers verwendet wird. Dieser Parameter ist erforderlich.

</dd> <dt>

*ResourceSettings* \[ In\]
</dt> <dd>

Typ: **\[ \] Zeichenfolge**

Eine Reihe von eingebetteten Instanzen der [**Msvm \_ ResourceAllocationSettingData-Klasse**](msvm-resourceallocationsettingdata.md) (oder abgeleiteter Klassen davon). Zusammen beschreiben diese Instanzen die virtuellen Ressourcen des virtuellen Computers. Für den virtuellen Computer wird unabhängig davon, ob dieser Parameter festgelegt ist, ein Standardsatz von Geräten erstellt. Beispielsweise werden Prozessor und Arbeitsspeicher automatisch erstellt und mit Standardwerten konfiguriert.

</dd> <dt>

*ReferenceConfiguration* \[ In\]
</dt> <dd>

Typ: **CIM \_ VirtualSystemSettingData**

Ein Verweis auf eine Instanz der [**Msvm \_ VirtualSystemSettingData-Klasse,**](msvm-virtualsystemsettingdata.md) die das Objekt der obersten Ebene einer Vm-Referenzkonfiguration ist. Die Referenzkonfiguration wird verwendet, um die Konfiguration des neuen virtuellen Computers zu ergänzen, wenn die Parameter *SystemSettings* und *ResourceSettings* keine entsprechenden Informationen angegeben haben.

</dd> <dt>

*ResultingSystem* \[ out\]
</dt> <dd>

Typ: **CIM \_ ComputerSystem**

Ein Verweis auf eine Instanz der [**CIM \_ ComputerSystem-Klasse,**](/windows/desktop/CIMWin32Prov/cim-computersystem) die den neu erstellten virtuellen Computer darstellt.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Typ: **CIM \_ ConcreteJob**

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein objekt, das von [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))abgeleitet wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Wenn diese Methode synchron ausgeführt wird, wird bei Erfolg 0 zurückgegeben. Wenn diese Methode asynchron ausgeführt wird, wird 4096 zurückgegeben, und der *Job-Ausgabeparameter* kann verwendet werden, um den Fortschritt des asynchronen Vorgangs nachzuverfolgen. Jeder andere Rückgabewert gibt einen Fehler an.

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

## <a name="remarks"></a>Hinweise

Der Zugriff auf die [**Msvm \_ VirtualSystemManagementService-Klasse**](msvm-virtualsystemmanagementservice.md) kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

