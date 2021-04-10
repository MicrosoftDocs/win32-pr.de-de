---
description: Berechnet die Menge an Video Arbeitsspeicher, der für einen virtuellen remotefx-Computer erforderlich ist.
ms.assetid: F8C30601-EDA3-47F1-A717-9FE7E9DB8F62
title: Calculatevideomemoryrequirements-Methode der Msvm_Synth3dVideoPool-Klasse
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
ms.openlocfilehash: 2a9fd80e777a9d166b896c2ce51d03bd91bbabfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129745"
---
# <a name="calculatevideomemoryrequirements-method-of-the-msvm_synth3dvideopool-class"></a>Calculatevideomemoryrequirements-Methode der MSVM \_ Synth3dVideoPool-Klasse

Berechnet die Menge an Video Arbeitsspeicher, der für einen virtuellen remotefx-Computer erforderlich ist.

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

*Monitorauflösung* \[ in\]
</dt> <dd>

Die maximale Monitor Auflösung für den virtuellen Computer. Dabei muss es sich um einen der folgenden Werte handeln:



| Wert                                                                        | Bedeutung                                           |
|------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Die maximale Auflösung beträgt 1024 768.<br/>  |
| <dl> <dt>1</dt> </dl> | Die maximale Auflösung beträgt 1280 1024.<br/> |
| <dl> <dt>2</dt> </dl> | Die maximale Auflösung beträgt 1600 1200.<br/> |
| <dl> <dt>3</dt> </dl> | Die maximale Auflösung beträgt 1920 1200.<br/> |



 

</dd> <dt>

*anzahlüberwachungen* \[ in\]
</dt> <dd>

Die maximale Anzahl von Monitoren für die virtuelle Maschine. Die Mindestanzahl von Monitoren ist 1, und der Höchstwert hängt von der maximalen Bildschirmauflösung ab. In der folgenden Tabelle ist die maximale Anzahl von Monitoren definiert, die für unterschiedliche Auflösungen zulässig sind.



| Lösung             | Maximale Anzahl von Monitoren |
|------------------------|------------------|
| 1024 768<br/>  | 4<br/>     |
| 1280 1024<br/> | 4<br/>     |
| 1600 1200<br/> | 3<br/>     |
| 1920 1200<br/> | 2<br/>     |



 

</dd> <dt>

Requirements *dvideomemory* \[ vorgenommen\]
</dt> <dd>

Empfängt die erforderliche Menge an Videospeicher in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Statuscode zurück, bei dem es sich um einen der folgenden Werte handeln kann.



| Rückgabecode/-wert                                                                                                                                                                | BESCHREIBUNG                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt> </dl>                    | Erfolgreich.<br/>                                |
| <dl> <dt>**Methoden Parameter aktiviert-Auftrag gestartet**</dt> <dt>4096</dt> </dl> | Der Auftrag wurde gestartet.<br/>                               |
| <dl> <dt></dt> Fehler <dt>32768</dt> </dl>                                 | Fehler.<br/>                                    |
| <dl> <dt>**Zugriff verweigert**</dt> <dt>32769</dt> </dl>                          | Zugriff verweigert.<br/>                             |
| <dl> <dt>**Nicht unterstützt**</dt> <dt>32770</dt> </dl>                          | Wird nicht unterstützt.<br/>                             |
| <dl> <dt>**Status ist unbekannt**</dt> <dt>32771</dt> </dl>                      | Der Status ist unbekannt.<br/>                         |
| <dl> <dt>**Timeout**</dt> <dt>32772</dt> </dl>                                | Timeout<br/>                                   |
| <dl> <dt>**Ungültiger Parameter**</dt> <dt>32773</dt> </dl>                      | Ein Parameter ist nicht gültig.<br/>                  |
| <dl> Das <dt>**System wird in**</dt> <dt>32774</dt> verwendet. </dl>                      | Das System wird verwendet.<br/>                          |
| <dl> <dt>**Ungültiger Status für diesen Vorgang**</dt> <dt>32775</dt> </dl>       | Der Status ist für diesen Vorgang ungültig.<br/> |
| <dl> <dt>**Falscher Datentyp**</dt> <dt>32776</dt> </dl>                    | Falscher Datentyp.<br/>                       |
| <dl> <dt>**System ist nicht verfügbar**</dt> <dt>32777</dt> </dl>                | Das System ist nicht verfügbar.<br/>                   |
| <dl> <dt>**Nicht genügend Arbeitsspeicher**</dt> <dt>32778</dt> </dl>                          | Nicht genügend Arbeitsspeicher.<br/>                             |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode wird in der Regel auf dem Host System aufgerufen, um zu bestimmen, ob der Host über ausreichend verfügbaren Videospeicher zum Hosten eines virtuellen remotefx-Computers verfügt. Zu diesem Zweck vergleichen Sie die von dieser Methode berechnete Menge an Videospeicher mit der Eigenschaft [**MSVM \_ physicalgpuinfo. availablevideomemory**](msvm-physicalgpuinfo.md) , um zu bestimmen, ob der Host Computer über ausreichend verfügbaren Videospeicher verfügt. Anhand dieser Informationen können Sie feststellen, ob eine virtuelle Maschine auf das Host System verschoben werden kann.

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

[**MSVM \_ physicalgpuinfo**](msvm-physicalgpuinfo.md)
</dt> <dt>

[**MSVM \_ Synth3dVideoPool**](msvm-synth3dvideopool.md)
</dt> </dl>

 

 




