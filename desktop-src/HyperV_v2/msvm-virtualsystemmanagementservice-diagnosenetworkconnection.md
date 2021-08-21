---
description: Diagnostizieren der Netzwerkkonnektivität eines virtuellen Computers in Windows Netzwerkvirtualisierungsumgebung
ms.assetid: c18f48bf-1f57-4a23-a495-462afad42750
title: DiagnoseNetworkConnection-Methode der Msvm_VirtualSystemManagementService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DiagnoseNetworkConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9c82f72a9c2a2b16ad991940fcb378c41e75fdf31e9e6f8b74f23f9d115cab93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681129"
---
# <a name="diagnosenetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a>DiagnoseNetworkConnection-Methode der Msvm \_ VirtualSystemManagementService-Klasse

Diagnostizieren der Netzwerkkonnektivität eines virtuellen Computers in Windows Netzwerkvirtualisierungsumgebung

## <a name="syntax"></a>Syntax


```mof
uint32 DiagnoseNetworkConnection(
  [in]  Msvm_EthernetPortAllocationSettingData REF TargetNetworkAdapter,
  [in]  string                                     DiagnosticSettings,
  [out] string                                     DiagnosticInformation,
  [out] CIM_ConcreteJob                        REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TargetNetworkAdapter* \[ In\]
</dt> <dd>

Verweis auf ein [**Msvm \_ EthernetPortAllocationSettingData-Objekt,**](msvm-ethernetportallocationsettingdata.md) das den Zielnetzwerkadapter beschreibt.

</dd> <dt>

*DiagnosticSettings* \[ In\]
</dt> <dd>

Die zu verwendenden Diagnoseeinstellungen.

</dd> <dt>

*DiagnosticInformation* \[ out\]
</dt> <dd>

Bei Erfolg gibt die Diagnoseinformationen zurück.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ ConcreteJob abgeleitet wurde.**](/previous-versions//cc136808(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert von 0 oder 4096 zurück. andernfalls gibt einen Fehler zurück.

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
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1703 desktop apps only (Nur \[ Desktop-Apps der Version 1703)\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

