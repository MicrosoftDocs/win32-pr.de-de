---
description: Diese Klasse ist die übergeordnete Klasse für Datenträger-E/A-Ereignisse. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 630fb6c6-b505-4384-ab7b-ee898d95bd41
title: DiskIo-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0e91f5e8b84d77b0938f35da69a84c26fa0f34a4da63bce40330484a29e19b5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118395301"
---
# <a name="diskio-class"></a>DiskIo-Klasse

Diese Klasse ist die übergeordnete Klasse für Datenträger-E/A-Ereignisse.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{3d6fa8d4-fe05-11d0-9dda-00c04fd7ba7c}")]
class DiskIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **DiskIo-Klasse** definiert keine Member.

## <a name="remarks"></a>Hinweise

Um Datenträger-I/0-Ereignisse in einer NT-Kernelprotokollierungssitzung zu aktivieren, geben Sie beim Aufrufen der [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) das **EVENT TRACE FLAG DISK \_ \_ \_ \_ IO-Flag** im **EnableFlags-Member** einer [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an. Sie können auch eines oder mehrere der folgenden Flags angeben:

-   **\_ \_ EREIGNISVERFOLGUNGSFLAG \_ DISK IO \_ \_ INIT**
-   **\_ \_ EREIGNISVERFOLGUNGSFLAGTREIBER \_**

Ereignisverfolgungsverbraucher können eine spezielle Verarbeitung für Datenträger-E/A-Ereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**DiskIoGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben. Verwenden Sie die folgenden Ereignistypen, um das tatsächliche Datenträger-E/A-Ereignis beim Nutzen von Ereignissen zu identifizieren.



| Ereignistyp                                                                      | BESCHREIBUNG                                                                                                                                                   |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENT \_ TRACE \_ TYPE \_ IO \_ READ**(Ereignistypwert ist 10)<br/>             | Liest das Ereignis. Die [**\_ MOF-Klasse DiskIo TypeGroup1**](diskio-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                              |
| **EVENT \_ TRACE \_ TYPE \_ IO \_ WRITE**(Ereignistypwert ist 11)<br/>            | Schreibereignis. Die [**\_ MOF-Klasse DiskIo TypeGroup1**](diskio-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.                                             |
| **EVENT \_ TRACE \_ TYPE IO READ \_ \_ \_ INIT**(Ereignistypwert ist 12)<br/>       | Initialisieren sie das Leseereignis. Die [**\_ MOF-Klasse DiskIo TypeGroup2**](diskio-typegroup2.md) definiert die Ereignisdaten für dieses Ereignis.                                   |
| **EVENT \_ TRACE \_ TYPE IO WRITE \_ \_ \_ INIT**(Ereignistypwert ist 13)<br/>      | Initialisieren sie das Schreibereignis. Die [**\_ MOF-Klasse DiskIo TypeGroup2**](diskio-typegroup2.md) definiert die Ereignisdaten für dieses Ereignis.                                  |
| **EVENT \_ TRACE \_ TYPE \_ IO \_ FLUSH**(Ereignistypwert ist 14)<br/>            | Initialisieren sie das Schreibereignis. Die [**\_ MOF-Klasse DiskIo TypeGroup3**](diskio-typegroup3.md) definiert die Ereignisdaten für dieses Ereignis.                                  |
| **EVENT \_ TRACE \_ TYPE IO FLUSH \_ \_ \_ INIT**(Ereignistypwert ist 15)<br/>      | Initialisieren des Flush-Ereignisses. Die [**\_ MOF-Klasse DiskIo TypeGroup2**](diskio-typegroup2.md) definiert die Ereignisdaten für dieses Ereignis.                                  |
| **EVENT \_ TRACE \_ TYPE \_ IO \_ REDIRECTED \_ INIT**(Ereignistypwert ist 16)<br/> | Initialisieren sie das umgeleitete Ereignis. Umgeleitete E/A-Ereignisse werden verwendet, um Datenträger-E/A einem Windows Imaging Format (WIM) dem Dateinamen innerhalb der WIM-Datei zu zuordnen.                  |
| Der Ereignistypwert ist 52<br/>                                               | Anforderungsereignis zum Abschließen des Treibers. Die [**MOF-Klasse DriverCompleteRequest**](drivercompleterequest.md) definiert die Ereignisdaten für dieses Ereignis.                    |
| Der Ereignistypwert ist 53.<br/>                                               | Rückgabeereignis für anforderungsvervollständigende Treiber. Die [**MOF-Klasse DriverCompleteRequestReturn**](drivercompleterequestreturn.md) definiert die Ereignisdaten für dieses Ereignis. |
| Der Ereignistypwert ist 37.<br/>                                               | Routineereignis zur Treiberabschlussroutine. Die [**MOF-Klasse DriverCompletionRoutine**](drivercompletionroutine.md) definiert die Ereignisdaten für dieses Ereignis.              |
| Der Ereignistypwert ist 34<br/>                                               | Hauptfunktionsaufrufereignis des Treibers. Die [**MOF-Klasse DriverMajorFunctionCall**](drivermajorfunctioncall.md) definiert die Ereignisdaten für dieses Ereignis.             |
| Der Ereignistypwert ist 35<br/>                                               | Rückgabeereignis für Hauptfunktionsaufrufe des Treibers. Die [**MOF-Klasse DriverMajorFunctionReturn**](drivermajorfunctionreturn.md) definiert die Ereignisdaten für dieses Ereignis.  |



 

Der Datenträger-E/A-Anbieter kann nicht identifizieren, welche Datei während eines Datenträger-E/A-Ereignisses gelesen oder geschrieben wird. Um den Namen der Datei abzurufen, die dem Datenträger-E/A-Ereignis zugeordnet ist, aktivieren Sie den Datei-E/A-Ereignisanbieter.

Datenträger-E/A-Ereignisse werden zum Zeitpunkt der E/A-Beendigung aufgezeichnet. Um zu bestimmen, wann der E/A-Vorgang begonnen hat, verwenden Sie die Initialisierungsereignisse, z. B. EVENT \_ TRACE TYPE IO READ \_ \_ \_ \_ INIT.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DiskIo \_ TypeGroup1**](diskio-typegroup1.md)
</dt> <dt>

[**DiskIo \_ TypeGroup2**](diskio-typegroup2.md)
</dt> <dt>

[**DiskIo \_ TypeGroup3**](diskio-typegroup3.md)
</dt> <dt>

[**DriverCompleteRequest**](drivercompleterequest.md)
</dt> <dt>

[**DriverCompleteRequestReturn**](drivercompleterequestreturn.md)
</dt> <dt>

[**DriverCompletionRoutine**](drivercompletionroutine.md)
</dt> <dt>

[**DriverMajorFunctionCall**](drivermajorfunctioncall.md)
</dt> <dt>

[**DriverMajorFunctionReturn**](drivermajorfunctionreturn.md)
</dt> </dl>

 

 
