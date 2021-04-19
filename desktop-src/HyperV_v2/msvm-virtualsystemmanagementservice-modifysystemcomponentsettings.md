---
description: Ändert die generischen Systemkomponenten Einstellungen.
ms.assetid: e745be32-c26a-4343-99c8-950788243adf
title: Modifysystemcomponentsettings-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifySystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e9495256d1b7610bebdac1fb2cc8b70960a63304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346904"
---
# <a name="modifysystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Modifysystemcomponentsettings-Methode der MSVM \_ virtualsystemmanagementservice-Klasse

Ändert die generischen Systemkomponenten Einstellungen.

## <a name="syntax"></a>Syntax


```mof
uint32 ModifySystemComponentSettings(
  [in]  string                              ComponentSettings[],
  [out] Msvm_SystemComponentSettingData REF ResultingComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Componentsettings* \[ in\]
</dt> <dd>

Ein Array von zu aktualisierenden Komponenten Einstellungen.

</dd> <dt>

*Resultingcomponentsettings* \[ vorgenommen\]
</dt> <dd>

Bei Erfolg wird ein Array von [**MSVM \_ systemcomponentsettingdata**](msvm-systemcomponentsettingdata.md) zurückgegeben, das auf die resultierenden Komponenten Einstellungen verweist.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg wird 0 oder 4096 zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.

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

**Ungültiger Status** (5)
</dt> <dt>

Nicht **kompatible Parameter** (6)
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
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1703, \[ nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

