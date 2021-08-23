---
description: Ändert einstellungen des virtuellen Systems.
ms.assetid: 9c3d28f8-9806-411a-866f-d062c6d31818
title: ModifySystemSettings-Methode der CIM_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 82b35038d3c358645478b82e5c2c5ef023941ab3fc443299b2c493522c822878
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068630"
---
# <a name="modifysystemsettings-method-of-the-cim_virtualsystemmanagementservice-class"></a>ModifySystemSettings-Methode der CIM \_ VirtualSystemManagementService-Klasse

Ändert einstellungen des virtuellen Systems.

Bei Anwendung auf die Systemeinstellungen einer "aktuellen" konfiguration des virtuellen Systems kann die virtuelle Systeminstanz als Nebeneffekt geändert werden.

## <a name="syntax"></a>Syntax


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SystemSettings* \[ In\]
</dt> <dd>

Zeichenfolge, die eine Instanz der [**Cim \_ VirtualSystemSettingData-Klasse**](cim-virtualsystemsettingdata.md) enthält, die zum Ändern der Einstellungen des virtuellen Systems verwendet wird. Die Instanz muss über eine gültige **Instanz-ID** verfügen, um die zu ändernde Einstellung des virtuellen Systems zu identifizieren.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang lange ausgeführt wird, kann optional ein [**CIM \_ ConcreteJob**](cim-concretejob.md) zurückgegeben werden, der den Auftrag darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Wert 0 zurück. andernfalls wird ein Fehler zurückgegeben.

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

**Ungültiger Zustand** (5)
</dt> <dt>

**Inkompatible Parameter** (6)
</dt> <dt>

**DMTF Reserved** (..)
</dt> <dt>

**Überprüfte Methodenparameter – Auftragsstart** (4096)
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
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




