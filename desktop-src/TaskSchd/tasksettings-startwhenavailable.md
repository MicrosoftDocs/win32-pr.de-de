---
title: TaskSettings.StartWhenAvailable-Eigenschaft
description: Ruft für die Skripterstellung einen booleschen Wert ab, der angibt, dass die Taskplaner die Aufgabe jederzeit nach Ablauf der geplanten Zeit starten kann, oder legt diesen fest.
ms.assetid: 911de67c-baf8-4346-9b4c-e39e5f96c0fe
keywords:
- StartWhenAvailable-Eigenschaft Taskplaner
- StartWhenAvailable-Eigenschaft Taskplaner , TaskSettings-Objekt
- TaskSettings-Objekt Taskplaner , StartWhenAvailable-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.StartWhenAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0ed43a04bba63d0e760866684df15c4cae5e80a1b3338d122408756f4cec46e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757923"
---
# <a name="tasksettingsstartwhenavailable-property"></a>TaskSettings.StartWhenAvailable-Eigenschaft

Ruft für die Skripterstellung einen booleschen Wert ab, der angibt, dass die Taskplaner die Aufgabe jederzeit nach Ablauf der geplanten Zeit starten kann, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.StartWhenAvailable As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

True gibt die -Eigenschaft an, dass die Taskplaner die Aufgabe jederzeit starten kann, nachdem die geplante Zeit abgelaufen ist. Die Standardeinstellung lautet „false“.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gilt nur für zeitbasierte Aufgaben mit einer Endgrenze oder zeitbasierte Aufgaben, die auf unendliche Wiederholung festgelegt sind.

Aufgaben, die nach Ablauf der geplanten Zeit gestartet werden (weil die [**StartWhenAvailable-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable) auf True festgelegt ist), werden in der Warteschlange des Taskplaner Diensts mit Aufgaben in die Warteschlange eingereiht und nach einer Verzögerung gestartet. Die Standardverzögerung beträgt 10 Minuten.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**StartWhenAvailable-Element**](taskschedulerschema-startwhenavailable-settingstype-element.md) des Taskplaner Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





