---
title: System Monitor collectsample-Methode
description: Gibt einen Wert für jeden Zähler im Counter-Objekt an.
ms.assetid: 4c91c759-597f-4aa8-aa77-eb181616e8b0
keywords:
- Collectsample-Methode (Sysmon)
- Collectsample-Methode (Sysmon), Systemmonitor-Schnittstelle
- Systemmonitor-Schnittstelle sysmon, collectsample-Methode
topic_type:
- apiref
api_name:
- SystemMonitor.CollectSample
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1c269d044c17a2ec1322fa969e0c86f468a901
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477097"
---
# <a name="systemmonitorcollectsample-method"></a>Systemmonitor:: collectsample-Methode

Gibt einen Wert für jeden Zähler [**im Counter-Objekt an**](counters.md) .

## <a name="syntax"></a>Syntax


```VB
Sub CollectSample()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

" **Collectsample** " nur dann aufzurufen, wenn " [**ManualUpdate**](systemmonitor-manualupdate.md) " den Wert "true" hat und Sie Stichprobenwerte aus der aktuellen Aktivität des Computers verwenden, verwenden Sie diese Methode nicht, wenn Sie eine Stichprobenentnahme Das Diagramm oder der Bericht wird mit dem neuen Wert aktualisiert. Beachten Sie, dass für einige Arten von Diagrammen zwei Beispiele erforderlich sind, um die Daten zu Graphen, z. b. das Liniendiagramm.

Implementieren Sie das [**onsamplegesammel-**](-systemmonitor-onsamplecollected.md) Ereignis, um eine Benachrichtigung zu erhalten, wenn das Beispiel erfasst wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Counters**](counters.md)
</dt> <dt>

[**System Monitor**](systemmonitor.md)
</dt> </dl>

 

 





