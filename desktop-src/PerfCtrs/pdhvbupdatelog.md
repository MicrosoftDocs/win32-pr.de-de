---
description: Die Funktion pdhvbupdatelog Functions aktualisiert die aktuelle Abfrage und schreibt neue Daten in die Protokolldatei. Diese Funktion ruft pdhupdatelog auf.
ms.assetid: a7a3ad18-2d61-448e-9764-ba363398e804
title: Pdhvbupdatelog-Funktion
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
ms.openlocfilehash: c02e533f57481004b0a7de9f779399b20bddc0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349221"
---
# <a name="pdhvbupdatelog-function"></a>Pdhvbupdatelog-Funktion

Die Funktion **pdhvbupdatelog** Functions aktualisiert die aktuelle Abfrage und schreibt neue Daten in die Protokolldatei. Diese Funktion ruft [**pdhupdatelog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)auf.

> [!IMPORTANT]
> Die Funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen empfiehlt Microsoft die Verwendung der Funktionen, die unter [Funktionen von Leistungsindikatoren](performance-counters-functions.md)beschrieben werden.

Funktion pdhvbupdatelog ( \_ ByVal hlog as PDH \_ hlog, \_ ByVal szuserstring as LPCTSTR \_ )

## <a name="parameters"></a>Parameter

<dl> <dt>

*hlog* \[ in\]
</dt> <dd>

Handle für die zu Aktualisier Ende Protokolldatei. Dieses Handle wird von der [**pdhvbopenlog**](pdhvbopenlog.md) -Funktion zurückgegeben.

</dd> <dt>

*szuserstring* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die die Daten angibt, die der Protokolldatei hinzugefügt werden sollen. Dies wird im Allgemeinen für Kommentare in der Protokolldatei verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird 0 zurückgegeben.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein [Systemfehler Code](/windows/desktop/Debug/system-error-codes) oder ein [PDH-Fehlercode](pdh-error-codes.md). Die folgenden Werte sind möglich.



| Rückgabecode                                                                                                | Beschreibung                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nicht genügend PDH- \_ \_ Puffer**</dt> </dl>   | Die angeforderten Daten sind größer als der angegebene Puffer. Die angeforderten Daten können nicht zurückgegeben werden.<br/> |
| <dl> <dt>**Ungültiges PDH- \_ \_ Argument**</dt> </dl>      | Mindestens ein Zeichen folgen Puffer weist nicht die richtige Größe auf.<br/>                                  |
| <dl> <dt>**Ungültiges PDH- \_ \_ handle**</dt> </dl>        | Das Handle ist kein gültiges PDH-Objekt.<br/>                                                       |
| <dl> <dt>**Fehler beim Öffnen der PDH- \_ Protokoll \_ Datei. \_ \_**</dt> </dl> | Die angegebene Protokolldatei kann nicht geöffnet werden.<br/>                                                      |
| <dl> <dt>**PDH- \_ Datei wurde \_ nicht \_ gefunden.**</dt> </dl>       | Die angegebene Datei wurde nicht gefunden.<br/>                                                          |



 

## <a name="remarks"></a>Bemerkungen

Es muss eine aktuell geöffnete Abfrage vorhanden sein, und die gewünschten Zähler müssen hinzugefügt werden, bevor diese Funktion aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Bibliothek<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Pdhupdatelog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
</dt> <dt>

[**Pdhvbgetlogfilesize**](pdhvbgetlogfilesize.md)
</dt> <dt>

[**Pdhvbopenlog**](pdhvbopenlog.md)
</dt> </dl>

 

