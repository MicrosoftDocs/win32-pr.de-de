---
description: Exportiert den Bezugspunkt des virtuellen Systems.
ms.assetid: e4d80404-6b1b-4153-9ab2-aebab18c331a
title: ExportReferencePoint-Methode der Msvm_VirtualSystemReferencePointService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3273c4781858b02e60b632ae491b1694068a32f5feaddea885576dade6876989
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147953"
---
# <a name="exportreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>ExportReferencePoint-Methode der Msvm \_ VirtualSystemReferencePointService-Klasse

Exportiert den Bezugspunkt des virtuellen Systems.

## <a name="syntax"></a>Syntax


```mof
uint32 ExportReferencePoint(
  [in]  Msvm_VirtualSystemReferencePoint REF ReferencePoint,
  [in]  string                               ExportDirectory,
  [in]  string                               ExportSettingData,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ReferencePoint* \[ In\]
</dt> <dd>

Ein Verweis auf die [**Msvm \_ VirtualSystemReferencePoint-Instanz,**](msvm-virtualsystemreferencepoint.md) die den zu exportierenden Verweispunkt darstellt.

</dd> <dt>

*ExportDirectory* \[ In\]
</dt> <dd>

Der vollqualifizierte Pfad des Verzeichnisses, in das der Verweispunkt exportiert werden soll.

</dd> <dt>

*ExportSettingData* \[ In\]
</dt> <dd>

Eine Instanz von [**Msvm \_ VirtualSystemReferencePointExportSettingData,**](msvm-virtualsystemreferencepointexportsettingdata.md) die die Einstellungen für den Exportvorgang darstellt.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Ein optionaler Parameter zum Überwachen des Fortschritts des Vorgangs, der verwendet wird, wenn die Methode nicht synchron ausgeführt werden konnte. Wenn der Vorgang asynchron ausgeführt wird, ist der Rückgabewert 4096.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg wird 0 (Vollständig ohne Fehler) oder 4096 (Auftrag gestartet) zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Überprüfte Methodenparameter – Auftrag gestartet** (4096)
</dt> <dt>

**Fehler** (32768)
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

**Status ist unbekannt** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger** Parameter (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Zustand für diesen Vorgang** (32775)
</dt> <dt>

**Falscher Datentyp** (32776)
</dt> <dt>

**System ist nicht verfügbar** (32777)
</dt> <dt>

**Nicht genügend Arbeitsspeicher** (32778)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




