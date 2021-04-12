---
description: Erstellt eine neue Instanz eines virtuellen Computers.
ms.assetid: 15BC967D-F392-45A6-ACF6-5C2F2334AAE6
title: Definesystem-Methode der Msvm_VirtualSystemManagementService-Klasse
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
ms.openlocfilehash: 965d24313607a767d546503d005a6493234b2f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217187"
---
# <a name="definesystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Definesystem-Methode der MSVM \_ virtualsystemmanagementservice-Klasse

Erstellt eine neue Instanz eines virtuellen Computers. Eigenschaften, die nicht angegeben sind, werden mit Standardwerten aufgefüllt.

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

Typ: **Zeichenfolge**

Eine eingebettete Instanz der [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Klasse, die verwendet wird, um die Attribute der zu erstellenden virtuellen Maschine zu definieren. Dieser Parameter ist erforderlich.

</dd> <dt>

*Resourcesettings* \[ in\]
</dt> <dd>

Typ: **Zeichen \[ \] Folge**

Eine Reihe von eingebetteten Instanzen der [**MSVM \_ resourcezucationsettingdata**](msvm-resourceallocationsettingdata.md) -Klasse (oder abgeleitete Klassen). Diese Instanzen beschreiben die virtuellen Ressourcen des virtuellen Computers. Ein Standardsatz von Geräten wird für den virtuellen Computer erstellt, unabhängig davon, ob dieser Parameter festgelegt ist. Beispielsweise werden Prozessor und Arbeitsspeicher automatisch mit Standardwerten erstellt und konfiguriert.

</dd> <dt>

*Referenceconfiguration* \[ in\]
</dt> <dd>

Typ: **CIM \_ virtualsystemsettingdata**

Ein Verweis auf eine Instanz der [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md) -Klasse, bei der es sich um das Objekt der obersten Ebene einer Referenz Konfiguration für virtuelle Maschinen handelt. Die Referenz Konfiguration wird verwendet, um die Konfiguration der neuen virtuellen Maschine zu ergänzen, wenn die Parameter " *SystemSettings* " und " *resourcesettings* " keine entsprechenden Informationen bereitgestellt haben.

</dd> <dt>

*Resultingsystem* \[ vorgenommen\]
</dt> <dd>

Typ: **CIM \_ Computersystem**

Ein Verweis auf eine Instanz der [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Klasse, die den neu erstellten virtuellen Computer darstellt.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Typ: **CIM \_ bettejob**

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Wenn diese Methode synchron ausgeführt wird, wird 0 zurückgegeben, wenn Sie erfolgreich ausgeführt wird. Wenn diese Methode asynchron ausgeführt wird, wird 4096 zurückgegeben, und der *Auftrags* Ausgabeparameter kann verwendet werden, um den Fortschritt des asynchronen Vorgangs zu verfolgen. Jeder andere Rückgabewert gibt einen Fehler an.

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

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

 

