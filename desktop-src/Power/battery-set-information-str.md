---
description: Enthält Akku Informationen, die festgelegt werden sollen.
ms.assetid: 535e56cb-2bab-458a-84a8-2d9a4d96412b
title: BATTERY_SET_INFORMATION-Struktur (poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_SET_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: 0b23489bc5a7608e2e8afb297bb4be7ba35cecb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131673"
---
# <a name="battery_set_information-structure"></a>Struktur der Batterie \_ Satz \_ Informationen

Enthält Akku Informationen, die festgelegt werden sollen. Diese Struktur wird zusammen mit dem [**ioctl-Code für die \_ Akku \_ Satz \_ Informationen**](ioctl-battery-set-information.md) verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef struct _BATTERY_SET_INFORMATION {
  ULONG                         BatteryTag;
  BATTERY_SET_INFORMATION_LEVEL InformationLevel;
  UCHAR                         Buffer[1];
} BATTERY_SET_INFORMATION, *PBATTERY_SET_INFORMATION;
```



## <a name="members"></a>Member

<dl> <dt>

**Batterytag**
</dt> <dd>

Das aktuelle Akku Kennzeichen für den Akku. Informationen zu einem Akku, der mit dem Tag übereinstimmt, können nur zurückgegeben werden. Wenn dieser Wert nicht mit dem aktuellen Tag des Akkus identisch ist, wird die ioctl-Anforderung mit der Fehler \_ Datei "nicht gefunden" abgeschlossen, was dem Aufrufer anzeigt, \_ \_ dass der Akku, für den er ein Tag besitzt, nicht mehr vorhanden ist. Der Aufrufer kann den [**IOCTL- \_ Akku- \_ abfragetagvorgang \_**](ioctl-battery-query-tag.md) verwenden, um das Tag des neu installierten Akkus zu ermitteln, sofern vorhanden. (Weitere Informationen finden Sie unter [Akku-Tags](battery-information.md) .)

Wenn eine Abfrage Informationsanforderung erfolgt, wird dieser Wert überprüft. Wenn die Anforderung ausgeführt wird, während sich dieser Wert ändert, wird die Anforderung mit dem Status "Fehler \_ Datei nicht gefunden" abgebrochen \_ \_ .

</dd> <dt>

**Informationlevel**
</dt> <dd>

Die Akku Informationen, die festgelegt werden sollen. Der Typ der Daten im **Puffer** Element hängt vom Wert dieses Members ab. Dieser Member kann einen der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryCharge"></span><span id="batterycharge"></span><span id="BATTERYCHARGE"></span><dl> <dt>**Akkuladung**</dt> <dt>1</dt> </dl>                         | Informiert das Akku Gerät, dass der Benutzer zu diesem Zeitpunkt die Abrechnung durch den Akku angefordert hat. Beispielsweise kann die Anwendung mit einem intelligenten Akku/Ladegerät/Selektor jeweils eine Akkukapazität berechnen. Der **puffermember** dieser Struktur wird ignoriert.<br/>                                                                      |
| <span id="BatteryCriticalBias"></span><span id="batterycriticalbias"></span><span id="BATTERYCRITICALBIAS"></span><dl> <dt>**Batterycriticalbias**</dt> <dt>0</dt> </dl> | Legt die kritische Bias-Anpassung des Akkus fest. Beachten Sie, dass dieser Wert normalerweise von Software geändert wird und in den Schnittstellen nur als Wartungs Feature vorhanden ist. Nicht alle Akkus können eine solche Einstellung beibehalten, und die Akku Informationen sollten gelesen werden, um zu bestätigen, dass der Akku die Einstellung akzeptiert hat.<br/> |
| <span id="BatteryDischarge"></span><span id="batterydischarge"></span><span id="BATTERYDISCHARGE"></span><dl> <dt>**Akku Entladung**</dt> <dt>2</dt> </dl>             | Informiert das Akku Gerät, dass der Benutzer zu diesem Zeitpunkt die Entladung des Akkus angefordert hat. Dies könnte beispielsweise verwendet werden, um anzugeben, welche Akkukapazität der Benutzer zurzeit für das System benötigt. Der **puffermember** dieser Struktur wird ignoriert.<br/>                                                                          |



 

</dd> <dt>

**Buffer**
</dt> <dd>

Die Akku Informationen, die festgelegt werden sollen. Die Daten hängen vom Wert von **informationlevel** ab.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Struktur der **Batterie \_ Satz \_ Informationen** ist eine Struktur mit variabler Länge, und Sie müssen einen Puffer der passenden Größe zuordnen, damit die Informationen in die Struktur eingeschlossen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                                                                                                                                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>Batclass. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IOCTL- \_ Akku \_ Satz \_ Informationen**](ioctl-battery-set-information.md)
</dt> </dl>

 

 




