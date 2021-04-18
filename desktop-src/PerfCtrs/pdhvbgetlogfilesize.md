---
description: Die pdhvbgetlogfilesize-Funktion gibt die Größe der angegebenen Protokolldatei zurück. Diese Funktion ruft pdhgetlogfilesize auf.
ms.assetid: 8f4fbb68-b0f5-4163-ae6e-5b7139a35adf
title: Pdhvbgetlogfilesize-Funktion
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
ms.openlocfilehash: 0b9f490477704086bd9aa8c53dd32456d486471e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359045"
---
# <a name="pdhvbgetlogfilesize-function"></a>Pdhvbgetlogfilesize-Funktion

Die **pdhvbgetlogfilesize** -Funktion gibt die Größe der angegebenen Protokolldatei zurück. Diese Funktion ruft [**pdhgetlogfilesize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)auf.

> [!IMPORTANT]
> Die Funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen empfiehlt Microsoft die Verwendung der Funktionen, die unter [Funktionen von Leistungsindikatoren](performance-counters-functions.md)beschrieben werden.

Funktion "pdhvbgetlogfilesize" ( \_ ByVal hlog as PDH \_ hlog, \_ ByRef llsize als Long \_ ) als DWORD

## <a name="parameters"></a>Parameter

<dl> <dt>

*hlog* \[ in\]
</dt> <dd>

Handle für die Protokolldatei. Dieses Handle wird von der [**pdhopenlog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga) -Funktion zurückgegeben.

</dd> <dt>

*llsize* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe der Protokolldatei (in Bytes) empfängt.

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



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Bibliothek<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Pdhgetlogfilesize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
</dt> <dt>

[**Pdhvbopenlog**](pdhvbopenlog.md)
</dt> <dt>

[**Pdhvbupdatelog**](pdhvbupdatelog.md)
</dt> </dl>

 

