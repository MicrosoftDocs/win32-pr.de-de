---
description: Die PdhVbGetLogFileSize-Funktion gibt die Größe der angegebenen Protokolldatei zurück. Diese Funktion ruft PdhGetLogFileSize auf.
ms.assetid: 8f4fbb68-b0f5-4163-ae6e-5b7139a35adf
title: PdhVbGetLogFileSize-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetLogFileSize
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: cd3925eee621ac205615f17b26767096151d459628ca7d331a7aaee3336b27ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674790"
---
# <a name="pdhvbgetlogfilesize-function"></a>PdhVbGetLogFileSize-Funktion

Die **PdhVbGetLogFileSize-Funktion gibt** die Größe der angegebenen Protokolldatei zurück. Diese Funktion ruft [**PdhGetLogFileSize auf.**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)

> [!IMPORTANT]
> Die funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen empfiehlt Microsoft die Verwendung der unter [Leistungsindikatorfunktionen beschriebenen Funktionen.](performance-counters-functions.md)

Funktion PdhVbGetLogFileSize( \_ ByVal hLog as PDH \_ HLOG, \_ ByRef llSize as LONG \_ ) as DWORD

## <a name="parameters"></a>Parameter

<dl> <dt>

*hLog* \[ In\]
</dt> <dd>

Handle für die Protokolldatei. Dieses Handle wird von der [**PdhOpenLog-Funktion**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) zurückgegeben.

</dd> <dt>

*llSize* \[ out\]
</dt> <dd>

Zeiger auf eine Variable, die die Größe der Protokolldatei in Bytes empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, wird 0 zurückgegeben.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein [Systemfehlercode oder](/windows/desktop/Debug/system-error-codes) [ein PDH-Fehlercode.](pdh-error-codes.md) Im Folgenden finden Sie mögliche Werte.



| Rückgabecode                                                                                                | Beschreibung                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NICHT AUSREICHENDER \_ \_ PDH-PUFFER**</dt> </dl>   | Die angeforderten Daten sind größer als der angegebene Puffer. Die angeforderten Daten können nicht zurückgeben werden.<br/> |
| <dl> <dt>**\_PDH: UNGÜLTIGES \_ ARGUMENT**</dt> </dl>      | Mindestens einer der Zeichenfolgenpuffer ist nicht die richtige Größe.<br/>                                  |
| <dl> <dt>**\_PDH: UNGÜLTIGES \_ HANDLE**</dt> </dl>        | Das Handle ist kein gültiges PDH-Objekt.<br/>                                                       |
| <dl> <dt>**FEHLER BEIM ÖFFNEN \_ DER \_ PDH-PROTOKOLLDATEI \_ \_**</dt> </dl> | Die angegebene Protokolldatei kann nicht geöffnet werden.<br/>                                                      |
| <dl> <dt>**\_PDH-DATEI \_ NICHT \_ GEFUNDEN**</dt> </dl>       | Die angegebene Datei wurde nicht finden.<br/>                                                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Bibliothek<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
</dt> <dt>

[**PdhVbOpenLog**](pdhvbopenlog.md)
</dt> <dt>

[**PdhVbUpdateLog**](pdhvbupdatelog.md)
</dt> </dl>

 

