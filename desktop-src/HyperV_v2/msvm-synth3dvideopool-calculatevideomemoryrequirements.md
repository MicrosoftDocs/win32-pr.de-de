---
description: Berechnet die Menge an Videospeicher, die für einen virtuellen Computer RemoteFX ist.
ms.assetid: F8C30601-EDA3-47F1-A717-9FE7E9DB8F62
title: CalculateVideoMemoryRequirements-Methode der Msvm_Synth3dVideoPool-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synth3dVideoPool.CalculateVideoMemoryRequirements
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2fd1485cdd4e96155db6540a5f07344add5f413514a92c420fcac78a008e7aca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950079"
---
# <a name="calculatevideomemoryrequirements-method-of-the-msvm_synth3dvideopool-class"></a>CalculateVideoMemoryRequirements-Methode der Msvm \_ Synth3dVideoPool-Klasse

Berechnet die Menge an Videospeicher, die für einen virtuellen Computer RemoteFX ist.

## <a name="syntax"></a>Syntax


```mof
uint32 CalculateVideoMemoryRequirements(
  [in]  uint32 monitorResolution,
  [in]  uint32 numberOfMonitors,
  [out] uint64 requiredVideoMemory
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*monitorResolution* \[ In\]
</dt> <dd>

Die maximale Monitorauflösung für den virtuellen Computer. Dies muss einer der folgenden Werte sein.



| Wert                                                                        | Bedeutung                                           |
|------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Die maximale Auflösung beträgt 1024 768.<br/>  |
| <dl> <dt>1</dt> </dl> | Die maximale Auflösung beträgt 1280 1024.<br/> |
| <dl> <dt>2</dt> </dl> | Die maximale Auflösung beträgt 1600 1200.<br/> |
| <dl> <dt>3</dt> </dl> | Die maximale Auflösung beträgt 1920 1200.<br/> |



 

</dd> <dt>

*numberOfMonitors* \[ In\]
</dt> <dd>

Die maximale Anzahl von Monitoren für den virtuellen Computer. Die Mindestanzahl von Monitoren ist 1, und die maximale Anzahl hängt von der maximalen Bildschirmauflösung ab. In der folgenden Tabelle wird die maximale Anzahl von Monitoren definiert, die für verschiedene Auflösungen zulässig sind.



| Lösung             | Maximale Anzahl von Monitoren |
|------------------------|------------------|
| 1024 768<br/>  | 4<br/>     |
| 1280 1024<br/> | 4<br/>     |
| 1600 1200<br/> | 3<br/>     |
| 1920 1200<br/> | 2<br/>     |



 

</dd> <dt>

*requiredVideoMemory* \[ out\]
</dt> <dd>

Empfängt die erforderliche Menge an Videospeicher in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Statuscode zurück, der einer der folgenden Werte sein kann.



| Rückgabecode/-wert                                                                                                                                                                | Beschreibung                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt> </dl>                    | Erfolgreiche.<br/>                                |
| <dl> <dt>**Überprüfte Methodenparameter – Auftrag gestartet**</dt> <dt>4096</dt> </dl> | Auftrag wurde gestartet.<br/>                               |
| <dl> <dt>**Fehler**</dt> <dt>32768</dt> </dl>                                 | Fehler.<br/>                                    |
| <dl> <dt>**Zugriff verweigert**</dt> <dt>32769</dt> </dl>                          | Zugriff verweigert:<br/>                             |
| <dl> <dt>**Nicht unterstützt**</dt> <dt>32770</dt> </dl>                          | Wird nicht unterstützt.<br/>                             |
| <dl> <dt>**Der Status ist unbekannt**</dt> <dt>32771.</dt> </dl>                      | Der Status ist unbekannt.<br/>                         |
| <dl> <dt>**Timeout**</dt> <dt>32772</dt> </dl>                                | Timeout<br/>                                   |
| <dl> <dt>**Ungültiger Parameter**</dt> <dt>32773</dt> </dl>                      | Ein Parameter ist nicht gültig.<br/>                  |
| <dl> <dt>**System wird in**</dt> <dt>32774 verwendet</dt> </dl>                      | Das System wird verwendet.<br/>                          |
| <dl> <dt>**Ungültiger Zustand für diesen Vorgang**</dt> <dt>32775</dt> </dl>       | Der Zustand ist für diesen Vorgang ungültig.<br/> |
| <dl> <dt>**Falscher Datentyp**</dt> <dt>32776</dt> </dl>                    | Falscher Datentyp.<br/>                       |
| <dl> <dt>**System ist nicht verfügbar**</dt> <dt>32777</dt> </dl>                | Das System ist nicht verfügbar.<br/>                   |
| <dl> <dt>**Nicht genügend Arbeitsspeicher**</dt> <dt>32778</dt> </dl>                          | Nicht genügend Arbeitsspeicher.<br/>                             |



 

## <a name="remarks"></a>Hinweise

Diese Methode wird in der Regel auf dem Hostsystem aufgerufen, um zu bestimmen, ob der Host über genügend verfügbaren Videospeicher zum Hosten eines virtuellen computers RemoteFX verfügt. Hierzu vergleichen Sie die von dieser Methode berechnete Menge an Videospeicher mit der [**Eigenschaft Msvm \_ PhysicalGPUInfo.AvailableVideoMemory,**](msvm-physicalgpuinfo.md) um zu ermitteln, ob auf dem Hostcomputer genügend Videospeicher verfügbar ist. Sie können diese Informationen verwenden, um zu bestimmen, ob ein virtueller Computer in das Hostsystem verschoben werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ PhysicalGPUInfo**](msvm-physicalgpuinfo.md)
</dt> <dt>

[**Msvm \_ Synth3dVideoPool**](msvm-synth3dvideopool.md)
</dt> </dl>

 

 




