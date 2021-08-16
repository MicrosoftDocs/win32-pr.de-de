---
description: Enthält zu setzende Akkuinformationen.
ms.assetid: 535e56cb-2bab-458a-84a8-2d9a4d96412b
title: BATTERY_SET_INFORMATION -Struktur (Poclass.h)
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
ms.openlocfilehash: c53e9c539f8ef20b184c6c056999c7c541f3c1718bafaa58c0b1e20dcef16a97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143613"
---
# <a name="battery_set_information-structure"></a>BATTERY \_ SET \_ INFORMATION-Struktur

Enthält zu setzende Akkuinformationen. Diese Struktur wird mit dem [**IOCTL \_ BATTERY \_ SET \_ INFORMATION-Steuerungscode**](ioctl-battery-set-information.md) verwendet.

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

**BatteryTag**
</dt> <dd>

Das aktuelle Akkutag für den Akku. Informationen zu einem Akku, der mit dem Tag übereinstimmen, können nur zurückgegeben werden. Wenn dieser Wert nicht mit dem aktuellen Tag des Akkus übereinstimmen, wird die IOCTL-Anforderung mit ERROR FILE NOT FOUND abgeschlossen, was dem Aufrufer angibt, dass der Akku, für den er ein Tag hat, nicht mehr vorhanden \_ \_ \_ ist. Der Aufrufer kann den [**IOCTL \_ BATTERY QUERY \_ \_ TAG-Vorgang**](ioctl-battery-query-tag.md) verwenden, um das Tag des neu installierten Akkus zu bestimmen, sofern vorhanden. (Weitere [Informationen finden Sie unter Akkutags.)](battery-information.md)

Wenn eine Abfrageinformationsanforderung erfolgt, wird dieser Wert überprüft. Wenn die Anforderung noch in Bearbeitung ist, während sich dieser Wert ändert, wird die Anforderung mit dem Status ERROR \_ FILE NOT FOUND \_ (FEHLERDATEI NICHT \_ GEFUNDEN) abgebrochen.

</dd> <dt>

**InformationLevel**
</dt> <dd>

Die akku-Informationen, die festgelegt werden sollen. Der Typ der Daten im **Buffer-Member** hängt vom Wert dieses Members ab. Dieser Member kann einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                                       | Bedeutung                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BatteryCharge"></span><span id="batterycharge"></span><span id="BATTERYCHARGE"></span><dl> <dt>**BatteryCharge**</dt> <dt>1</dt> </dl>                         | Informiert das Akkugerät darüber, dass der Benutzer angefordert hat, dass der Akku zu diesem Zeitpunkt geladen werden soll. Beispielsweise kann die Anwendung mit einem intelligenten Akku/Akku/Akku/Selektor einen Akku nach dem anderen aufladen. Der **Buffer-Member** dieser -Struktur wird ignoriert.<br/>                                                                      |
| <span id="BatteryCriticalBias"></span><span id="batterycriticalbias"></span><span id="BATTERYCRITICALBIAS"></span><dl> <dt>**BatteryCriticalBias**</dt> <dt>0</dt> </dl> | Legt die kritische Voreingenommenheitsanpassung des Akkus fest. Beachten Sie, dass nicht vorgesehen ist, dass dieser Wert normalerweise von Software geändert wird und nur als Wartungsfeature in den Schnittstellen vorhanden ist. Nicht alle Akkus können eine solche Einstellung verwalten, und die Akkuinformationen sollten gelesen werden, um zu bestätigen, dass der Akku die Einstellung akzeptiert hat.<br/> |
| <span id="BatteryDischarge"></span><span id="batterydischarge"></span><span id="BATTERYDISCHARGE"></span><dl> <dt>**BatteryDischarge**</dt> <dt>2</dt> </dl>             | Informiert das Akkugerät darüber, dass der Benutzer angefordert hat, dass der Akku zu diesem Zeitpunkt entladen wird. Dies kann beispielsweise verwendet werden, um anzugeben, welche Akkukapazität der Benutzer derzeit an das System anhing. Der **Buffer-Member** dieser -Struktur wird ignoriert.<br/>                                                                          |



 

</dd> <dt>

**Buffer**
</dt> <dd>

Die akku-Informationen, die festgelegt werden sollen. Die Daten hängen vom Wert von **InformationLevel ab.**

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **BATTERY \_ SET \_ INFORMATION-Struktur** ist eine Struktur variabler Länge, und Sie müssen einen Puffer mit geeigneter Größe zuordnen, damit die Informationen in die Struktur aufgenommen werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                                                                                                                                                                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                                                                                                                                                                                |
| Header<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>Batclass.h auf Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003</dt> und Windows XP </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_IOCTL-AKKUSATZINFORMATIONEN \_ \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

 




