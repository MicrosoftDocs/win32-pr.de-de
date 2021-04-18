---
description: Die cbasereferenceclock-Klasse implementiert eine Referenzuhr.
ms.assetid: 898e1968-a9ab-4bb9-abf0-943bfae502e2
title: Cbasereferenceclock-Klasse (Ref. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1da55a57faac201a2dbf0ef4d8a9774157d9215d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358608"
---
# <a name="cbasereferenceclock-class"></a>Cbasereferenceclock-Klasse

![cbasereferenceclock-Klassenhierarchie](images/rclock01.png)

Die- `CBaseReferenceClock` Klasse implementiert eine verweisuhr.



| Geschützte Member-Variablen                                                         | BESCHREIBUNG                                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**m \_ pschedule**](cbasereferenceclock-m-pschedule.md)                            | Ein " [**camschedule**](camschedule.md) "-Objekt, das Planungsaufgaben für die Uhr behandelt. |
| Geschützte Methoden                                                                  | BESCHREIBUNG                                                                            |
| [**~ Cbasereferenceclock**](cbasereferenceclock--cbasereferenceclock.md)           | Dekonstruktormethode.                                                                     |
| Öffentliche Methoden                                                                     | BESCHREIBUNG                                                                            |
| [**Cbasereferenceclock**](cbasereferenceclock-cbasereferenceclock.md)             | Konstruktormethode.                                                                    |
| [**Getprivatetime**](cbasereferenceclock-getprivatetime.md)                       | Ruft die tatsächliche Uhrzeit von der Uhr ab.                                                |
| [**Settimedelta**](cbasereferenceclock-settimedelta.md)                           | Passt die interne Uhrzeit an.                                                       |
| [**Getschedule**](cbasereferenceclock-getschedule.md)                             | Ruft einen Zeiger auf das Zeit Planungs Objekt der Uhr ab.                                  |
| [**Triggerthread**](cbasereferenceclock-triggerthread.md)                         | Aktiviert den Arbeits Thread, der die Planung verarbeitet.                                    |
| IReferenceClock-Methoden                                                            | BESCHREIBUNG                                                                            |
| [**GetTime**](cbasereferenceclock-gettime.md)                                     | Ruft den aktuellen Verweis Zeitpunkt ab.                                                  |
| [**Empfehlungen**](cbasereferenceclock-advisetime.md)                               | Erstellt eine One-Shot-anforderungsanforderung.                                                     |
| [**Empfehlungen regelmäßig**](cbasereferenceclock-adviseperiodic.md)                       | Erstellt eine regelmäßige anforderungsanforderung.                                                     |
| [**Unadvise**](cbasereferenceclock-unadvise.md)                                   | Entfernt eine ausstehende Benachrichtigungs Anforderung.                                                      |
| Ireferenceclocktimercontrol-Methoden                                                | BESCHREIBUNG                                                                            |
| [**Getdefaulttimerresolution**](cbasereferenceclock-getdefaulttimerresolution.md) | Gibt die aktuelle Auflösung des Zeit Gebers der verweisuhr zurück.                         |
| [**Setdefaulttimerresolution**](cbasereferenceclock-setdefaulttimerresolution.md) | Legt die Auflösung des Zeit Gebers der verweisuhr fest.                                    |
| Hilfsfunktionen                                                                   | BESCHREIBUNG                                                                            |
| [**Convertummillisekunden**](converttomilliseconds.md)                             | Konvertiert eine Verweis Zeit in Millisekunden.                                             |



 

## <a name="remarks"></a>Bemerkungen

Diese Klasse implementiert eine Referenzuhr, die die Schnittstellen [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) und [**ireferenceclocktimercontrol**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) unterstützt. Wenn ein Filter beispielsweise eine Referenzuhr für das Filter Diagramm bereitstellen kann, kann er durch den Zugriff auf ein Hardware Gerät diese Klasse zum Implementieren der Uhr verwenden.

Das- `CBaseReferenceClock` Objekt verwaltet zwei unterschiedliche Uhrzeitwerte:

-   Intern gibt die [**cbasereferenceclock:: getprivatetime**](cbasereferenceclock-getprivatetime.md) -Methode die tatsächliche Zeit zurück, die von der Uhr aufbewahrt wird.
-   Extern gibt die [**cbasereferenceclock:: getTime**](cbasereferenceclock-gettime.md) -Methode die Verweis Zeit für das Filter Diagramm zurück.

Es ist gültig, dass die interne Uhr rückwärts in kurzen Zeitabständen ausgeführt wird. Wenn z. b. die Uhr vorwärts abweicht, kann Sie vom Filter rückwärts angepasst werden. (Siehe [**cbasereferenceclock:: settimedelta**](cbasereferenceclock-settimedelta.md).) Die **GetTime** -Methode verwendet die von **getprivatetime** gemeldeten Zeit Werte. Die Verweis Zeit nimmt jedoch monoton zu. Das heißt, es wird nie rückwärts ausgeführt. Wenn die interne Uhr rückwärts ausgeführt wird, meldet **GetTime** daher weiterhin die alte Zeit, bis die interne Uhr abfängt.

Beispielsweise können die beiden Methoden die folgenden Sequenzen zurückgeben:

``` syntax
GetPrivateTime: 105, 106, 103, 104, 105, 106, 107, 108
GetTime:        105, 106, 106, 106, 106, 106, 107, 108
```

Auf dem dritten Takt springt die interne Uhr rückwärts zu 103. Die **GetTime** -Methode meldet den Bericht 106 so lange, bis die interne Uhr wiederholt wird.

Standardmäßig gibt **getprivatetime** die Systemzeit durch einen Aufruf der **timeGetTime** -Funktion zurück. Ein Filter, der eine Referenzuhr von einem externen Gerät bereitstellt, kann eine der folgenden Aktionen ausführen:

-   Überschreiben Sie **getprivatetime** , um die Uhrzeit vom Gerät zurückzugeben.
-   Überwachen Sie die Diskrepanz zwischen der Geräte Zeit und der Systemzeit, und wenden Sie **settimedelta** an, um Korrekturen vorzunehmen.

Diese Klasse verwendet ein [**camschedule**](camschedule.md) -Objekt, um die Planung von Anforderungs Anforderungen zu verarbeiten. Weitere Informationen finden Sie in der Dokumentation für die Klasse " **camschedule** ".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ref. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




