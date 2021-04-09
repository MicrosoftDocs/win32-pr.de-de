---
description: Erstellt einen neuen virtuellen Switch.
ms.assetid: de7495e9-48c5-427a-b9bb-0821b53a9b09
title: Definesystem-Methode der Msvm_VirtualEthernetSwitchManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bd6e2dfb7d9cf7e64fb76c35f6f3c3b8457d69d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867076"
---
# <a name="definesystem-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a>Definesystem-Methode der MSVM \_ virtualethernettwitchmanagementservice-Klasse

Erstellt einen neuen virtuellen Switch. Eigenschaften, die nicht angegeben sind, werden mit Standardwerten aufgefüllt.

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

Eine eingebettete Instanz der [**MSVM \_ virtualethernetzwitchsettingdata**](msvm-virtualethernetswitchsettingdata.md) -Klasse, die verwendet wird, um die Attribute des zu erstellenden virtuellen Switches zu definieren. Dieser Parameter ist erforderlich.

</dd> <dt>

*Resourcesettings* \[ in\]
</dt> <dd>

Ein Array von eingebetteten Instanzen der [**MSVM-Klasse \_ ethernetportzudationsettingdata**](msvm-ethernetportallocationsettingdata.md) , die die Einstellungen der Switchports beschreibt, die im Bereich des neuen virtuellen Switches erstellt werden sollen. Wenn **null** angegeben wird, wird der virtuelle Switch ohne Ressourcen erstellt (d. h. keine Switchports).

</dd> <dt>

*Referenceconfiguration* \[ in\]
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*Resultingsystem* \[ vorgenommen\]
</dt> <dd>

Wenn ein virtueller Switch erfolgreich erstellt wurde, ist dies ein Verweis auf eine Instanz der [**MSVM \_ virtualethernwitch**](msvm-virtualethernetswitch.md) -Klasse, die den neu definierten virtuellen Switch darstellt.

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

[**MSVM \_ virtualethernetzwitchmanagementservice**](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

