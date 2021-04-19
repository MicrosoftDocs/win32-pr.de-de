---
description: Konvertieren einer vorhandenen Momentaufnahme eines virtuellen Systems in einen Referenzpunkt Die Momentaufnahme wird als Nebeneffekt gelöscht. Nur Wiederherstellungs Momentaufnahmen können in Verweis Punkte konvertiert werden.
ms.assetid: c634d749-e18f-4a11-a574-2aee705c0722
title: Converttoreferencepoint-Methode der Msvm_VirtualSystemSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ConvertToReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 18eecc1677abaec5893b3749b4ee82f757cbe93e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346491"
---
# <a name="converttoreferencepoint-method-of-the-msvm_virtualsystemsnapshotservice-class"></a>Converttoreferencepoint-Methode der MSVM \_ virtualsystemsnapshotservice-Klasse

Konvertieren einer vorhandenen Momentaufnahme eines virtuellen Systems in einen Referenzpunkt Die Momentaufnahme wird als Nebeneffekt gelöscht. Nur Wiederherstellungs Momentaufnahmen können in Verweis Punkte konvertiert werden.

## <a name="syntax"></a>Syntax


```mof
uint32 ConvertToReferencePoint(
  [in]      CIM_VirtualSystemSettingData     REF AffectedSnapshot,
  [in]      string                               ReferencePointSettings,
  [in, out] Msvm_VirtualSystemReferencePoint REF ResultingReferencePoint,
  [out]     CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Affectedsnapshot* \[ in\]
</dt> <dd>

Verweis auf die betroffene virtuelle System Momentaufnahme.

</dd> <dt>

*Referencepointsettings* \[ in\]
</dt> <dd>

Parameter Einstellungen.

</dd> <dt>

*Resultingreferencepoint* \[ in, out\]
</dt> <dd>

Resultierender virtueller System-Referenzpunkt

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang lange ausgeführt wird, kann optional ein Auftrag zurückgegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) zurück. Andernfalls wird einer der folgenden Werte zurückgegeben:

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

**Ungültiger Typ** (6)
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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ virtualsystemsnapshotservice**](msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 




