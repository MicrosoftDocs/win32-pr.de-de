---
description: 'FileIo-Klasse: Diese Klasse ist die übergeordnete Klasse für Datei-E/A-Ereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
ms.assetid: 8e006a63-a061-4b62-8f90-b8c8823bb047
title: FileIo-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 716528902a115e23eae5b49ef572b87a71d11e25
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106528"
---
# <a name="fileio-class"></a>FileIo-Klasse

Diese Klasse ist die übergeordnete Klasse für Datei-E/A-Ereignisse.

Die folgende Syntax wird durch MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{90cbdc39-4a3e-11d1-84f4-0000f80464e3}"), EventVersion(2)]
class FileIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die **FileIo-Klasse** definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Um die Datei-E/A-Ereignisse in einer NT-Kernelprotokollierungssitzung zu aktivieren, geben Sie beim Aufrufen der [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) das **FLAG EVENT TRACE FLAG DISK FILE \_ \_ \_ \_ \_ IO** im **EnableFlags-Member** einer [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an. Sie können auch eines oder mehrere der folgenden Flags angeben:

-   **\_ \_ EREIGNISVERFOLGUNGSFLAGDATEI \_ \_ E/A**
-   **\_ \_ EREIGNIS-ABLAUFVERFOLGUNGSFLAGDATEI \_ IO \_ \_ INIT**

Ereignisverfolgungsverbraucher können eine spezielle Verarbeitung für Datei-E/A-Ereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**FileIoGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben. Verwenden Sie die folgenden Ereignistypen, um das tatsächliche Ereignis bei der Nutzung von Ereignissen zu identifizieren.



| Ereignistyp             | BESCHREIBUNG                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ereignistypwert ist 0  | Dateinamenereignis. Die [**MOF-Klasse FileIo \_ Name**](fileio-name.md) definiert die Ereignisdaten für dieses Ereignis.                                                                               |
| Der Ereignistypwert ist 32. | Datei-Erstellungsereignis. Die [**MOF-Klasse FileIo \_ Name**](fileio-name.md) definiert die Ereignisdaten für dieses Ereignis.                                                                             |
| Der Ereignistypwert ist 35 | Dateilöschereignis. Die [**MOF-Klasse FileIo \_ Name**](fileio-name.md) definiert die Ereignisdaten für dieses Ereignis.                                                                             |
| Der Ereignistypwert ist 36. | Datei-Rundownereignis. Listet alle geöffneten Dateien auf dem Computer am Ende der Ablaufverfolgungssitzung auf. Die [**MOF-Klasse FileIo \_ Name**](fileio-name.md) definiert die Ereignisdaten für dieses Ereignis. |
| Der Ereignistypwert ist 64. | Dateierstellungsereignis. Die [**FILEIO \_ CREATE**](fileio-create.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                         |
| Der Ereignistypwert ist 72. | Verzeichnisenumerationsereignis. Die [**FileIo \_ DirEnum**](fileio-direnum.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                             |
| Der Ereignistypwert ist 77. | Verzeichnisbenachrichtigungsereignis. Die [**FileIo \_ DirEnum**](fileio-direnum.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                            |
| Der Ereignistypwert ist 69. | Ereignis zum Festlegen von Informationen. Die [**MOF-Klasse FileIo \_ Info**](fileio-info.md) definiert die Ereignisdaten für dieses Ereignis.                                                                         |
| Der Ereignistypwert ist 70. | Dateiereignis löschen. Die [**MOF-Klasse FileIo \_ Info**](fileio-info.md) definiert die Ereignisdaten für dieses Ereignis.                                                                             |
| Der Ereignistypwert ist 71. | Dateiereignis umbenennen. Die [**MOF-Klasse FileIo \_ Info**](fileio-info.md) definiert die Ereignisdaten für dieses Ereignis.                                                                             |
| Der Ereignistypwert ist 74 | Abfragedateiinformationsereignis. Die [**MOF-Klasse FileIo \_ Info**](fileio-info.md) definiert die Ereignisdaten für dieses Ereignis.                                                                  |
| Der Ereignistypwert ist 75. | Dateisystem-Steuerungsereignis. Die [**MOF-Klasse FileIo \_ Info**](fileio-info.md) definiert die Ereignisdaten für dieses Ereignis.                                                                     |
| Der Ereignistypwert ist 76 | Ereignis zum Ende des Vorgangs. Die [**MOF-Klasse FileIo \_ OpEnd**](fileio-opend.md) definiert die Ereignisdaten für dieses Ereignis.                                                                      |
| Der Ereignistypwert ist 67. | Dateileseereignis. Die [**\_ MOF-Klasse FileIo ReadWrite**](fileio-readwrite.md) definiert die Ereignisdaten für dieses Ereignis.                                                                     |
| Der Ereignistypwert ist 68 | Datei-Schreibereignis. Die [**\_ MOF-Klasse FileIo ReadWrite**](fileio-readwrite.md) definiert die Ereignisdaten für dieses Ereignis.                                                                    |
| Der Ereignistypwert ist 65 | Clean up-Ereignis. Das Ereignis wird generiert, wenn das letzte Handle für die Datei freigegeben wird. Die [**FileIo \_ SimpleOp**](fileio-simpleop.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.   |
| Der Ereignistypwert ist 66. | Close-Ereignis. Das Ereignis wird generiert, wenn das Dateiobjekt freigegeben wird. Die [**FileIo \_ SimpleOp**](fileio-simpleop.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.                     |
| Der Ereignistypwert ist 73. | Flush-Ereignis. Dieses Ereignis wird generiert, wenn die Dateipuffer vollständig auf den Datenträger geleert werden. Die [**FileIo \_ SimpleOp**](fileio-simpleop.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.  |



 

Datei-E/A-Ereignisse werden zu Beginn des Vorgangs protokolliert.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**FileIo \_ V0**](fileio-v0.md)
</dt> <dt>

[**FileIo \_ V1**](fileio-v1.md)
</dt> </dl>

 

 
