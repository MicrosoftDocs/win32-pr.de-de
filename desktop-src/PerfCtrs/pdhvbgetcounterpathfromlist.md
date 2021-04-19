---
description: Die pdhvbgetcounterpathfromlist-Funktion kopiert den Indikator Pfad, auf den der Index-Parameter verweist, aus einer Indikator Pfad Liste, die vom Benutzer beim letzten Aufrufen der pdhvbkreatecounterpathlist-Funktion erstellt wurde.
ms.assetid: e77a022d-42f2-4c48-acb7-36cb013730dd
title: Pdhvbgetcounterpathfromlist-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathFromList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 4c5ae4632ede898b7cd323723037ea68d53455b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357758"
---
# <a name="pdhvbgetcounterpathfromlist-function"></a>Pdhvbgetcounterpathfromlist-Funktion

Die **pdhvbgetcounterpathfromlist** -Funktion kopiert den Indikator Pfad, auf den der Index-Parameter verweist, aus einer *Indikator* Pfad Liste, die vom Benutzer beim letzten Aufrufen der [**pdhvbkreatecounterpathlist**](pdhvbcreatecounterpathlist.md) -Funktion erstellt wurde.

> [!IMPORTANT]
> Die Funktion, die in diesem Thema beschrieben wird, kann in Zukunft geändert oder nicht mehr verfügbar sein. Stattdessen empfiehlt Microsoft die Verwendung der Funktionen, die unter [Funktionen von Leistungsindikatoren](performance-counters-functions.md)beschrieben werden.

Funktion "pdhvbgetcounterpathfromlist" ( \_ ByVal-Index "Long", \_ ByVal-Puffer als Zeichenfolge, \_ ByVal-BufferLength "Long" \_ )

## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* 
</dt> <dd>

Der Index des abzurufenden Indikator Pfads. Dies muss ein Wert sein, der größer oder gleich 1 und kleiner oder gleich dem Wert ist, der von der [**pdhvbkreatecounterpathlist**](pdhvbcreatecounterpathlist.md) -Funktion zurückgegeben wird.

</dd> <dt>

*Buffer* 
</dt> <dd>

Die dimensionierte und initialisierte Zeichenfolge, die den Indikator Pfad empfängt, der dem Wert des Index Parameters entspricht.

</dd> <dt>

*BufferLength* 
</dt> <dd>

Maximale Anzahl von Zeichen, die in die Zeichenfolge passt, auf die von Buffer verwiesen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt die Anzahl der in den Puffer kopierten Zeichen zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Bibliothek<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Pdhvbkreatecounterpathlist**](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[**Pdhvbgetcounterpathelements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**Pdhvbgetonecounterpath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




