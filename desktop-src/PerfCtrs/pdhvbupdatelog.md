---
description: Die Funktion PdhVbUpdateLog aktualisiert die aktuelle Abfrage und schreibt neue Daten in die Protokolldatei. Diese Funktion ruft PdhUpdateLog auf.
ms.assetid: a7a3ad18-2d61-448e-9764-ba363398e804
title: PdhVbUpdateLog-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbUpdateLog
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: c7bf8af71d3a0f5cd20a84ef0f1532806e3d3e8d268bd2d322d617534b533cc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033610"
---
# <a name="pdhvbupdatelog-function"></a>PdhVbUpdateLog-Funktion

Die **Funktion PdhVbUpdateLog** aktualisiert die aktuelle Abfrage und schreibt neue Daten in die Protokolldatei. Diese Funktion ruft [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)auf.

> [!IMPORTANT]
> Die in diesem Thema beschriebene Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen empfiehlt Microsoft die Verwendung der in [Leistungsindikatorfunktionen beschriebenen](performance-counters-functions.md)Funktionen.

Funktion PdhVbUpdateLog( \_ ByVal hLog as PDH \_ HLOG, \_ ByVal szUserString As LPCTSTR \_ )

## <a name="parameters"></a>Parameter

<dl> <dt>

*hLog* \[ In\]
</dt> <dd>

Behandeln Sie die zu aktualisierende Protokolldatei. Dieses Handle wird von der [**PdhVbOpenLog-Funktion**](pdhvbopenlog.md) zurückgegeben.

</dd> <dt>

*szUserString* \[ In\]
</dt> <dd>

Zeiger auf eine Zeichenfolge, die die Daten angibt, die der Protokolldatei hinzugefügt werden sollen. Dies wird in der Regel für Kommentare in der Protokolldatei verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, wird 0 zurückgegeben.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein [Systemfehlercode](/windows/desktop/Debug/system-error-codes) oder ein [PDH-Fehlercode.](pdh-error-codes.md) Im Folgenden sind mögliche Werte angegeben.



| Rückgabecode                                                                                                | Beschreibung                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**PDH \_ INSUFFICIENT \_ BUFFER**</dt> </dl>   | Die angeforderten Daten sind größer als der bereitgestellte Puffer. Die angeforderten Daten können nicht zurückgegeben werden.<br/> |
| <dl> <dt>**\_UNGÜLTIGES \_ PDH-ARGUMENT**</dt> </dl>      | Mindestens einer der Zeichenfolgenpuffer ist nicht die richtige Größe.<br/>                                  |
| <dl> <dt>**\_UNGÜLTIGES \_ PDH-HANDLE**</dt> </dl>        | Das Handle ist kein gültiges PDH-Objekt.<br/>                                                       |
| <dl> <dt>**FEHLER BEIM \_ ÖFFNEN DER PDH-PROTOKOLLDATEI \_ \_ \_**</dt> </dl> | Die angegebene Protokolldatei kann nicht geöffnet werden.<br/>                                                      |
| <dl> <dt>**\_PDH-DATEI \_ NICHT \_ GEFUNDEN**</dt> </dl>       | Die angegebene Datei konnte nicht gefunden werden.<br/>                                                          |



 

## <a name="remarks"></a>Hinweise

Es muss eine derzeit geöffnete Abfrage vorhanden sein, und die gewünschten Leistungsindikatoren müssen ihr hinzugefügt werden, bevor diese Funktion aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Bibliothek<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
</dt> <dt>

[**PdhVbGetLogFileSize**](pdhvbgetlogfilesize.md)
</dt> <dt>

[**PdhVbOpenLog**](pdhvbopenlog.md)
</dt> </dl>

 

