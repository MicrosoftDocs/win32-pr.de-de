---
description: Diese Klasse ist die übergeordnete Klasse für Datenträger-e/a-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 630fb6c6-b505-4384-ab7b-ee898d95bd41
title: Diskio-Klasse
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
ms.openlocfilehash: 97f9907e4da51675bb1a5f562931e471ee0e133e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958755"
---
# <a name="diskio-class"></a>Diskio-Klasse

Diese Klasse ist die übergeordnete Klasse für Datenträger-e/a-Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{3d6fa8d4-fe05-11d0-9dda-00c04fd7ba7c}")]
class DiskIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **diskio** -Klasse definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Wenn Sie Datenträger-e/a-Ereignisse in einer NT-Kernel Protokollierungs Sitzung aktivieren möchten, geben Sie das Flag für die Ereignis Ablaufverfolgungsflag für Datenträger- [](/windows/win32/api/evntrace/nf-evntrace-starttracea) e/a im **enableflags** -Member einer Eigenschaften Struktur der [**Ereignis Ablauf \_ Verfolgung \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an **\_ \_ \_ \_** Sie können auch eines oder mehrere der folgenden Flags angeben:

-   **Ereignis \_ Ablauf \_ Verfolgung \_ Flag \_ Daten \_ Träger-e/a**
-   **Ereignis Ablauf Verfolgungs Kennzeichen- \_ \_ \_ Treiber**

Consumer der Ereignis Ablauf Verfolgung können eine spezielle Verarbeitung für Datenträger-e/a-Ereignisse implementieren, indem Sie die Funktion [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**diskioguid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben. Verwenden Sie die folgenden Ereignis Typen, um das tatsächliche Datenträger-e/a-Ereignis beim Verarbeiten von Ereignissen zu identifizieren.



| Ereignistyp                                                                      | BESCHREIBUNG                                                                                                                                                   |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ereignis \_ E \_ \_ \_**/a-Ablaufverfolgungstyp<br/>             | Lese Ereignis. Die [**diskio \_ TypeGroup1**](diskio-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                              |
| **Ereignis \_ E/a-Schreibvorgänge des \_ \_ ablaufverfolgungstyps \_**<br/>            | Schreib Ereignis. Die [**diskio \_ TypeGroup1**](diskio-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                             |
| **Ereignis \_ Ablaufverfolgungstyp-e/a \_ \_ \_ Lesen \_ Init**(Ereignistyp ist 12)<br/>       | Lese Ereignis initialisieren. Die [**diskio \_ TypeGroup2**](diskio-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                   |
| **Ereignis \_ E/a- \_ \_ \_ \_ Ablaufverfolgungstyp**<br/>      | Initialisieren Sie das Schreib Ereignis. Die [**diskio \_ TypeGroup2**](diskio-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                  |
| **Ereignis \_ E \_ \_ \_**/a-Leerung des Ablauf Verfolgungs Typs (Ereignistyp ist 14<br/>            | Initialisieren Sie das Schreib Ereignis. Die [**diskio \_ TypeGroup3**](diskio-typegroup3.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                  |
| **Ereignis \_ Ablauf Verfolgungs Typen-e/a-Leerungs- \_ \_ \_ \_ Init**<br/>      | Lösch Ereignis initialisieren. Die [**diskio \_ TypeGroup2**](diskio-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                  |
| **Ereignis \_ \_ \_ \_ Umgeleiteter \_** e/a-Ablaufverfolgungstyp<br/> | Initialisieren Sie das umgeleitete Ereignis. Umgeleitete e/a-Ereignisse werden verwendet, um die Datenträger-e/a-Vorgänge in einem Windows-Abbild Format (WIM) dem Dateinamen                  |
| Der Ereignistyp Wert ist 52<br/>                                               | Anforderungs Ereignis für Treiber Abschluss. Die " [**drivercompleterequest**](drivercompleterequest.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                    |
| Der Ereignistyp Wert ist 53<br/>                                               | Das Anforderungs Rückgabe Ereignis des Treibers wurde beendet. Die " [**drivercompleterequestreturn**](drivercompleterequestreturn.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis. |
| Der Ereignistyp Wert ist 37<br/>                                               | Routine Ereignis für Treiber Abschluss. Die MOF-Klasse [**drivercompletionroutine**](drivercompletionroutine.md) definiert die Ereignisdaten für dieses Ereignis.              |
| Der Ereignistyp Wert ist 34<br/>                                               | Ereignis des Haupt Funktions aufrufdes Treibers. Die " [**drivermajorfunctioncallmof**](drivermajorfunctioncall.md) "-Klasse definiert die Ereignisdaten für dieses Ereignis.             |
| Der Ereignistyp Wert ist 35<br/>                                               | Ereignis für den Haupt Funktions Rückruf des Treibers. Die " [**drivermajorfunctionreturn**](drivermajorfunctionreturn.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.  |



 

Der Datenträger-e/a-Anbieter kann nicht ermitteln, welche Datei während eines Datenträger-e/a-Ereignisses gelesen oder geschrieben wird. Aktivieren Sie den Datei-e/a-Ereignis Anbieter, um den Namen der Datei abzurufen, die dem Datenträger-e/a-Ereignis zugeordnet ist.

Datenträger-e/a-Ereignisse werden zum Zeitpunkt des e/a-Abschlusses aufgezeichnet. Um zu ermitteln, wann der e/a-Vorgang begonnen hat, verwenden Sie die Initialisierungs Ereignisse, z. b. den Ereignis Ablauf \_ Verfolgungs \_ Typ \_ IO \_ Read \_ init.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Diskio \_ TypeGroup1**](diskio-typegroup1.md)
</dt> <dt>

[**Diskio \_ TypeGroup2**](diskio-typegroup2.md)
</dt> <dt>

[**Diskio \_ TypeGroup3**](diskio-typegroup3.md)
</dt> <dt>

[**Drivercompleterequest**](drivercompleterequest.md)
</dt> <dt>

[**Drivercompleterequestreturn**](drivercompleterequestreturn.md)
</dt> <dt>

[**Drivercompletionroutine**](drivercompletionroutine.md)
</dt> <dt>

[**Drivermajorfunctioncallcenter**](drivermajorfunctioncall.md)
</dt> <dt>

[**Drivermajorfunctionreturn**](drivermajorfunctionreturn.md)
</dt> </dl>

 

 
