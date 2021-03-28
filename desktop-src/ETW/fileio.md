---
description: Diese Klasse ist die übergeordnete Klasse für Datei-e/a-Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 8e006a63-a061-4b62-8f90-b8c8823bb047
title: Klasse "fleio"
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
ms.openlocfilehash: 2f7c032cb7af325efa1d2ea76702068fc7b3be62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978849"
---
# <a name="fileio-class"></a>Klasse "fleio"

Diese Klasse ist die übergeordnete Klasse für Datei-e/a-Ereignisse.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{90cbdc39-4a3e-11d1-84f4-0000f80464e3}"), EventVersion(2)]
class FileIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Member

Die Klasse " **fleio** " definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Wenn Sie die Datei-e/a-Ereignisse in einer NT-Kernel Protokollierungs Sitzung aktivieren möchten, geben Sie beim Aufrufen der [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion das Flag für die **\_ \_ \_ ablaufverfolgungsdatenträgerdatei \_ \_** -e/a im **enableflags** -Member der [**\_ \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) Sie können auch eines oder mehrere der folgenden Flags angeben:

-   **Datei-e/a \_ \_ \_ \_**
-   **Ereignis Ablauf Verfolgungs Kennzeichen- \_ \_ \_ Datei \_ \_**

Ereignisablaufverfolgungs-Consumer können eine spezielle Verarbeitung für Datei-e/a-Ereignisse implementieren, indem Sie die [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) -Funktion aufrufen und als *pguid* -Parameter " [**fleioguid**](nt-kernel-logger-constants.md) " angeben Verwenden Sie die folgenden Ereignis Typen, um das tatsächliche Ereignis beim Verarbeiten von Ereignissen zu identifizieren.



| Ereignistyp             | BESCHREIBUNG                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Der Ereignistyp Wert ist 0.  | Dateiname-Ereignis. Die Klasse " [**fleio \_ Name**](fileio-name.md) MOF" definiert die Ereignisdaten für dieses Ereignis.                                                                               |
| Der Ereignistyp Wert ist 32 | Ereignis zum Erstellen der Datei. Die Klasse " [**fleio \_ Name**](fileio-name.md) MOF" definiert die Ereignisdaten für dieses Ereignis.                                                                             |
| Der Ereignistyp Wert ist 35 | Ereignis zum Löschen von Dateien. Die Klasse " [**fleio \_ Name**](fileio-name.md) MOF" definiert die Ereignisdaten für dieses Ereignis.                                                                             |
| Der Ereignistyp Wert ist 36 | Dateirundown-Ereignis. Listet alle geöffneten Dateien auf dem Computer am Ende der Ablauf Verfolgungs Sitzung auf. Die Klasse " [**fleio \_ Name**](fileio-name.md) MOF" definiert die Ereignisdaten für dieses Ereignis. |
| Der Ereignistyp Wert ist 64 | Ereignis zum Erstellen der Datei. Die "MOF"-Klasse " [**fleio \_ Create**](fileio-create.md) " definiert die Ereignisdaten für dieses Ereignis.                                                                         |
| Der Ereignistyp Wert ist 72 | Verzeichnisenumerationsereignis. Die Klasse " [**fleio \_ direnum**](fileio-direnum.md) MOF" definiert die Ereignisdaten für dieses Ereignis.                                                             |
| Der Ereignistyp Wert ist 77 | Verzeichnis Benachrichtigungs Ereignis. Die Klasse " [**fleio \_ direnum**](fileio-direnum.md) MOF" definiert die Ereignisdaten für dieses Ereignis.                                                            |
| Der Ereignistyp Wert ist 69 | Legen Sie das Informations Ereignis fest. Die " [**fleio \_ Info**](fileio-info.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                         |
| Der Ereignistyp Wert ist 70 | Datei Ereignis löschen. Die " [**fleio \_ Info**](fileio-info.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                             |
| Der Ereignistyp Wert ist 71 | Datei Ereignis umbenennen. Die " [**fleio \_ Info**](fileio-info.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                             |
| Der Ereignistyp Wert ist 74 | Ereignis für Abfrage Dateiinformationen. Die " [**fleio \_ Info**](fileio-info.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                  |
| Der Ereignistyp Wert ist 75 | Dateisystem-Steuerungs Ereignis. Die " [**fleio \_ Info**](fileio-info.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.                                                                     |
| Der Ereignistyp Wert ist 76 | Ende des Vorgangs Ereignisses. Die Klasse " [**fleio \_ opend**](fileio-opend.md) MOF" definiert die Ereignisdaten für dieses Ereignis.                                                                      |
| Der Ereignistyp Wert ist 67 | Datei Lese Ereignis. Die MOF-Klasse " [**fleio Read \_ Write**](fileio-readwrite.md) " definiert die Ereignisdaten für dieses Ereignis.                                                                     |
| Der Ereignistyp Wert ist 68 | Datei Schreib Ereignis. Die MOF-Klasse " [**fleio Read \_ Write**](fileio-readwrite.md) " definiert die Ereignisdaten für dieses Ereignis.                                                                    |
| Der Ereignistyp Wert ist 65 | Bereinigen Sie das Ereignis. Das-Ereignis wird generiert, wenn das letzte Handle der Datei freigegeben wird. Die MOF-Klasse " [**fleio \_ simpleop**](fileio-simpleop.md) " definiert die Ereignisdaten für dieses Ereignis.   |
| Der Ereignistyp Wert ist 66 | Schließen Sie das Ereignis. Das-Ereignis wird generiert, wenn das File-Objekt freigegeben wird. Die MOF-Klasse " [**fleio \_ simpleop**](fileio-simpleop.md) " definiert die Ereignisdaten für dieses Ereignis.                     |
| Der Ereignistyp Wert ist 73 | Flush-Ereignis. Dieses Ereignis wird generiert, wenn die Datei Puffer vollständig auf den Datenträger geleert werden. Die MOF-Klasse " [**fleio \_ simpleop**](fileio-simpleop.md) " definiert die Ereignisdaten für dieses Ereignis.  |



 

Datei-e/a-Ereignisse werden zu Beginn des Vorgangs protokolliert.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSNT \_ systemtrace**](msnt-systemtrace.md)
</dt> <dt>

[**"Fleio \_ v0"**](fileio-v0.md)
</dt> <dt>

[**Fleio \_ v1**](fileio-v1.md)
</dt> </dl>

 

 
